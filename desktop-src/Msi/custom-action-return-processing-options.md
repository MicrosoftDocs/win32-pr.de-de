---
description: In diesem Thema werden die Optionsflags identifiziert, mit denen Sie die Verarbeitung des benutzerdefinierten Aktions Threads steuern können.
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: Rückgabe Verarbeitungsoptionen für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8664ff489280993a7fc52117f3d19bccb023b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868880"
---
# <a name="custom-action-return-processing-options"></a>Rückgabe Verarbeitungsoptionen für benutzerdefinierte Aktionen

In diesem Thema werden die Optionsflags identifiziert, mit denen Sie die Verarbeitung des benutzerdefinierten Aktions Threads steuern können. Mithilfe der Flags wird angegeben, dass die Haupt-und benutzerdefinierten aktionsthreads synchron ausgeführt werden (Windows Installer auf den Abschluss des benutzerdefinierten Aktions Threads wartet, bevor der Hauptinstallations Thread fortgesetzt wird) oder asynchron (Windows Installer führt die benutzerdefinierte Aktion gleichzeitig aus, während die Haupt Installation fortgesetzt wird).

Fügen Sie zum Aktivieren der Optionsflags den Wert, der in der folgenden Tabelle angegeben ist, dem Wert im type-Feld der [CustomAction-Tabelle](customaction-table.md)hinzu.



| Konstante                                                           | Hexadezimal             | Decimal | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                                                             | 0x00000000              | +0      | Eine synchrone Ausführung, die fehlschlägt, wenn der Exitcode nicht 0 (null) ist. <br/> Wenn das Flag "msidbcustomaction typecontinue" nicht festgelegt ist, muss die benutzerdefinierte Aktion einen der Rückgabewerte zurückgeben, die in den [Rückgabe Werten der benutzerdefinierten Aktion](custom-action-return-values.md)beschrieben werden.<br/>                                                                                                                                                                                                                             |
| **msidbcustomaktiontypecontinue**                                  | 0x00000040              | + 64     | Eine synchrone Ausführung, die Exitcode ignoriert und fortgesetzt wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbcustomaktiontypeasync**                                     | 0x00000080              | + 128    | Eine asynchrone Ausführung, die auf den Exitcode am Ende der Sequenz wartet.<br/> Diese Option kann nicht mit [gleichzeitigen Installationen](concurrent-installations.md), [Rollbacks von benutzerdefinierten Aktionen](rollback-custom-actions.md)oder Skripterstellung für [benutzerdefinierte Aktionen](scripts.md)verwendet werden.<br/>                                                                                                                                                                                                                                |
| **msidbcustomaktiontypeasync**  +  **msidbcustomaktiontypecontinue** | 0x00000040 + 0x00000080 | +192    | Eine asynchrone Ausführung, die nicht auf den Abschluss wartet.<br/> Die Ausführung wird nach dem Beenden Windows Installer fortgesetzt.<br/> Diese Option kann nur mit den benutzerdefinierten exe-Aktionen verwendet werden, die [ausführbare Dateien](executable-files.md)sind. <br/> Alle anderen Typen von benutzerdefinierten Aktionen können nur in der Installationssitzung asynchron sein und müssen beendet werden, damit die Installation beendet wird.<br/> Diese Option kann nicht mit [gleichzeitigen Installationen](concurrent-installations.md)verwendet werden.<br/> |



 

 

 




