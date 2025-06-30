# Cisco Appliances Router ISO Images

A comprehensive collection of Cisco networking appliances, router ISO images, and network operating system images specifically curated for GNS3 network simulation and emulation.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation Guide](#installation-guide)
- [Supported Devices](#supported-devices)
- [Usage Instructions](#usage-instructions)
- [Configuration Examples](#configuration-examples)
- [Troubleshooting](#troubleshooting)
- [Legal Disclaimer](#legal-disclaimer)
- [Contributing](#contributing)
- [Related Resources](#related-resources)
- [Support](#support)

## 🌟 Overview

This repository provides a curated collection of Cisco network appliance images and ISO files for use with GNS3 (Graphical Network Simulator-3). These images enable network engineers, students, and IT professionals to create realistic network topologies for learning, testing, and certification preparation without requiring physical hardware.

## ✨ Features

- **Comprehensive Collection**: Wide range of Cisco router and switch images
- **GNS3 Optimized**: Pre-configured and tested for GNS3 compatibility
- **Educational Focus**: Perfect for CCNA, CCNP, and CCIE preparation
- **Lab Environment**: Ideal for creating complex network topologies
- **Version Variety**: Multiple IOS versions for different use cases

## 🔧 Prerequisites

Before using these images, ensure you have:

### Software Requirements
- **GNS3**: Version 2.2.0 or higher
- **Operating System**: Windows 10/11, macOS 10.14+, or Linux (Ubuntu 18.04+)
- **Virtualization**: 
  - VMware Workstation/Fusion, or
  - VirtualBox 6.0+, or
  - QEMU/KVM (Linux)

### Hardware Requirements
- **RAM**: Minimum 8GB (16GB+ recommended)
- **Storage**: At least 20GB free space
- **CPU**: Modern multi-core processor with virtualization support
- **Network**: Internet connection for initial setup

### Legal Requirements
- Valid Cisco licensing for commercial use
- Educational use compliance with institutional agreements
- Understanding of intellectual property rights

## 📥 Installation Guide

### Step 1: Download GNS3
```bash
# Download from official website
https://gns3.com/software/download
```

### Step 2: Clone Repository
```bash
git clone https://github.com/Raimal-Raja/Cisco_Appliances_Router_ISO_Images.git
cd Cisco_Appliances_Router_ISO_Images
```

### Step 3: Import Images to GNS3
1. Open GNS3
2. Go to **Edit** → **Preferences**
3. Navigate to **Dynamips** → **IOS routers**
4. Click **New** to add router images
5. Browse and select the downloaded ISO files
6. Configure platform settings as needed

### Step 4: Verify Installation
1. Create a new project in GNS3
2. Drag and drop a router from the device panel
3. Power on the device
4. Access console to verify functionality

## 🖥️ Supported Devices

### Router Series
- **Cisco 1700 Series**: 1720, 1721, 1750, 1751, 1760
- **Cisco 2600 Series**: 2610, 2611, 2620, 2621, 2650, 2651
- **Cisco 2800 Series**: 2801, 2811, 2821, 2851
- **Cisco 3600 Series**: 3620, 3640, 3660
- **Cisco 3700 Series**: 3725, 3745
- **Cisco 7200 Series**: 7206VXR

### Switch Platforms
- **Cisco Catalyst**: 3560, 3750 series (IOU images)
- **Cisco ASA**: Firewall appliances
- **Cisco NX-OS**: Nexus switch emulation

### IOS Versions
- IOS 12.x series
- IOS 15.x series
- IOS-XE images
- NX-OS images

## 🚀 Usage Instructions

### Basic Router Configuration
```bash
# Initial setup commands
enable
configure terminal
hostname Router1
interface fastethernet0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
```

### Creating Network Topologies
1. **Simple Network**: Router-Switch-PC configuration
2. **OSPF Network**: Multi-area OSPF implementation
3. **BGP Lab**: Internet routing simulation
4. **VPN Setup**: Site-to-site VPN configuration

### Best Practices
- **Resource Management**: Limit concurrent device instances
- **Save Configurations**: Regular backup of device configs
- **Version Control**: Document IOS versions used in labs
- **Performance Tuning**: Optimize idle-pc values

## 🎯 Configuration Examples

### OSPF Configuration
```cisco
router ospf 1
network 192.168.1.0 0.0.0.255 area 0
network 10.0.0.0 0.0.0.255 area 1
```

### VLAN Configuration
```cisco
vlan 10
name Sales
vlan 20
name Engineering
interface fastethernet0/1
switchport mode access
switchport access vlan 10
```

### ACL Configuration
```cisco
access-list 100 permit tcp 192.168.1.0 0.0.0.255 any eq 80
access-list 100 deny ip any any
interface fastethernet0/0
ip access-group 100 in
```

## 🔧 Troubleshooting

### Common Issues

#### Image Won't Boot
- **Solution**: Check idle-pc value and platform settings
- **Command**: Calculate idle-pc in GNS3 console

#### High CPU Usage
- **Solution**: Configure appropriate idle-pc values
- **Recommendation**: Use auto-calculation feature

#### Memory Errors
- **Solution**: Increase allocated RAM for devices
- **Minimum**: 128MB for basic routing, 256MB+ for advanced features

#### Console Access Issues
- **Solution**: Verify console settings in device properties
- **Check**: Telnet port assignments and firewall settings

### Performance Optimization
```bash
# Optimize GNS3 performance
- Use SSD storage for better I/O
- Allocate sufficient RAM per device
- Enable hardware acceleration when available
- Close unnecessary applications while running labs
```

## ⚖️ Legal Disclaimer

**IMPORTANT LEGAL NOTICE:**

This repository is intended for **educational and learning purposes only**. Users must comply with all applicable laws and licensing agreements:

- **Cisco Licensing**: Ensure you have proper licensing for commercial use
- **Educational Use**: Verify compliance with institutional agreements
- **Personal Use**: Understand limitations for personal learning environments
- **Distribution**: Do not redistribute copyrighted materials
- **Compliance**: Follow all applicable software licensing terms

The repository maintainers are not responsible for any misuse of the provided materials.

## 🤝 Contributing

We welcome contributions to improve this repository:

### How to Contribute
1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/new-images`)
3. **Add** new images with proper documentation
4. **Test** compatibility with latest GNS3 versions
5. **Submit** a pull request with detailed description

### Contribution Guidelines
- Verify image functionality before submission
- Include proper documentation for new images
- Follow naming conventions for consistency
- Test with multiple GNS3 versions when possible

## 📚 Related Resources

### Official Documentation
- [GNS3 Official Website](https://gns3.com/)
- [GNS3 Documentation](https://docs.gns3.com/)
- [Cisco Learning Network](https://learningnetwork.cisco.com/)
- [Cisco DevNet](https://developer.cisco.com/)

### GNS3 Resources
- [GNS3 Academy](https://gns3.com/training)
- [GNS3 Community](https://gns3.com/community)
- [GNS3 Marketplace](https://gns3.com/marketplace)
- [GNS3 YouTube Channel](https://www.youtube.com/c/GNS3network)

### Alternative Image Sources
- [Cisco Images for GNS3 and EVE-NG](https://github.com/hegdepavankumar/Cisco-Images-for-GNS3-and-EVE-NG)
- [GNS3 Vault](https://gns3vault.com/)
- [NetworkLessons.com](https://networklessons.com/cisco/gns3)

### Certification Resources
- [Cisco Certification Tracking System](https://www.cisco.com/c/en/us/training-events/training-certifications/certifications.html)
- [CCNA Study Materials](https://learningnetwork.cisco.com/s/ccna)
- [Network Lessons Free Labs](https://networklessons.com/cisco/gns3-labs)

### Network Simulation Alternatives
- [EVE-NG](https://www.eve-ng.net/)
- [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer)
- [Cisco VIRL/CML](https://developer.cisco.com/modeling-labs/)
- [Mininet](http://mininet.org/)

### Learning Platforms
- [Cisco Networking Academy](https://www.netacad.com/)
- [CBT Nuggets](https://www.cbtnuggets.com/)
- [INE Training](https://ine.com/)
- [Linux Academy](https://linuxacademy.com/)

### Community Forums
- [Cisco Community](https://community.cisco.com/)
- [Reddit r/Cisco](https://www.reddit.com/r/Cisco/)
- [Reddit r/networking](https://www.reddit.com/r/networking/)
- [GNS3 Community Forum](https://gns3.com/community)

## 📞 Support

### Getting Help
- **Issues**: Report problems via GitHub Issues
- **Discussions**: Use GitHub Discussions for questions
- **Email**: Contact repository maintainer for urgent matters
- **Community**: Join GNS3 community forums for peer support

### Reporting Issues
When reporting issues, please include:
- GNS3 version
- Operating system details
- Image filename and version
- Error messages or screenshots
- Steps to reproduce the problem

### Feature Requests
Submit feature requests with:
- Clear description of requested feature
- Use case explanation
- Potential implementation approach
- Priority level

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **GNS3 Team**: For developing the excellent network simulation platform
- **Cisco Systems**: For providing comprehensive networking solutions
- **Community Contributors**: For sharing knowledge and resources
- **Educational Institutions**: For promoting network education

---

**⚠️ Remember**: Always ensure you have proper licensing and permissions before using any Cisco IOS images in your environment. This repository is designed to support learning and education in network technologies.

**📧 Contact**: For questions or collaboration opportunities, please reach out through GitHub issues or discussions.
