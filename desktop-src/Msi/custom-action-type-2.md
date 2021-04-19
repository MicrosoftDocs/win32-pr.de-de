---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 2 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Benutzerdefinierter Aktionstyp 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352429"
---
# <a name="custom-action-type-2"></a>Benutzerdefinierter Aktionstyp 2

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde

## <a name="source"></a>`Source`

Die ausführbare Datei wird aus einem temporären binären Stream generiert. Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [binäre Tabelle](binary-table.md). Die Datenspalte in der binären Tabelle enthält die Streamdaten. Für jede Zeile wird ein separater Stream zugeordnet.

Neue Binärdaten können mithilfe von " [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ", gefolgt von " [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ", aus einer Datei eingefügt werden, um den Datensatz in die Tabelle einzufügen. Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann abhängig vom Typ der benutzerdefinierten Aktion verarbeitet wird.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypebinarydata** | 0x002       | 2       |



 

## <a name="target"></a>Ziel

Die Ziel Spalte der [CustomAction-Tabelle](customaction-table.md) enthält die Befehlszeilen Zeichenfolge für die ausführbare Datei, die in der Quell Spalte benannt ist.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der Tabelle CustomAction ein, um die Rückgabe Verarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der Tabelle CustomAction ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Schließen Sie optionale Flagbits in die Spalte Type der Tabelle CustomAction ein, um eine in-Script-Ausführungs Option anzugeben. Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript. Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben. Der Installer interpretiert jeden anderen Rückgabewert als Fehler. Wenn Sie Rückgabewerte ignorieren möchten, legen Sie das **msidbcustomaction typecontinue** -Bitflag im type-Feld der CustomAction-Tabelle fest.

## <a name="remarks"></a>Bemerkungen

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind. Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm [**zum Erstellen**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) des Prozesses den Prozess, wenn [**die benutzerdefinierte**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Aktion aus dem Installationsskript aufgerufen wird.

Beim Exportieren einer Datenbanktabelle wird jeder Stream als separate Datei in den Unterordner geschrieben, der nach der Tabelle benannt ist. dabei wird der Primärschlüssel als Dateiname (Namensspalte für die binäre Tabelle) mit der Standard Erweiterung ". ibd" verwendet. Der Name sollte das 8,3-Format verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt. Die permanente Archivdatei ersetzt die Streamdaten durch den verwendeten Dateinamen, damit die Daten beim Importieren der Tabelle gefunden werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Ausführbare Dateien](executable-files.md)
</dt> </dl>

 

 
