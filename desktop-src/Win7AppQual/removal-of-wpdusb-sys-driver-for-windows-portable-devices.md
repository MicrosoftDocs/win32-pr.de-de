---
description: Entfernen des WPDUSB.SYS-Treibers für portable Windows-Geräte
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Entfernen des WPDUSB.SYS-Treibers für portable Windows-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116248"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Entfernen des WPDUSB.SYS-Treibers für portable Windows-Geräte

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Niedrig  





## <a name="description"></a>BESCHREIBUNG

Microsoft hat die Kernelmoduskomponente des Windows Vista-USB-Treiberstapels (WPDUSB.SYS) für Windows Portable Devices (WPD) durch den generischen WINUSB.SYS ersetzt. Die Kommunikation mit dem ursprünglichen WPDUSB.SYS-Treiber erfolgt über private I/O-Steuerungscodes (IOCTL). Die Unterstützung dieser wurde ebenfalls entfernt.

Jeder Consumer dieser IOCTL-Codes wäre für die ordnungsgemäße Interpretation und Implementierung des Media Transfer Protocol (MTP) verantwortlich gewesen. Windows Vista hat die Verwendung dieser IOCTL-Codes durch Drittanbieteranwendungen nicht unterstützt.

## <a name="manifestation-of-impact"></a>Auswirkungen

Jede Anwendung, die von der Verfügbarkeit dieser privaten IOCTL-Codes abhängig ist, hat keinen Zugriff mehr auf mit USB verbundene MTP-Geräte.

## <a name="mitigation"></a>Minderung

Benutzer einer Anwendung, die von den privaten IOCTL-Codes abhängig ist, müssen eine andere Anwendung (oder eine aktualisierte Version der Anwendung) verwenden, um auf das mit USB verbundene MTP-Gerät zu zugreifen.

## <a name="solution"></a>Lösung

Anwendungen sollten die WPD-API (Windows Portable Devices) verwenden, um wpd-Geräte zu suchen und mit ihnen zu interagieren. Obwohl ein signifikanter Prozentsatz der WPD-Geräte MTP für die Kommunikation mit dem PC implementiert, ist WPD nicht nur auf MTP-Geräte beschränkt. Wenn der direkte Zugriff auf das Gerät über die privaten IOCTLs die Anwendung auf die Kommunikation mit geräten mit USB-Verbindung beschränkt hätte, erweitert die Verwendung der WPD-API die Liste der Konnektivitätsoptionen auf andere Kommunikationsprotokolle (z. B. WLAN). In den seltenen Fällen, in denen die Anwendung MTP-bewusst sein muss, stellt die WPD-API einen Pass-Through-Mechanismus für unformatierte MTP-Befehle bereit.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Die WPD-API wird in Windows XP (über das Windows Format SDK), Windows Vista und Windows 7 unterstützt. Die Windows 7-Implementierung von WPD fügt Unterstützung für MTP über Bluetooth hinzu.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

[Portable Windows-Geräte](../windows-portable-devices.md)

 

 
