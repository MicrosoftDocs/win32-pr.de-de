---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 1 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Benutzerdefinierter Aktionstyp 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050485"
---
# <a name="custom-action-type-1"></a>Benutzerdefinierter Aktionstyp 1

Diese benutzerdefinierte Aktion ruft eine Dynamic Link Library (dll) auf, die in C oder C++ geschrieben ist.

## <a name="source"></a>`Source`

Die dll wird aus einem temporären binären Stream generiert. Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [binäre Tabelle](binary-table.md).

Die Datenspalte in der binären Tabelle enthält die Streamdaten. Für jede Zeile wird ein separater Stream zugeordnet. Neue Binärdaten können mithilfe von " [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ", gefolgt von " [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ", aus einer Datei eingefügt werden, um den Datensatz in die Tabelle einzufügen. Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann abhängig vom Typ der benutzerdefinierten Aktion verarbeitet wird.

## <a name="type-value"></a>Typwert

Fügen Sie die folgenden Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypedll**  +  **msidbcustomaktiontypebinarydata** | 0x001       | 1       |



 

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

Beim Exportieren einer Datenbanktabelle wird jeder Stream als separate Datei in den Unterordner geschrieben, der nach der Tabelle benannt ist. dabei wird der Primärschlüssel als Dateiname (Namensspalte für die binäre Tabelle) mit der Standard Erweiterung ". ibd" verwendet. Der Name sollte das 8,3-Format verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt. Die permanente Archivdatei ersetzt die Streamdaten durch den verwendeten Dateinamen, damit die Daten beim Importieren der Tabelle gefunden werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Dynamic Link Libraries](dynamic-link-libraries.md)
</dt> <dt>

[Abrufen von Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



