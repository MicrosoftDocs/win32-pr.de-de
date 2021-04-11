---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 38 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Benutzerdefinierter Aktionstyp 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960266"
---
# <a name="custom-action-type-38"></a>Benutzerdefinierter Aktionstyp 38

Diese benutzerdefinierte Aktion wird in VBScript geschrieben. Siehe auch [Skripts](scripts.md).

## <a name="source"></a>`Source`

Das Quellfeld der [CustomAction-Tabelle](customaction-table.md) enthält den Nullwert. Der Skriptcode für die benutzerdefinierte Aktion wird als Zeichenfolge mit literalem Skript Text im Feld Ziel gespeichert.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                              | Hexadezimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypedirectory** | 0x026       | 38      |



 

Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen. Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md). Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                     | Hexadezimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypedirectory**  +  **msidbCustomActionType64BitScript** | 0x0001026   | 4134    |



 

## <a name="target"></a>Ziel

Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält den Skriptcode für die benutzerdefinierte Aktion als eine Zeichenfolge mit literalem Skript Text.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben. Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript. Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Dieser benutzerdefinierte Aktionstyp gibt immer Erfolg zurück.

## <a name="remarks"></a>Bemerkungen

Für eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, ist das install [**Session**](session-object.md) -Objekt erforderlich. Das Installationsprogramm fügt das **Sitzungs Objekt** mit dem Namen "Session" an das Skript an. Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



