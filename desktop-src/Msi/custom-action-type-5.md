---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 5 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Benutzerdefinierter Aktionstyp 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e5d6ea37d8efcc5a5d9517b36fb3ae5620830ae1a84173cb9a5488c57cc24e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086220"
---
# <a name="custom-action-type-5"></a>Benutzerdefinierter Aktionstyp 5

Diese benutzerdefinierte Aktion ist in JScript geschrieben, z. B. ECMA 262. Windows Das Installationsprogramm unterstützt JScript 1.0 nicht. Weitere Informationen finden Sie unter [Skripts.](scripts.md)

## <a name="source"></a>Quelle

Das Skript wird aus einem temporären binären Stream generiert. Das Feld Quelle der [CustomAction-Tabelle](customaction-table.md) enthält einen Schlüssel für die [Binärtabelle](binary-table.md). Die Spalte Daten in der Tabelle Binär enthält die Streamdaten. Für jede Zeile wird ein separater Stream zugeordnet.

Neue Binärdaten können aus einer Datei eingefügt werden, indem [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) gefolgt von [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) verwendet wird, um den Datensatz in die Tabelle einzufügen. Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann entsprechend dem Typ der benutzerdefinierten Aktion verarbeitet wird.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ der benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                              | Hexadezimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData** | 0x05        | 5       |



 

Windows Das Installationsprogramm kann benutzerdefinierte 64-Bit-Aktionen unter 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript-Bit** in seinem numerischen Typ enthalten. Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md) Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                     | Hexadezimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript** | 0x0001005   | 4101    |



 

## <a name="target"></a>Ziel

Das Feld Target der [Tabelle CustomAction](customaction-table.md) enthält eine optionale Skriptfunktion. Die Verarbeitung sendet zuerst das Skript zur Analyse und ruft dann die optionale Skriptfunktion auf.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Rückgabeverarbeitung anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter [Benutzerdefinierte Optionen für die Aktionsrückgabeverarbeitung.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

In Skript geschriebene optionale Funktionen müssen einen der unter [Rückgabewerte von JScript und benutzerdefinierten VBScript-Aktionen](return-values-of-jscript-and-vbscript-custom-actions.md)beschriebenen Werte zurückgeben.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, erfordert die Installation des [**Sitzungsobjekts**](session-object.md). Das Installationsprogramm fügt das **Session-Objekt** mit dem Namen *Sitzung* an das Skript an. Da das **Session-Objekt** während eines Installationsrollbacks möglicherweise nicht vorhanden ist, muss eine im Skript geschriebene verzögerte benutzerdefinierte Aktion eine der Methoden oder Eigenschaften des **Session-Objekts** verwenden, die im Abschnitt [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben sind, um den Kontext abzurufen.

Wenn eine Datenbanktabelle exportiert wird, wird jeder Stream als separate Datei im Unterordner geschrieben, der nach der Tabelle benannt ist. Dabei wird der Primärschlüssel als Dateiname (Namensspalte für die Binärtabelle) mit der Standarderweiterung ".ibd" verwendet. Der Name sollte das Dateiformat 8.3 verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt. Die persistente Archivdatei ersetzt die Datenstromdaten durch den verwendeten Dateinamen, sodass die Daten beim Importieren der Tabelle gefunden werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



