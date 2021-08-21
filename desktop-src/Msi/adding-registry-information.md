---
description: Die Registrierungstabelle und die zugehörigen Tabellen der Installationsdatenbank enthalten die Registrierungsinformationen, die die Anwendung in der Systemregistrierung schreiben muss.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Hinzufügen von Registrierungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df31ad20fef317d5d67f7f45a7b877511d4c35b05b1517c529693e787306b44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066410"
---
# <a name="adding-registry-information"></a>Hinzufügen von Registrierungsinformationen

Die [Registrierungstabelle](registry-table.md)und die zugehörigen Tabellen der Installationsdatenbank enthalten die Registrierungsinformationen, die die Anwendung in der Systemregistrierung schreiben muss. Weitere Informationen finden Sie [in der Gruppe Registrierungstabellen.](registry-tables-group.md) In diesem Abschnitt fügen Sie die Informationen hinzu, die auf dem Computer des Benutzers durch das Beispiel Editor werden sollen.

Verwenden Sie Ihren Datenbank-Editor, um MNP2000.msi, und geben Sie die folgenden Daten in die leere Registrierungstabelle ein.

[Registrierungstabelle](registry-table.md)



| Registry       | Root | Schlüssel                                 | Name             | Wert    | Komponente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfCharSet        | \#0      | Editor     |
| ClipPrecision  | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfClipPrecision  | \#2      | Editor     |
| Hemmung     | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfFaceName       | FixedSys | Editor     |
| Kursiv         | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfItalic         | \#0      | Editor     |
| Orientation    | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfOrientation    | \#0      | Editor     |
| OutPrecision   | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfOutPrecision   | \#1      | Editor     |
| Pagesettings   | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | fSavePageSetting | \#0      | Editor     |
| PitchAndFamily | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfPitchAndFamily | \#49     | Editor     |
| PointSize      | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | iPointSize       | \#120    | Editor     |
| Qualität        | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfQuality        | \#2      | Editor     |
| Durchgestrichen      | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfStrikeOut      | \#0      | Editor     |
| Weight         | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | lfWeight         | \#400    | Editor     |
| Umschließen           | 2    | SOFTWARE \\ Microsoft \\ Editor Sample | fWrap            | \#0      | Editor     |



 

[Fortsetzen](specifying-shortcuts.md)

 

 



