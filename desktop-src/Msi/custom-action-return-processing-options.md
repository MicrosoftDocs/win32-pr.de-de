---
description: In diesem Thema werden die Optionsflags identifiziert, mit denen Sie die Verarbeitung des benutzerdefinierten Aktionsthreads steuern können.
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: Rückgabeverarbeitungsoptionen für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2dd719271e6291decbd2123d5cf1525121769704b3fc4177c8b301662697689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947978"
---
# <a name="custom-action-return-processing-options"></a>Rückgabeverarbeitungsoptionen für benutzerdefinierte Aktionen

In diesem Thema werden die Optionsflags identifiziert, mit denen Sie die Verarbeitung des benutzerdefinierten Aktionsthreads steuern können. Die Flags werden verwendet, um anzugeben, dass die Haupt- und benutzerdefinierten Aktionsthreads synchron ausgeführt werden (Windows Installer wartet auf den Abschluss des benutzerdefinierten Aktionsthreads, bevor der Hauptinstallationsthread fortgesetzt wird), oder asynchron (Windows Installer führt die benutzerdefinierte Aktion gleichzeitig aus, während die Hauptinstallation fortgesetzt wird).

Um die Optionsflags zu aktivieren, fügen Sie den in der folgenden Tabelle identifizierten Wert dem Wert im Feld Typ der [CustomAction-Tabelle hinzu.](customaction-table.md)



| Konstante                                                           | Hexadezimal             | Decimal | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                                                             | 0x00000000              | +0      | Eine synchrone Ausführung, die fehlschlägt, wenn der Exitcode nicht 0 (null) ist. <br/> Wenn das Flag msidbCustomActionTypeContinue nicht festgelegt ist, muss die benutzerdefinierte Aktion einen der Rückgabewerte zurückgeben, die unter Rückgabewerte für [benutzerdefinierte Aktionen](custom-action-return-values.md)beschrieben sind.<br/>                                                                                                                                                                                                                             |
| **msidbCustomActionTypeContinue**                                  | 0x00000040              | +64     | Eine synchrone Ausführung, die Exitcode ignoriert und fortgesetzt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbCustomActionTypeAsync**                                     | 0x00000080              | +128    | Eine asynchrone Ausführung, die am Ende der Sequenz auf Exitcode wartet.<br/> Diese Option kann nicht mit [gleichzeitigen Installationen,](concurrent-installations.md) [rollback custom actions](rollback-custom-actions.md)oder [Script Custom Actions](scripts.md)verwendet werden.<br/>                                                                                                                                                                                                                                |
| **msidbCustomActionTypeAsync**  +  **msidbCustomActionTypeContinue** | 0x00000040 + 0x00000080 | +192    | Eine asynchrone Ausführung, die nicht auf den Abschluss wartet.<br/> Die Ausführung wird fortgesetzt, nachdem Windows Installer beendet wurde.<br/> Diese Option kann nur mit den benutzerdefinierten Aktionen vom Typ EXE verwendet werden, d. h. [ausführbaren Dateien.](executable-files.md) <br/> Alle anderen Arten von benutzerdefinierten Aktionen können nur innerhalb der Installationssitzung asynchron sein und müssen beendet werden, damit die Installation beendet wird.<br/> Diese Option kann nicht mit [gleichzeitigen Installationen](concurrent-installations.md)verwendet werden.<br/> |



 

 

 




