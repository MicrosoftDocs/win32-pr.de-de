---
description: Die uikreatepatchpackage-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) an und generiert ein Windows Installer Patchpaket (MSP-Paket).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: Uikreatepatchpackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861900"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>Uikreatepatchpackage (Patchwiz.dll)

Die uikreatepatchpackage-Funktion nimmt eine Paket Erstellungs Datei (PCP-Datei) an und generiert ein Windows Installer Patchpaket (MSP-Paket). Das Aufrufen von [Msimsp.exe](msimsp-exe.md) ist die empfohlene Methode für die Verwendung von [Patchwiz.dll](patchwiz-dll.md). Die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion ist in Version 4,0 von Patchwiz.dll verfügbar und erweitert die Funktionalität der uikreatepatchpackage-Funktion.

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
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

Speicherort für temporäre Dateien. Dieser Parameter kann **null** oder eine leere Zeichenfolge sein, wird jedoch möglicherweise nicht ausgelassen. Der Standard Speicherort ist% tmp% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fremuvetempfoldercontents*
</dt> <dd>

Wenn **true**, entfernen Sie den temporären Ordner und seinen gesamten Inhalt, falls vorhanden. Wenn **false** und der Ordner vorhanden ist, schlägt die Funktion fehl.

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen finden Sie in der Tabelle unter [Rückgabewerte für uikreatepatchpackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Bemerkungen

Ein Beispiel für das Erstellen einer PCP-Datei und die Verwendung von uikreatepatchpackage zum Generieren eines Windows Installer Patchpakets finden Sie im Abschnitt [ein Beispiel für ein kleines Update Patching](a-small-update-patching-example.md).

Zum Erstellen eines Patches ist ein nicht komprimiertes Setup Image erforderlich, z. b. ein administratives Image oder ein nicht komprimiertes Setup-Image von einer CD-ROM. Uikreatepatchpackage generiert keine binären Patches für Dateien in den CAB-Dateien.

 

 



