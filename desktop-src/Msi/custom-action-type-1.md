---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 1 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Benutzerdefinierter Aktionstyp 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3437fcd8a9a0da84ecb03f2527d30b6644210b2feb2ccc6c5f6558c3667a0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044900"
---
# <a name="custom-action-type-1"></a>Benutzerdefinierter Aktionstyp 1

Diese benutzerdefinierte Aktion ruft eine DLL (Dynamic Link Library) auf, die in C oder C++ geschrieben wurde.

## <a name="source"></a>Quelle

Die DLL wird aus einem temporären binären Stream generiert. Das Feld Quelle der [CustomAction-Tabelle](customaction-table.md) enthält einen Schlüssel für die [Binärtabelle](binary-table.md).

Die Spalte Daten in der Tabelle Binär enthält die Streamdaten. Für jede Zeile wird ein separater Stream zugeordnet. Neue Binärdaten können aus einer Datei eingefügt werden, indem [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) gefolgt von [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) verwendet wird, um den Datensatz in die Tabelle einzufügen. Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann abhängig vom Typ der benutzerdefinierten Aktion verarbeitet wird.

## <a name="type-value"></a>Typwert

Fügen Sie die folgenden Flagbits in die Spalte Type der [CustomAction-Tabelle](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                          | Hexadezimal | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

## <a name="target"></a>Ziel

Die DLL wird über den Einstiegspunkt namens im Feld Target der [CustomAction-Tabelle](customaction-table.md)aufgerufen und übergibt ein einzelnes Argument, das das Handle für die aktuelle Installationssitzung ist. Der in der Tabelle angegebene Einstiegspunktname muss mit dem aus der DLL exportierten übereinstimmen. Beachten Sie Folgendes: Wenn die Eintragsfunktion nicht von einem angegeben wird. DEF-Datei oder durch eine /EXPORT:-Linkerspezifikation kann der Name einen führenden Unterstrich und das @4 Suffix " " aufweisen. Die aufgerufene Funktion muss die \_ \_ stdcall-Aufrufkonvention angeben.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Rückgabeverarbeitung anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter [Benutzerdefinierte Optionen für die Aktionsrückgabeverarbeitung.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen finden Sie unter [Rückgabewerte für benutzerdefinierte Aktionen.](custom-action-return-values.md)

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die eine DLL (Dynamic Link Library) aufruft, erfordert ein Handle für die Installationssitzung. Wenn es sich auch um eine benutzerdefinierte Aktion mit verzögerter Ausführung handelt, ist die Sitzung während der Ausführung des Installationsskripts möglicherweise nicht mehr vorhanden. Informationen dazu, wie eine benutzerdefinierte Aktion dieses Typs Kontextinformationen abrufen kann, finden Sie unter [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Wenn eine Datenbanktabelle exportiert wird, wird jeder Stream als separate Datei im Unterordner geschrieben, der nach der Tabelle benannt ist. Dabei wird der Primärschlüssel als Dateiname (Namensspalte für die Binärtabelle) mit der Standarderweiterung ".ibd" verwendet. Der Name sollte das Format 8.3 verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt. Die persistente Archivdatei ersetzt die Datenstromdaten durch den verwendeten Dateinamen, sodass die Daten beim Importieren der Tabelle gefunden werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Dynamic Link-Bibliotheken](dynamic-link-libraries.md)
</dt> <dt>

[Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



