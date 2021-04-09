---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 18 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Benutzerdefinierter Aktionstyp 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960712"
---
# <a name="custom-action-type-18"></a>Benutzerdefinierter Aktionstyp 18

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde

## <a name="source"></a>`Source`

Die ausführbare Datei wird aus einer Datei generiert, die mit der Anwendung installiert wird. Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Dateitabelle](file-table.md). Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem die Datei installiert und vor dem Entfernen entfernt wurde.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypesourcefile** | 0x012       | 18      |



 

## <a name="target"></a>Ziel

Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält die Befehlszeilen Zeichenfolge für die in der Spalte Quelle identifizierte ausführbare Datei.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben. Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript. Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben. Der Installer interpretiert jeden anderen Rückgabewert als Fehler. Wenn Sie Rückgabewerte ignorieren möchten, legen Sie das **msidbcustomaction typecontinue** -Bitflag im type-Feld der CustomAction-Tabelle fest.

## <a name="remarks"></a>Bemerkungen

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind. Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm [**zum Erstellen**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) des Prozesses den Prozess, wenn [**die benutzerdefinierte**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Aktion aus dem Installationsskript aufgerufen wird.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. b. der benutzerdefinierte Aktionstyp 18 (exe), müssen die folgenden Sequenz Einschränkungen einhalten:

-   Die benutzerdefinierte Aktion muss nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden. Dadurch kann die benutzerdefinierte Aktion den Pfad auflösen, der zum Auffinden der exe benötigt wird.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen die benutzerdefinierten Aktionen (in Skripts) dieses Typs nach der [InstallFiles-Aktion](installfiles-action.md)sequenziert werden.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Ausführbare Dateien](executable-files.md)
</dt> </dl>

 

 
