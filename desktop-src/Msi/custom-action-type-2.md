---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 2 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Benutzerdefinierter Aktionstyp 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba648578ecdd9d300a5cf15793e3abd9407f78853830f49c16a26db184ff3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996850"
---
# <a name="custom-action-type-2"></a>Benutzerdefinierter Aktionstyp 2

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die über eine Befehlszeile gestartet wurde.

## <a name="source"></a>Quelle

Die ausführbare Datei wird aus einem temporären binären Stream generiert. Das Feld Source der [CustomAction-Tabelle enthält](customaction-table.md) einen Schlüssel für die [Binärtabelle](binary-table.md). Die Spalte Daten in der Binärtabelle enthält die Datenstromdaten. Jeder Zeile wird ein separater Stream zugeordnet.

Neue Binärdaten können aus einer Datei eingefügt werden, indem [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) gefolgt von [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) zum Einfügen des Datensatzes in die Tabelle verwendet wird. Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann je nach Typ der benutzerdefinierten Aktion verarbeitet wird.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |



 

## <a name="target"></a>Ziel

Die Spalte Target der [CustomAction-Tabelle enthält](customaction-table.md) die Befehlszeilenzeichenfolge für die ausführbare Datei mit dem Namen in der Spalte Source.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Schließen Sie optionale Flagbits in die Spalte Typ der CustomAction-Tabelle ein, um Rückgabeverarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter Rückgabeverarbeitungsoptionen [für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Schließen Sie optionale Flagbits in die Spalte Typ der CustomAction-Tabelle ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung benutzerdefinierter Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Benutzerdefinierte Aktionsausführungsplanung.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Schließen Sie optionale Flagbits in die Spalte Typ der CustomAction-Tabelle ein, um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, bei denen es sich [um ausführbare Dateien](executable-files.md) handelt, müssen den Wert 0 zurückgeben, um erfolgreich zu sein. Das Installationsprogramm interpretiert alle anderen Rückgabewerte als Fehler. Um Rückgabewerte zu ignorieren, legen Sie das **Bitflag msidbCustomActionTypeContinue** im Feld Type der CustomAction-Tabelle fest.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, verwendet eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt werden. Wenn es sich auch um eine benutzerdefinierte Aktion mit verzögerter Ausführung [handelt,](deferred-execution-custom-actions.md)verwendet das Installationsprogramm [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) oder [**CreateProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) um den Prozess zu erstellen, wenn die benutzerdefinierte Aktion über das Installationsskript aufgerufen wird.

Wenn eine Datenbanktabelle exportiert wird, wird jeder Stream als separate Datei im Unterordner nach der Tabelle geschrieben. Dabei wird der Primärschlüssel als Dateiname (Name-Spalte für die Binärtabelle) mit der Standarderweiterung ".ibd" verwendet. Der Name sollte das Format 8.3 verwenden, wenn das Dateisystem oder Versionskontrollsystem keine langen Dateinamen unterstützt. Die persistente Archivdatei ersetzt die Datenstromdaten durch den verwendeten Dateinamen, sodass die Daten beim Importieren der Tabelle gefunden werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Ausführbare Dateien](executable-files.md)
</dt> </dl>

 

 
