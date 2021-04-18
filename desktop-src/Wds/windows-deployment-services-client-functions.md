---
title: Client Funktionen der Windows-Bereitstellungs Dienste
description: Die folgenden Funktionen werden mit der Client-API der Windows-Bereitstellungs Dienste verwendet.
ms.assetid: 4cedd8a8-7f46-4229-9d96-58965b751e43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe124c6f02d12943d40fbc98af4a687d5b892f86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337183"
---
# <a name="windows-deployment-services-client-functions"></a>Client Funktionen der Windows-Bereitstellungs Dienste

Die folgenden Funktionen werden mit der Client-API der Windows-Bereitstellungs Dienste verwendet.



| Funktion                                                                                 | BESCHREIBUNG                                                                                                                            |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ wdsclicallback*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclicallback)                                          | Fortschritts Benachrichtigung und Fehlermeldungen während einer Datei-oder Bildübertragung.                                                              |
| [*PFN \_ wdsclitracefunction*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclitracefunction)                                | Empfängt Debugmeldungen vom WDS-Client.                                                                                       |
| [**Wdscliauthorizesession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession)                                 | Konvertiert eine anonyme Sitzung in eine authentifizierte Sitzung.                                                                           |
| [**Wdsclicanceltransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicanceltransfer)                                     | Bricht einen WDS-Übertragungsvorgang ab.                                                                                                      |
| [**Wdscliclose**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)                                                       | Schließt ein Handle für eine WDS-Sitzung oder ein Image und gibt Ressourcen frei.                                                                      |
| [**Wdsclikreatesession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)                                       | Startet eine neue Sitzung mit einem WDS-Server.                                                                                                |
| [**Wdsclifindfirstimage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage)                                     | Startet die Enumeration von Bildern, die auf einem WDS-Server gespeichert sind, und gibt ein Find-Handle zurück, das auf das erste Bild verweist.                     |
| [**Wdsclifindnextimage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage)                                       | Verschiebt den Verweis eines Find-Handles auf das nächste Bild, das auf einem WDS-Server gespeichert ist.                                                      |
| [**Wdsclifrestringarray**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifreestringarray)                                   | Gibt das Array von Zeichen folgen Werten frei, das von der [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages) -Funktion zugewiesen wird. |
| [**Wdscligetenreerationflags**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags)                           | Gibt das abbildrenumerationsflag für das aktuelle Bild Handle zurück.                                                                       |
| [**Wdscligetimagetimagearchitektur**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture)                         | Gibt die Prozessorarchitektur für das aktuelle Bild zurück.                                                                              |
| [**Wdscligetimagedescription**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription)                           | Gibt die Beschreibung des aktuellen Bilds zurück.                                                                                          |
| [**Wdscligetimagegroup**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup)                                       | Gibt den Namen der Bild Gruppe für das aktuelle Bild zurück.                                                                                    |
| [**Wdscligetimagehalname**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname)                                   | Gibt den HAL-Namen (Hardware Abstraktion Layer) für das aktuelle Bild zurück.                                                               |
| [**Wdscligetimagelenker fromfindhandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromfindhandle)         | Gibt ein Bild Handle für das aktuelle Bild zurück.                                                                                         |
| [**Wdscligetimagepper fromtransferhandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromtransferhandle) | Gibt ein Bild Handle von einem abgeschlossenen Übertragungs Handle zurück.                                                                              |
| [**Wdscligetimageindex**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex)                                       | Gibt den Bildindex für das aktuelle Bild zurück.                                                                                         |
| [**Wdscligetimagelanguage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage)                                 | Gibt die Standardsprache des aktuellen Bilds zurück.                                                                                     |
| [**Wdscligetimagelanguages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages)                               | Gibt ein Array von Sprachen zurück, die vom aktuellen Bild unterstützt werden.                                                                          |
| [**Wdscligetimagelastmodifiedtime**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime)                 | Gibt die Uhrzeit der letzten Änderung für das aktuelle Bild zurück.                                                                                  |
| [**Wdscligetimagename**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename)                                         | Gibt den Namen des aktuellen Bilds zurück.                                                                                                 |
| [**Wdscligetimagenamespace**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagenamespace)                               | Gibt den Namen des aktuellen Bilds zurück.                                                                                                 |
| [**Wdscligetimagepfad**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath)                                         | Gibt den Pfad zur Bilddatei zurück, die das aktuelle Bild enthält.                                                                    |
| [**Wdscligetimagetimagesize**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize)                                         | Gibt die Größe des aktuellen Bilds zurück.                                                                                                 |
| [**Wdscligetimageversion**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion)                                   | Gibt die Version des aktuellen Bilds zurück.                                                                                              |
| [**Wdscligettransfersize**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligettransfersize)                                   | Gibt die Größe der aktuellen Übertragung zurück.                                                                                              |
| [**Wdscliinitializelog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog)                                       | Initialisiert das Protokoll für den Client.                                                                                                    |
| [**Wdsclilog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclilog)                                                           | Sendet ein Protokoll Ereignis an den WDS-Server.                                                                                                   |
| [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages)                         | Ruft aus einem WDS-Image, den Treiber Paketen (INF-Dateien) ab, die auf diesem Computer verwendet werden können.                                           |
| [**Wdscliregistertrace**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliregistertrace)                                       | Registriert eine Rückruffunktion, die Debugmeldungen empfängt.                                                                    |
| [**Wdsclitransferfile**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferfile)                                         | Überträgt eine Datei von einem WDS-Server mithilfe eines Multicast Übertragungsprotokolls auf den WDS-Client.                                              |
| [**Wdsclitransferimage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferimage)                                       | Überträgt ein Abbild von einem WDS-Server.                                                                                                  |
| [**Wdscliwaitfortransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliwaitfortransfer)                                   | Wartet auf den Abschluss einer Übertragung.                                                                                                      |



 



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wdscligetdriverqueryxml**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetdriverqueryxml)           | Generiert eine XML-Zeichenfolge, die verwendet werden kann, um einen WDS-Server nach Treiber Paketen abzufragen. Verfügbar ab Windows 8 und Windows Server 2012.               |
| [**WdsCliObtainDriverPackagesEx**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackagesex) | Ruft die Treiber Pakete (INF-Dateien) ab, die für den angegebenen XML-Code der WDS-Treiber Abfrage anwendbar sind. Verfügbar ab Windows 8 und Windows Server 2012. |



 

 

 




