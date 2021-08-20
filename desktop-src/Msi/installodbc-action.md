---
description: Die InstallODBC-Aktion installiert die Treiber, Translators und Datenquellen in der ODBCDriver-Tabelle, ODBCTranslator-Tabelle und ODBCDataSource-Tabelle.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: InstallODBC-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a371aed67ec412c46946d7df7fd4775f0a0d4e20d91cbb60d69f894371f203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142224"
---
# <a name="installodbc-action"></a>InstallODBC-Aktion

Die InstallODBC-Aktion installiert die Treiber, Translators und Datenquellen in der [ODBCDriver-Tabelle,](odbcdriver-table.md) [ODBCTranslator-Tabelle](odbctranslator-table.md)und [ODBCDataSource-Tabelle.](odbcdatasource-table.md) Wenn bereits ein Treiber oder Translator vorhanden ist, macht die InstallODBC-Aktion SQL aufruft, die für die Installation erforderlich sind.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die InstallODBC-Aktion kopiert oder entfernt keine Dateien und muss nach Aktionen sein, die Dateien kopieren oder entfernen.

## <a name="actiondata-messages"></a>ActionData-Meldungen

In der folgenden Tabelle sind die ActionData-Meldungen für jeden installierten Treiber aufgeführt.



| Feld       | Beschreibung                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Treiberbeschreibung. Der ODBC-Treiberschlüssel.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | Ordner.                                                                  |
| \[4, 5, ...\] | Attribut- und Wertpaare aus [ODBCAttribute](odbcattribute-table.md). |



 

In der folgenden Tabelle sind die ActionData-Meldungen für jeden installierten Translator aufgeführt.



| Feld       | Beschreibung                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Treiberbeschreibung. Der ODBC-Treiberschlüssel.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | Ordner.                                                                  |
| \[4, 5, ...\] | Attribut- und Wertpaare aus [ODBCAttribute](odbcattribute-table.md). |



 

In der folgenden Tabelle sind die ActionData-Meldungen für jede installierte Datenquelle aufgeführt.



| Feld       | Beschreibung                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Treiberbeschreibung. Der ODBC-Treiberschlüssel.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | Registrierung: ODBC \_ ADD \_ DSN oder ODBC \_ ADD SYS \_ \_ DSN.                     |
| \[4, 5, ...\] | Attribut- und Wertpaare aus [ODBCAttribute](odbcattribute-table.md). |



 

## <a name="remarks"></a>Hinweise

Der ODBC-Treiber-Manager muss im Microsoft Installer-Paket erstellt werden, und eine Komponente namens ODBCDriverManager muss enthalten sein. Der Manager wird bei Bedarf installiert.

Um die Komponente umzubenennen, legen Sie eine Eigenschaft namens ODBCDriverManager auf den neuen Namen der Komponente fest. Wenn ein 64-Bit-ODBC-Treiber-Manager installiert werden soll, sollte die Komponente, die ihn enthält, ODBCDriverManager64 heißen.

-   Die InstallODBC-Aktion fragt die [ODBCDataSource-Tabelle](odbcdatasource-table.md) und die [ODBCSourceAttribute-Tabelle](odbcsourceattribute-table.md) für jede zu installierende Datenquelle und die Attribute der Datenquelle ab.
-   Die InstallODBC-Aktion fragt die [ODBCDriver-Tabelle](odbcdriver-table.md) und die [ODBCTranslator-Tabelle](odbctranslator-table.md) für jeden Treiber und Translator ab, der für die Installation ausgewählt ist.
-   Die InstallODBC-Aktion fragt die [ODBCAttribute-Tabelle](odbcattribute-table.md) nach den Attributen der Treiber und Translator ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Beispiele für Installationsprogramme](windows-installer-examples.md)
</dt> </dl>

 

 



