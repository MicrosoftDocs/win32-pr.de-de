---
description: Die UiCreatePatchPackage-Funktion verwendet eine Paketerstellungsdatei (PCP-Datei) und generiert ein Windows Installer-Patchpaket (MSP-Paket).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2802eb92d9df42a683053198ab14bbe7894fa512c63f25e1cd4afe060ea74c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810500"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>UiCreatePatchPackage (Patchwiz.dll)

Die UiCreatePatchPackage-Funktion verwendet eine Paketerstellungsdatei (PCP-Datei) und generiert ein Windows Installer-Patchpaket (MSP-Paket). Das Aufrufen [ vonMsimsp.exe](msimsp-exe.md) ist die empfohlene Methode für die Verwendung [ vonPatchwiz.dll](patchwiz-dll.md). Die [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) ist in Version 4.0 von Patchwiz.dll verfügbar und erweitert die Funktionalität der UiCreatePatchPackage-Funktion.

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

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

Vollständiger Pfad zur Patcherstellungs-Eigenschaftendatei (PCP-Datei) für diesen Patch.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

Vollständiger Pfad zum Windows Installer-Patchpaket (MSP-Datei), das erstellt werden soll. Dieser Parameter kann **NULL** oder eine leere Zeichenfolge sein, aber nicht ausgelassen werden. Wenn sie **NULL** oder eine leere Zeichenfolge ist, verwendet die Funktion den Wert von PatchOutputPath in der [Eigenschaftentabelle (Patchwiz.dll).](properties-table-patchwiz-dll-.md)

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

Vollständiger Pfad zu einer Textdatei, die angefügt wird. Dieser Parameter kann **NULL** oder eine leere Zeichenfolge sein, aber nicht ausgelassen werden.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

Handle für ein Fenster, in dem der Statustext angezeigt wird. Dieser Parameter kann **NULL** oder eine leere Zeichenfolge sein, aber nicht ausgelassen werden.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

Speicherort für temporäre Dateien. Dieser Parameter kann **NULL** oder eine leere Zeichenfolge sein, aber nicht ausgelassen werden. Der Standardspeicherort ist %TMP% \\ ~pcw \_ tmp.tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Wenn **TRUE,** entfernen Sie den temporären Ordner und den gesamten Inhalt, sofern vorhanden. Wenn **FALSE** und der Ordner vorhanden sind, schlägt die Funktion fehl.

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen finden Sie in der Tabelle [unter Rückgabewerte für UiCreatePatchPackage.](return-values-for-uicreatepatchpackage.md)

## <a name="remarks"></a>Hinweise

Ein Beispiel für die Erstellung einer PCP-Datei und die Verwendung von UiCreatePatchPackage zum Generieren eines Windows Installer-Patchpakets finden Sie im Abschnitt [A Small Update Patching Example](a-small-update-patching-example.md).

Zum Erstellen eines Patches ist ein nicht komprimiertes Setupimage erforderlich, z. B. ein Administratives Image oder ein nicht komprimiertes Setupimage von einer CD-ROM. UiCreatePatchPackage generiert keine binären Patches für Dateien in Schränken.

 

 



