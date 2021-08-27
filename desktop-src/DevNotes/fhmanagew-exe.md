---
description: Das FhManagew.exe Programm löscht Dateiversionen, die ein angegebenes Alter überschreiten, vom derzeit zugewiesenen Dateiversionsverlauf Zielgerät.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2570da9b2b874b723b28917028fab3c58ecdf772
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481516"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

Das FhManagew.exe Programm löscht Dateiversionen, die ein angegebenes Alter überschreiten, vom derzeit zugewiesenen Dateiversionsverlauf Zielgerät.

Dieses Programm ist in Windows 8 und Windows Server 2012 und höher verfügbar.

Um dieses Programm auszuführen, wechseln Sie zum **Startmenü,** klicken Sie auf **Ausführen**, und geben Sie den folgenden Befehl ein.

**FhManagew.exe -cleanup** *age*




| Parameter | BESCHREIBUNG | 
|-----------|-------------|
| <span id="age"></span><span id="AGE"></span><em>Alter</em><br /> | Dieser Parameter gibt das Mindestalter von Dateiversionen in Tagen an, die gelöscht werden können. Eine Dateiversion wird gelöscht, wenn beide der folgenden Bedingungen zutreffen:<br /><ul><li>Die Dateiversion ist älter als das angegebene Alter.</li><li>Die Datei ist nicht mehr im Schutzbereich enthalten, oder es gibt eine neuere Version derselben Datei auf dem Zielgerät.</li></ul>Wenn der <em>age-Parameter</em> auf 0 (null) festgelegt ist, werden alle Dateiversionen gelöscht, mit Ausnahme der neuesten Version jeder Datei, die derzeit im Schutzbereich vorhanden ist.<br /> | 




 

Um die gesamte Ausgabe dieses Programms zu unterdrücken, verwenden Sie die Befehlszeilenoption **-quiet** wie folgt.

**FhManagew.exe -cleanup** *age* **-quiet**

## <a name="examples"></a>Beispiele



| Beispiel                                                                                                                                                                                                      | BESCHREIBUNG                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**<br/>                                 | Löschen Sie alle Dateiversionen, die älter als einen Monat sind.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**<br/> | Löschen Sie alle Dateiversionen, die älter als ein Jahr sind, und unterdrücken Sie die gesamte Ausgabe.<br/> |



 

 

 




