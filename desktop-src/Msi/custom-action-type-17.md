---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 17 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Benutzerdefinierter Aktionstyp 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c54d19f99c552b731d88ab62926212539381f40e202a044c31a41fd906a7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947988"
---
# <a name="custom-action-type-17"></a>Benutzerdefinierter Aktionstyp 17

Diese benutzerdefinierte Aktion ruft eine dll (Dynamic Link Library) auf, die in C oder C++ geschrieben ist.

## <a name="source"></a>Quelle

Die DLL wird während der aktuellen Sitzung mit der Anwendung installiert. Das Feld Source der [CustomAction-Tabelle enthält](customaction-table.md) einen Schlüssel für die [Dateitabelle](file-table.md). Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem diese Datei installiert und entfernt wurde.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile** | 0x011       | 17      |



 

## <a name="target"></a>Ziel

Die DLL wird über den Einstiegspunkt aufgerufen, der im Feld Target der [CustomAction-Tabelle](customaction-table.md)benannt ist, und über gibt ein einzelnes Argument, das das Handle ist, an die aktuelle Installationssitzung weiter. Der in der Tabelle angegebene Einstiegspunktname muss mit dem aus der DLL exportierten Übereinstimmen. Beachten Sie, dass , wenn die Eintragsfunktion nicht von einem angegeben wird. DEF-Datei oder durch eine /EXPORT: Linkerspezifikation kann der Name einen führenden Unterstrich und ein Suffix " @4 " aufweisen. Die aufgerufene Funktion muss die \_ \_ Aufrufkonvention stdcall angeben.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Rückgabeverarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter Rückgabeverarbeitungsoptionen [für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung benutzerdefinierter Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Benutzerdefinierte Aktionsausführungsplanung.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen [finden Sie unter Rückgabewerte für benutzerdefinierte Aktionen.](custom-action-return-values.md)

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die eine Dynamic Link Library (DLL) aufruft, erfordert ein Handle für die Installationssitzung. Wenn es sich auch um eine benutzerdefinierte Aktion mit verzögerter Ausführung handelt, ist die Sitzung während der Ausführung des Installationsskripts möglicherweise nicht mehr vorhanden. Informationen dazu, wie eine benutzerdefinierte Aktion dieses Typs Kontextinformationen abrufen kann, finden Sie unter Abrufen von Kontextinformationen für benutzerdefinierte Aktionen [mit verzögerter Ausführung.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Benutzerdefinierte Aktionen werden in einem separaten Thread ausgeführt und haben möglicherweise eingeschränkten Zugriff auf das System. Benutzerdefinierte Aktionen, die asynchron ausgeführt werden, blockieren den Hauptthread bei Beendigung der aktuellen Sequenz oder der Installationssitzung, bis sie zurückkehren.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. B. BENUTZERDEFINIERTEr Aktionstyp 17 (DLL), müssen die folgenden Sequenzierungseinschränkungen einhalten:

-   Die benutzerdefinierte Aktion muss nach der [CostFinalize-Aktion sequenziert werden.](costfinalize-action.md) Dies ist so, dass die benutzerdefinierte Aktion den Pfad auflösen kann, der zum Suchen der DLL erforderlich ist.
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen verzögerte (skriptbasierte) benutzerdefinierte Aktionen dieses Typs nach der [InstallFiles-Aktion sequenziert werden.](installfiles-action.md)
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion sequenziert werden.](installfinalize-action.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Benutzerdefinierte Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)
</dt> <dt>

[Dynamic Link Libraries](dynamic-link-libraries.md)
</dt> </dl>

 

 



