---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 21 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Benutzerdefinierter Aktionstyp 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6184455b15b1bcea1c53532ef53ef526b7af159d81322994220186d6cd187e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105259"
---
# <a name="custom-action-type-21"></a>Benutzerdefinierter Aktionstyp 21

Diese benutzerdefinierte Aktion wird in JScript geschrieben, z. B. ECMA 262. Windows Das Installationsprogramm unterstützt JScript 1.0 nicht. Weitere Informationen finden Sie unter [Skripts](scripts.md).

## <a name="source"></a>Quelle

Das Skript wird während der aktuellen Sitzung mit der Anwendung installiert. Das Feld Source der [CustomAction-Tabelle enthält](customaction-table.md) einen Schlüssel für die [Dateitabelle](file-table.md). Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. Daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem die Datei installiert und entfernt wurde.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                              | Hexadezimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile** | 0x015       | 21      |



 

Windows Das Installationsprogramm kann [benutzerdefinierte 64-Bit-Aktionen auf](64-bit-custom-actions.md) 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **bit msidbCustomActionType64BitScript** in seinem numerischen Typ enthalten. Weitere Informationen finden Sie unter Benutzerdefinierte 64-Bit-Aktionen. Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                     | Hexadezimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript** | 0x0001015   | 4117    |



 

## <a name="target"></a>Ziel

Das Feld Target der [CustomAction-Tabelle enthält](customaction-table.md) eine optionale Skriptfunktion. Die Verarbeitung sendet zuerst das Skript für die Analyse und ruft dann die optionale Skriptfunktion auf.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Rückgabeverarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter Rückgabeverarbeitungsoptionen [für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung benutzerdefinierter Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Benutzerdefinierte Aktionsausführungsplanung.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

Optionale Funktionen, die im Skript geschrieben werden, müssen einen der unter Rückgabewerte von JScript [und benutzerdefinierten VBScript-Aktionen beschriebenen Werte zurückgeben.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Hinweise

Für eine benutzerdefinierte Aktion, die in JScript VBScript geschrieben ist, ist das [**Session-Installationsobjekt**](session-object.md) erforderlich. Das Installationsprogramm hängt das **Sitzungsobjekt** mit dem Namen "Session" an das Skript an. Da das **Session-Objekt** während eines Installationsrollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben wurde, eine der Methoden oder Eigenschaften des **Session-Objekts** verwenden, die im Abschnitt [Abrufen](obtaining-context-information-for-deferred-execution-custom-actions.md) von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung beschrieben sind, um den Kontext abzurufen.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. B. Benutzerdefinierter Aktionstyp 21 (JScript), müssen die folgenden Sequenzierungseinschränkungen einhalten:

-   Die benutzerdefinierte Aktion muss nach der [CostFinalize-Aktion sequenziert werden.](costfinalize-action.md) Dies ist so, dass die benutzerdefinierte Aktion den Pfad auflösen kann, der zum Suchen der Quelldatei mit dem JScript.
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen verzögerte (skriptbasierte) benutzerdefinierte Aktionen dieses Typs nach der [InstallFiles-Aktion sequenziert werden.](installfiles-action.md)
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion sequenziert werden.](installfinalize-action.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



