---
title: Windows Defender Funktionen
description: Funktionen, die von Apps aufgerufen werden, um Überprüfungen, Signaturupdates oder Informationen von Windows Defender anzufordern.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ecfa00a38c2263fe1db1b996bb3ec052f8caef1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483126"
---
# <a name="windows-defender-functions"></a>Windows Defender Funktionen

Funktionen, die von Apps aufgerufen werden, um Überprüfungen, Signaturupdates oder Informationen von Windows Defender anzufordern.




| Funktion | BESCHREIBUNG | 
|----------|-------------|
| <a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a> | Gibt eine formatierte Fehlermeldung basierend auf einem Fehlercode zurück.<br /> | 
| <a href="mpfreememory.md"><strong>MpFreeMemory</strong></a> | Gibt Arbeitsspeicher für den Malwareschutz-Manager frei.<br /> | 
| <a href="mphandleclose.md"><strong>MpHandleClose</strong></a> | Schließt das von <a href="mpmanageropen.md"><strong>MpManagerOpen,</strong></a> <a href="mpscanstart.md"><strong>MpScanStart,</strong></a> <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>oder <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>zurückgegebene Handle.<br /> | 
| <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a> | Stellt eine Verbindung mit dem Malwareschutz-Manager auf dem lokalen Computer her.<br /> | 
| <a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a> | <strong>Nicht unterstützt.</strong> Gibt Statusinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück.<br /> | 
| <a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a> | Gibt Statusinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück.<br /> | 
| <a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a> | Gibt Versionsinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück.<br /> | 
| <a href="mpscancontrol.md"><strong>MpScanControl</strong></a> | Ermöglicht die Steuerung eines Scans, der asynchron über <a href="mpscanstart.md"><strong>MpScanStart</strong></a>initiiert wurde.<br /> | 
| <a href="mpscanstart.md"><strong>MpScanStart</strong></a> | Startet einen Überprüfungsvorgang.<br /> | 
| <a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a> | Gibt Informationen zur nächsten Bedrohung in der Enumerationsliste zurück. Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen abgeschlossen ist.<br /> | 
| <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a> | Gibt ein Enumerationshandle zum Abrufen von Bedrohungen zurück. Diese Funktion kann verwendet werden, um Bedrohungen zu öffnen, die von einem bestimmten Scan erkannt werden, alle aktiven Bedrohungen im System, den Verlauf der Bedrohungsbedrohung oder alle Bedrohungen, die in der Signaturdatenbank vorhanden sind.<br /> | 
| <a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a> | Wird verwendet, um statische Informationen (z. B. Schweregrad und Kategorie) oder lokalisierte Informationen (z. B. Kategoriebeschreibung und Empfehlungen) zu einer bestimmten Bedrohung abzufragen.<br /> | 
| <a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a> | Ermöglicht die Steuerung eines Signaturaktualisierungsvorgangs, der asynchron über <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>initiiert wurde.<br /> | 
| <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a> | Startet einen Signaturaktualisierungsvorgang.<br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> | Ändert Windows Defender Status in Ein oder Aus.<br /><blockquote>[!Note]<br />Ab Windows 10 Version 1607 und Windows Server 2016 gibt die <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable-Funktion</strong></a> immer <strong>E_NOTIMPL</strong>zurück.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a> | Gibt den aktuellen Status von Windows Defender zurück.<br /> | 




 

 

 





