---
description: Entwickler von Windows Installer-Paketen können den benutzerdefinierten Aktionstyp 53 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Benutzerdefinierter Aktionstyp 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b78c2dbc8aa233175eeacfa8d16521968dfceeb6b97504e639946c6284b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947891"
---
# <a name="custom-action-type-53"></a>Benutzerdefinierter Aktionstyp 53

Diese benutzerdefinierte Aktion wird in JScript geschrieben, z. B. ECMA 262. Windows Das Installationsprogramm unterstützt JScript 1.0 nicht. Weitere Informationen finden Sie unter [Skripts](scripts.md).

## <a name="source"></a>Quelle

Das Feld Source der [CustomAction-Tabelle](customaction-table.md) enthält einen Eigenschaftennamen oder einen Schlüssel für die [Property-Tabelle](property-table.md) für eine Eigenschaft, die den Skripttext enthält.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                            | Hexadezimal | Decimal |
|----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty** | 0x035       | 53      |



 

Windows Das Installationsprogramm kann benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **bit msidbCustomActionType64BitScript** in seinem numerischen Typ enthalten. Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md) Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                   | Hexadezimal | Decimal |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001035   | 4149    |



 

## <a name="target"></a>Ziel

Das Feld Target der [CustomAction-Tabelle enthält](customaction-table.md) eine optionale Skriptfunktion. Die Verarbeitung sendet zuerst das Skript für die Analyse und ruft dann die optionale Skriptfunktion auf.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Rückgabeverarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter Rückgabeverarbeitungsoptionen [für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung benutzerdefinierter Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Benutzerdefinierte Aktionsausführungsplanung.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Optionale Funktionen, die im Skript geschrieben werden, müssen einen der unter Rückgabewerte von JScript [und benutzerdefinierten VBScript-Aktionen beschriebenen Werte zurückgeben.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Hinweise

Für eine benutzerdefinierte Aktion, die in JScript, ist das Sitzungsobjekt [**für die Installation**](session-object.md) erforderlich. Da das **Session-Objekt** während eines Installationsrollbacks möglicherweise nicht vorhanden ist, verwendet eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben wird, eine der Methoden, die unter Abrufen von Kontextinformationen für benutzerdefinierte Aktionen für verzögerte Ausführung [beschrieben sind.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



