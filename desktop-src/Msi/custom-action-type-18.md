---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 18 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Benutzerdefinierter Aktionstyp 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3befbb614e9ee78961cf5b8ef969bdb3d6e7b6c0cb713a267cab3d09b4588d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379276"
---
# <a name="custom-action-type-18"></a>Benutzerdefinierter Aktionstyp 18

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die über eine Befehlszeile gestartet wurde.

## <a name="source"></a>Quelle

Die ausführbare Datei wird aus einer Datei generiert, die mit der Anwendung installiert wurde. Das Feld Source der [CustomAction-Tabelle enthält](customaction-table.md) einen Schlüssel für die [Dateitabelle](file-table.md). Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem die Datei installiert und entfernt wurde.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |



 

## <a name="target"></a>Ziel

Die Spalte Target der [CustomAction-Tabelle enthält](customaction-table.md) die Befehlszeilenzeichenfolge für die ausführbare Datei, die in der Spalte Source angegeben ist.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Rückgabeverarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter Rückgabeverarbeitungsoptionen [für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung benutzerdefinierter Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Benutzerdefinierte Aktionsausführungsplanung.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, bei denen es sich [um ausführbare Dateien](executable-files.md) handelt, müssen den Wert 0 zurückgeben, um erfolgreich zu sein. Das Installationsprogramm interpretiert alle anderen Rückgabewerte als Fehler. Um Rückgabewerte zu ignorieren, legen Sie das **Bitflag msidbCustomActionTypeContinue** im Feld Type der CustomAction-Tabelle fest.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, verwendet eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt werden. Wenn es sich auch um eine benutzerdefinierte Aktion mit verzögerter Ausführung [handelt,](deferred-execution-custom-actions.md)verwendet das Installationsprogramm [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) oder [**CreateProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) um den Prozess zu erstellen, wenn die benutzerdefinierte Aktion über das Installationsskript aufgerufen wird.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. B. Benutzerdefinierter Aktionstyp 18 (EXE), müssen die folgenden Sequenzierungseinschränkungen einhalten:

-   Die benutzerdefinierte Aktion muss nach der [CostFinalize-Aktion sequenziert werden.](costfinalize-action.md) Dies ist so, dass die benutzerdefinierte Aktion den Pfad auflösen kann, der zum Suchen der EXE-Datei erforderlich ist.
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen verzögerte (skriptbasierte) benutzerdefinierte Aktionen dieses Typs nach der [InstallFiles-Aktion sequenziert werden.](installfiles-action.md)
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion sequenziert werden.](installfinalize-action.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Ausführbare Dateien](executable-files.md)
</dt> </dl>

 

 
