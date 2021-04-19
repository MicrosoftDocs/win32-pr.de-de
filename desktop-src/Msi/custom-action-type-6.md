---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 6 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Benutzerdefinierter Aktionstyp 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348705"
---
# <a name="custom-action-type-6"></a>Benutzerdefinierter Aktionstyp 6

Diese benutzerdefinierte Aktion wird in VBScript geschrieben. Weitere Informationen finden Sie unter [Skripts](scripts.md).

## <a name="source"></a>`Source`

Das Skript wird aus einem temporären binären Stream generiert. Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [binäre Tabelle](binary-table.md). Die Datenspalte in der binären Tabelle enthält die Streamdaten. Für jede Zeile wird ein separater Stream zugeordnet.

Neue Binärdaten können mithilfe von " [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ", gefolgt von " [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ", aus einer Datei eingefügt werden, um den Datensatz in die Tabelle einzufügen. Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann abhängig vom Typ der benutzerdefinierten Aktion verarbeitet wird.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                               | Hexadezimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypebinarydata** | 0x006       | 6       |



 

Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen. Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md). Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                      | Hexadezimal | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypebinarydata**  +  **msidbCustomActionType64BitScript** | 0x0001006   | 4102    |



 

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

Eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, erfordert die Installation des [**Session-Objekts**](session-object.md). Das Installationsprogramm fügt das **Sitzungs** Objekt mit der namens *Sitzung* an das Skript an. Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.

Beim Exportieren einer Datenbanktabelle wird jeder Stream als separate Datei in den Unterordner geschrieben, der nach der Tabelle benannt ist. dabei wird der Primärschlüssel als Dateiname (Namensspalte für die binäre Tabelle) mit der Standard Erweiterung ". ibd" verwendet. Der Name sollte das Format "8,3 File Name" verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt. Die permanente Archivdatei ersetzt die Streamdaten durch den verwendeten Dateinamen, damit die Daten beim Importieren der Tabelle gefunden werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



