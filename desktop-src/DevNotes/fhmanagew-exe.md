---
description: Das FhManagew.exe Programm löscht Dateiversionen, die ein bestimmtes Alter überschreiten, aus dem momentan zugewiesenen Datei Versionsverlauf-Zielgerät.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483243"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

Das FhManagew.exe Programm löscht Dateiversionen, die ein bestimmtes Alter überschreiten, aus dem momentan zugewiesenen Datei Versionsverlauf-Zielgerät.

Dieses Programm ist in Windows 8 und Windows Server 2012 und höher verfügbar.

Wechseln Sie zum Ausführen dieses Programms zum **Startmenü** , klicken Sie auf **Ausführen**, und geben Sie den folgenden Befehl ein.

**FhManagew.exe Bereinigungs** *Alter*



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="age"></span><span id="AGE"></span><em>Eder</em><br/></td>
<td>Dieser Parameter gibt das minimale Alter (in Tagen) von Dateiversionen an, die gelöscht werden können. Eine Dateiversion wird gelöscht, wenn beide der folgenden Bedingungen zutreffen:<br/>
<ul>
<li>Die Dateiversion ist älter als das angegebene Alter.</li>
<li>Die Datei ist nicht mehr im Schutzbereich enthalten, oder es gibt eine neuere Version derselben Datei auf dem Zielgerät.</li>
</ul>
Wenn der <em>Age</em> -Parameter auf 0 (null) festgelegt ist, werden alle Dateiversionen gelöscht, mit Ausnahme der neuesten Version der einzelnen Dateien, die derzeit im Schutzbereich vorhanden sind.<br/></td>
</tr>
</tbody>
</table>



 

Um die gesamte Ausgabe dieses Programms zu unterdrücken, verwenden Sie die **-quiet-** Befehlszeilenoption wie folgt.

**FhManagew.exe-Cleanup** *Age* **-quiet**

## <a name="examples"></a>Beispiele



| Beispiel                                                                                                                                                                                                      | BESCHREIBUNG                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-Bereinigung 30**<br/>                                 | Löschen Sie alle Dateiversionen, die älter als ein Monat sind.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Bereinigung 365-quiet**<br/> | Löschen Sie alle Dateiversionen, die älter als ein Jahr sind, und unterdrücken Sie die gesamte Ausgabe.<br/> |



 

 

 




