---
title: Windows Clientfunktionen der Bereitstellungsdienste
description: Die folgenden Funktionen werden mit der Client-API Windows Bereitstellungsdienste verwendet.
ms.assetid: 4cedd8a8-7f46-4229-9d96-58965b751e43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c213822323405e030ba9907f692d6fcaa370356fb395a390dfa0f1fc0818244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566385"
---
# <a name="windows-deployment-services-client-functions"></a>Windows Clientfunktionen der Bereitstellungsdienste

Die folgenden Funktionen werden mit der Client-API Windows Bereitstellungsdienste verwendet.



| Funktion                                                                                 | Beschreibung                                                                                                                            |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsCliCallback*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclicallback)                                          | Statusbenachrichtigung und Fehlermeldungen während einer Datei- oder Bildübertragung.                                                              |
| [*PFN \_ WdsCliTraceFunction*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclitracefunction)                                | Empfängt Debugmeldungen vom WDS-Client.                                                                                       |
| [**WdsCliAuthorizeSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession)                                 | Konvertiert eine anonyme Sitzung in eine authentifizierte Sitzung.                                                                           |
| [**WdsCliCancelTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicanceltransfer)                                     | Bricht einen WDS-Übertragungsvorgang ab.                                                                                                      |
| [**WdsCliClose**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)                                                       | Schließt ein Handle für eine WDS-Sitzung oder ein WDS-Image und gibt Ressourcen frei.                                                                      |
| [**WdsCliCreateSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)                                       | Startet eine neue Sitzung mit einem WDS-Server.                                                                                                |
| [**WdsCliFindFirstImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage)                                     | Startet die Enumeration von Images, die auf einem WDS-Server gespeichert sind, und gibt ein Find-Handle zurück, das auf das erste Image verweist.                     |
| [**WdsCliFindNextImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage)                                       | Überlädt den Verweis eines Find-Handles auf das nächste Image, das auf einem WDS-Server gespeichert ist.                                                      |
| [**WdsCliFreeStringArray**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifreestringarray)                                   | Gibt das Array von Zeichenfolgenwerten frei, die von der [**WdsCliObtainDriverPackages-Funktion zugeordnet**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages) werden. |
| [**WdsCliGetEnumerationFlags**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags)                           | Gibt das Bildenumerationsflag für das aktuelle Bildhand handle zurück.                                                                       |
| [**WdsCliGetImageArchitecture**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture)                         | Gibt die Prozessorarchitektur für das aktuelle Image zurück.                                                                              |
| [**WdsCliGetImageDescription**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription)                           | Gibt die Beschreibung des aktuellen Bilds zurück.                                                                                          |
| [**WdsCliGetImageGroup**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup)                                       | Gibt den Namen der Bildgruppe für das aktuelle Bild zurück.                                                                                    |
| [**WdsCliGetImageHalName**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname)                                   | Gibt den Namen der Hardwareabstraktionsschicht (Hardware Abstraction Layer, HALOGEN) für das aktuelle Image zurück.                                                               |
| [**WdsCliGetImageHandleFromFindHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromfindhandle)         | Gibt ein Bildhand handle für das aktuelle Bild zurück.                                                                                         |
| [**WdsCliGetImageHandleFromTransferHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromtransferhandle) | Gibt ein Bildhand handle aus einem abgeschlossenen Übertragungshand handle zurück.                                                                              |
| [**WdsCliGetImageIndex**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex)                                       | Gibt den Bildindex für das aktuelle Bild zurück.                                                                                         |
| [**WdsCliGetImageLanguage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage)                                 | Gibt die Standardsprache des aktuellen Bilds zurück.                                                                                     |
| [**WdsCliGetImageLanguages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages)                               | Gibt ein Array von Sprachen zurück, die vom aktuellen Bild unterstützt werden.                                                                          |
| [**WdsCliGetImageLastModifiedTime**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime)                 | Gibt den Zeitpunkt der letzten Änderung für das aktuelle Bild zurück.                                                                                  |
| [**WdsCliGetImageName**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename)                                         | Gibt den Namen des aktuellen Bilds zurück.                                                                                                 |
| [**WdsCliGetImageNamespace**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagenamespace)                               | Gibt den Namen des aktuellen Bilds zurück.                                                                                                 |
| [**WdsCliGetImagePath**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath)                                         | Gibt den Pfad zur Bilddatei zurück, die das aktuelle Bild enthält.                                                                    |
| [**WdsCliGetImageSize**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize)                                         | Gibt die Größe des aktuellen Bilds zurück.                                                                                                 |
| [**WdsCliGetImageVersion**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion)                                   | Gibt die Version des aktuellen Images zurück.                                                                                              |
| [**WdsCliGetTransferSize**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligettransfersize)                                   | Gibt die Größe der aktuellen Übertragung zurück.                                                                                              |
| [**WdsCliInitializeLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog)                                       | Initialisiert das Protokoll für den Client.                                                                                                    |
| [**WdsCliLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclilog)                                                           | Sendet ein Protokollereignis an den WDS-Server.                                                                                                   |
| [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages)                         | Erhält von einem WDS-Image die Treiberpakete (INF-Dateien), die auf diesem Computer verwendet werden können.                                           |
| [**WdsCliRegisterTrace**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliregistertrace)                                       | Registriert eine Rückruffunktion, die Debugmeldungen erhält.                                                                    |
| [**WdsCliTransferFile**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferfile)                                         | Überträgt eine Datei mithilfe eines Multicastübertragungsprotokolls von einem WDS-Server an den WDS-Client.                                              |
| [**WdsCliTransferImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferimage)                                       | Überträgt ein Image von einem WDS-Server.                                                                                                  |
| [**WdsCliWaitForTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliwaitfortransfer)                                   | Wartet auf den Abschluss einer Übertragung.                                                                                                      |



 



| Funktion                                                             | Beschreibung                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WdsCliGetDriverQueryXml**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetdriverqueryxml)           | Generiert eine XML-Zeichenfolge, die zum Abfragen eines WDS-Servers nach Treiberpaketen verwendet werden kann. Verfügbar ab Windows 8 und Windows Server 2012.               |
| [**WdsCliObtainDriverPackagesEx**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackagesex) | Erhält die Treiberpakete (INF-Dateien), die auf die angegebene WDS-Treiberabfrage-XML anwendbar sind. Verfügbar ab Windows 8 und Windows Server 2012. |



 

 

 




