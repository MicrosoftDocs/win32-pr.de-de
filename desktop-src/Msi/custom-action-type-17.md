---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 17 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Benutzerdefinierter Aktionstyp 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348999"
---
# <a name="custom-action-type-17"></a>Benutzerdefinierter Aktionstyp 17

Diese benutzerdefinierte Aktion ruft eine Dynamic Link Library (dll) auf, die in C oder C++ geschrieben ist.

## <a name="source"></a>`Source`

Die dll wird während der aktuellen Sitzung mit der Anwendung installiert. Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Dateitabelle](file-table.md). Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem diese Datei installiert und vor dem Entfernen entfernt wurde.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypedll**  +  **msidbcustomaktiontypesourcefile** | 0x011       | 17      |



 

## <a name="target"></a>Ziel

Die dll wird über den Einstiegspunkt aufgerufen, der im Feld Ziel der [Tabelle CustomAction](customaction-table.md)benannt ist. dabei wird ein einzelnes Argument übergeben, das das Handle für die aktuelle Installationssitzung ist. Der in der Tabelle angegebene Einstiegspunkt Name muss mit dem aus der DLL exportierten Namen identisch sein. Beachten Sie, dass die Einstiegs Funktion nicht von einem angegeben wird. Die DEF-Datei oder eine/Export: Linker-Spezifikation, der Name kann einen vorangeführenden Unterstrich und ein @4 Suffix "" aufweisen. Die aufgerufene Funktion muss die Aufruf \_ \_ Konvention stdcall angeben.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben. Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript. Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).

## <a name="remarks"></a>Bemerkungen

Eine benutzerdefinierte Aktion, die eine Dynamic Link Library (dll) aufruft, erfordert ein Handle für die Installationssitzung. Wenn es sich auch um eine benutzerdefinierte Aktion für die verzögerte Ausführung handelt, ist die Sitzung während der Ausführung des Installations Skripts möglicherweise nicht mehr vorhanden. Informationen dazu, wie eine benutzerdefinierte Aktion dieses Typs Kontextinformationen abrufen kann, finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).

Benutzerdefinierte Aktionen werden in einem separaten Thread ausgeführt und haben möglicherweise begrenzten Zugriff auf das System. Benutzerdefinierte Aktionen, die asynchron ausgeführt werden, blockieren den Hauptthread entweder beim Beenden der aktuellen Sequenz oder der Installationssitzung, bis Sie zurückkehren.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. b. benutzerdefinierter Aktionstyp 17 (dll), müssen die folgenden Sequenz Einschränkungen einhalten:

-   Die benutzerdefinierte Aktion muss nach der [costfinalize-Aktion](costfinalize-action.md)sequenziert werden. Dadurch kann die benutzerdefinierte Aktion den Pfad auflösen, der zum Auffinden der dll erforderlich ist.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen die benutzerdefinierten Aktionen (in Skripts) dieses Typs nach der [InstallFiles-Aktion](installfiles-action.md)sequenziert werden.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Benutzerdefinierte Aktionen für verzögerte Ausführung](deferred-execution-custom-actions.md)
</dt> <dt>

[Dynamic Link Libraries](dynamic-link-libraries.md)
</dt> </dl>

 

 



