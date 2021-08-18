---
description: Entfernen des WPDUSB.SYS-Treibers für Windows portable Geräte
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Entfernen des WPDUSB.SYS-Treibers für Windows portable Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b5d1a815b97049816a618b9e93d0767e321fd60b689e6845318c1605574c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994740"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Entfernen des WPDUSB.SYS-Treibers für Windows portable Geräte

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>BESCHREIBUNG

Microsoft hat die Kernelmoduskomponente des USB-Treiberstapels Windows Vista (WPDUSB.SYS) für Windows Portable Devices (WPD) durch den generischen WINUSB.SYS-Treiber ersetzt. Die Kommunikation mit dem ursprünglichen WPDUSB.SYS-Treiber erfolgte über IOCTL-Codes (Private E/A Control). Die Unterstützung dieser wurde ebenfalls entfernt.

Jeder Consumer dieser IOCTL-Codes wäre für die ordnungsgemäße Interpretation und Implementierung des Media Transfer Protocol (MTP) verantwortlich gewesen. Windows Vista hat die Verwendung dieser IOCTL-Codes durch Drittanbieteranwendungen nicht unterstützt.

## <a name="manifestation-of-impact"></a>Auswirkungen

Jede Anwendung, die von der Verfügbarkeit dieser privaten IOCTL-Codes abhängig war, hätte keinen Zugriff mehr auf MIT USB verbundene MTP-Geräte.

## <a name="mitigation"></a>Minderung

Benutzer einer Anwendung, die von den privaten IOCTL-Codes abhängig ist, müssen eine andere Anwendung (oder eine aktualisierte Version der Anwendung) verwenden, um auf das MIT USB verbundene MTP-Gerät zuzugreifen.

## <a name="solution"></a>Lösung

Anwendungen sollten die APD-API (Windows Portable Devices) verwenden, um wpd-Geräte zu suchen und mit ihnen zu interagieren. Obwohl ein erheblicher Prozentsatz der WPD-Geräte MTP für die Kommunikation mit dem PC implementiert, ist WPD nicht auf MTP-Geräte beschränkt. Darüber hinaus wird durch die Verwendung der WPD-API die Liste der Konnektivitätsoptionen auf andere Kommunikationsprotokolle (z. B. WLAN) erweitert, wenn der direkte Zugriff auf das Gerät über die privaten IOCTLs die Anwendung auf die Kommunikation mit geräten beschränkt hätte, die mit USB verbunden sind. In den seltenen Fällen, in dem die Anwendung MTP-fähigen Muss, stellt die WPD-API einen Pass-Through-Mechanismus für unformatierte MTP-Befehle bereit.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Die WPD-API wird in Windows XP (über das Windows Format SDK), Windows Vista und Windows 7 unterstützt. Die Windows 7-Implementierung von WPD fügt Unterstützung für MTP über Bluetooth hinzu.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

[Windows Portable Geräte](../windows-portable-devices.md)

 

 
