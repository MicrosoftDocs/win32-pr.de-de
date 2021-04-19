---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Entfernen von WPDUSB.SYS Treiber für tragbare Windows-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362919"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Entfernen von WPDUSB.SYS Treiber für tragbare Windows-Geräte

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Microsoft hat die Kernelmoduskomponente des Windows Vista-USB-Treiber Stapels (WPDUSB.SYS) für Windows Portable Devices (WPD) mit dem generischen WINUSB.SYS-Treiber ersetzt. Die Kommunikation mit dem ursprünglichen WPDUSB.SYS Treiber erfolgte über private e/a-Steuerungs Codes (IOCTL). Diese Unterstützung wurde ebenfalls entfernt.

Jeder Consumer dieser ioctl-Codes wäre für die ordnungsgemäße Interpretation und Implementierung von MTP (Media Transfer Protocol) verantwortlich. Die Verwendung dieser ioctl-Codes durch Drittanbieter Anwendungen wurde von Windows Vista nicht unterstützt.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Alle Anwendungen, die von der Verfügbarkeit dieser privaten ioctl-Codes abhängen, haben keinen Zugriff mehr auf USB-verbundene MTP-Geräte.

## <a name="mitigation"></a>Minderung

Benutzer einer Anwendung, die von den privaten ioctl-Codes abhängig ist, müssen eine andere Anwendung (oder eine aktualisierte Version der Anwendung) verwenden, um auf das USB-verbundene MTP-Gerät zuzugreifen.

## <a name="solution"></a>Lösung

Anwendungen sollten mithilfe der WPD-API (Portable Devices) von Windows beliebige WPD-Geräte suchen und mit ihnen interagieren. Obwohl ein erheblicher Prozentsatz von WPD-Geräten MTP für die Kommunikation mit dem PC implementiert, ist WPD nicht auf MTP-Geräte beschränkt. Darüber hinaus erweitert der direkte Zugriff auf das Gerät über die private IOCTLs die Anwendung auf die Kommunikation mit nur USB-Geräten, die mithilfe der WPD-API die Liste der Konnektivitätsoptionen auf andere Kommunikationsprotokolle (z. b. Wi-Fi) erweitert. In den seltenen Fällen, in denen die Anwendung MTP-fähig sein muss, stellt die WPD-API einen Pass-Through-Mechanismus für unformatierte MTP-Befehle bereit.

## <a name="leveraging-feature-capabilities"></a>Nutzen von Featurefunktionen

Die WPD-API wird in Windows XP (über das Windows-Format-SDK), Windows Vista und Windows 7 unterstützt. Die Windows 7-Implementierung von WPD bietet Unterstützung für MTP über Bluetooth.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

[Tragbare Windows-Geräte](../windows-portable-devices.md)

 

 
