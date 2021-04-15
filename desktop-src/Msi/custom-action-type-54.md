---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 54 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Benutzerdefinierter Aktionstyp 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485491"
---
# <a name="custom-action-type-54"></a>Benutzerdefinierter Aktionstyp 54

Diese benutzerdefinierte Aktion wird in VBScript geschrieben. Siehe auch [Skripts](scripts.md).

## <a name="source"></a>`Source`

Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Eigenschaftsnamen oder einen Schlüssel für die [Eigenschaften Tabelle](property-table.md) für eine Eigenschaft, die den Skript Text enthält.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                             | Hexadezimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypeproperty** | 0x036       | 54      |



 

Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen. Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md). Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                    | Hexadezimal | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypeproperty**  +  **msidbCustomActionType64BitScript** | 0x0001036   | 4150    |



 

## <a name="target"></a>Ziel

Das Zielfeld der [CustomAction-Tabelle](customaction-table.md) enthält eine optionale Skriptfunktion. Die Verarbeitung sendet zuerst das Skript für die Verarbeitung und ruft dann die optionale Skriptfunktion auf.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben. Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript. Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Optionale Funktionen, die im Skript geschrieben werden, müssen einen der Werte zurückgeben, die unter [Rückgabewerte der benutzerdefinierten Aktionen JScript und VBScript](return-values-of-jscript-and-vbscript-custom-actions.md)beschrieben werden.

## <a name="remarks"></a>Bemerkungen

Für eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, ist das install [**Session**](session-object.md) -Objekt erforderlich. Das Installationsprogramm fügt das **Sitzungs Objekt** mit der namens *Sitzung* an das Skript an. Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



