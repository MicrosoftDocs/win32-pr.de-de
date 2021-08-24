---
description: ICE40 führt verschiedene Überprüfungen durch.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077c44154413d9aa9e75b1c13fe2f2f80ccb52fee6459888c7bc9678ea0e935f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528430"
---
# <a name="ice40"></a>ICE40

ICE40 führt verschiedene Überprüfungen durch.

## <a name="result"></a>Ergebnis

ICE40 gibt Warnungen zu folgenden Themen aus:

-   Die [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) wurde überschrieben.
-   Die [RemoveIniFile-Tabelle](removeinifile-table.md) verfügt über den Eintrag Tag löschen ohne Wert.
-   In .msi Datei fehlt die [Tabelle Fehler,](error-table.md) und [**die**](page-count-summary.md) Eigenschaft Zusammenfassung der Seitenanzahl ist kleiner oder gleich 100. Diese ICE-Warnung ist veraltet, Windows Installer keine Fehlertabelle für das Paket erfordert. Fehlermeldungen können mithilfe von Msimsg.dll.

## <a name="example"></a>Beispiel

[Eigenschaftentabelle](property-table.md)



| Eigenschaft                               | Wert |
|----------------------------------------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | Ein     |



 

[RemoveIniFile-Tabelle](removeinifile-table.md)



| RemoveIniFile                          | Aktion | Wert |
|----------------------------------------|--------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | 4      |       |



 

## <a name="results"></a>Ergebnisse

ICE40 würde die folgenden Fehler melden.



| ICE40-Fehler                                                                                           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) wird in der Property-Tabelle definiert. Dies kann zu Schwierigkeiten führen. | Das Definieren der [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) in .msi datei kann zu unerwartetem Verhalten führen. Um diesen Fehler zu beheben, definieren Sie diese Eigenschaft nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Der RemoveIniFile-Eintrag Remove1 muss einen Wert haben, da die Aktion "Tag löschen" (4) ist.                | In der RemoveIniFile -Spalte der [RemoveIniFile-Tabelle](removeinifile-table.md) gibt es eine Delete Tag-Aktion, ohne ein tag anzugeben, das in der Spalte Value gelöscht werden soll.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Fehlertabelle fehlt. Es werden nur numerische Fehlermeldungen generiert.                              | Diese ICE-Warnung ist veraltet, da Windows Installer nicht erfordert, dass das Paket über die [Fehlertabelle verfügt.](error-table.md) Fehlermeldungen können mithilfe von Msimsg.dll.<br/> Diese Warnung bedeutet, dass .msi Fehlerdatei die Tabelle [](page-count-summary.md) [Fehler](error-table.md) fehlt und die Eigenschaft Zusammenfassung der Seitenanzahl kleiner oder gleich 100 ist. <br/> Um diesen Fehler zu beheben, verwenden Sie eine aktuelle Version des Windows Installers, oder fügen Sie dem Installationspaket eine Fehlertabelle hinzu, und erstellen Sie Formatierungsvorlagen in der Spalte Meldung für Fehlermeldungen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




