---
description: Die uikreatepatchpackageex-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) und generiert ein Windows Installer Patchpaket (MSP-Paket). Das Aufrufen von Msimsp.exe ist die empfohlene Methode für die Verwendung von Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: Uikreatepatchpackageex (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341168"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a>Uikreatepatchpackageex (Patchwiz.dll)

Die uikreatepatchpackageex-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) und generiert ein Windows Installer Patchpaket (MSP-Paket). Das Aufrufen von [Msimsp.exe](msimsp-exe.md) ist die empfohlene Methode für die Verwendung von [Patchwiz.dll](patchwiz-dll.md).

Die uikreatepatchpackageex-Funktion ist ab Patchwiz.dll Version 4,0 verfügbar und erweitert die Funktionalität der [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) -Funktion.

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szpcppath*
</dt> <dd>

Vollständiger Pfad zur Eigenschaften Datei für die Patcherstellung (PCP-Datei) für diesen Patch.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szpatchpfad*
</dt> <dd>

Vollständiger Pfad zum Windows Installer Patchpaket (MSP-Datei), das erstellt werden soll. Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen. Wenn Sie **null** oder eine leere Zeichenfolge ist, verwendet die Funktion den Wert von "patchoutputpath" in der [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md).

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szlogpath*
</dt> <dd>

Vollständiger Pfad zu einer Text Protokolldatei, die angefügt wird. Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndstatus*
</dt> <dd>

Handle für ein Fenster, in dem der Status Text angezeigt wird. Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*sztempfolder*
</dt> <dd>

Speicherort für temporäre Dateien. Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen. Der Benutzer muss über ausreichende Berechtigungen zum Lesen und Schreiben in diesen Ordner verfügen. Der Standard Speicherort ist% tmp% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fremuvetempfoldercontents*
</dt> <dd>

Wenn **true**, entfernen Sie den temporären Ordner und seinen gesamten Inhalt, falls vorhanden. Wenn **false** und der Ordner vorhanden ist, schlägt die Funktion fehl.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Dieser Parameter kann auf eine oder eine Kombination der folgenden Werte festgelegt werden, um Protokollierungs-oder Benutzeroberflächen Optionen anzugeben.



| Flag            | Wert       | Bedeutung                                  |
|-----------------|-------------|------------------------------------------|
| Lognone         | 0x00000000  | Schreiben Sie keine Nachrichten in das Protokoll.            |
| LOGINFO         | 0x00000001  | Schreiben Sie Informationsmeldungen in das Protokoll. |
| Logwarn         | 0x00000002  | Schreiben Sie Warnungen in das Protokoll.               |
| Logerr          | 0x00000004  | Schreiben Sie Fehlermeldungen in das Protokoll.         |
| Logperfmessages | 0x00000008  | Schreiben Sie Leistungs Meldungen in das Protokoll.   |
| Uinone          | 0x00000000f | Die Benutzeroberfläche wird nicht angezeigt.       |
| Uiall           | 0x00000010  | Zeigen Sie die Benutzeroberfläche an.              |



 

</dd> <dt>

<span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*
</dt> <dd>

Reserviert. Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen finden Sie in der Tabelle unter [Rückgabewerte für uikreatepatchpackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Bemerkungen

Ein Beispiel für das Erstellen einer PCP-Datei und die Verwendung von [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) zum Generieren eines Windows Installer Patchpakets finden Sie im Abschnitt [ein Beispiel für ein kleines Update Patching](a-small-update-patching-example.md).

Zum Erstellen eines Patches ist ein nicht komprimiertes Setup Image erforderlich, z. b. ein administratives Image oder ein nicht komprimiertes Setup-Image von einer CD-ROM. [Uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) generiert keine binären Patches für Dateien in den CAB-Dateien.

 

 



