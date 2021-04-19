---
description: Die "installodbc"-Aktion installiert die Treiber, Konvertierer und Datenquellen in der Tabelle "odbcdriver", "odbctranslator" und "ODBCDatasource".
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Installodbc-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350107"
---
# <a name="installodbc-action"></a>Installodbc-Aktion

Die "installodbc"-Aktion installiert die Treiber, Konvertierer und Datenquellen in der Tabelle " [odbcdriver](odbcdriver-table.md)", " [odbctranslator](odbctranslator-table.md)" und " [ODBCDatasource](odbcdatasource-table.md)". Wenn bereits ein Treiber oder ein Konvertierungsprogramm vorhanden ist, werden von der installodbc-Aktion SQL-Aufrufe für die Installation erforderlich.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die "installodbc"-Aktion kopiert oder entfernt keine Dateien und muss nach Aktionen erfolgen, mit denen Dateien kopiert oder entfernt werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

In der folgenden Tabelle sind die Aktions Daten Meldungen für jeden installierten Treiber aufgeführt.



| Feld       | BESCHREIBUNG                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Treiber Beschreibung. Der Schlüssel des ODBC-Treibers.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Ordner.                                                                  |
| \[4, 5,...\] | Attribut-Wert-Paare aus [ODB-Tribute](odbcattribute-table.md). |



 

In der folgenden Tabelle sind die Aktions Daten Meldungen für die einzelnen installierten Konvertierer aufgeführt.



| Feld       | BESCHREIBUNG                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Treiber Beschreibung. Der Schlüssel des ODBC-Treibers.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Ordner.                                                                  |
| \[4, 5,...\] | Attribut-Wert-Paare aus [ODB-Tribute](odbcattribute-table.md). |



 

In der folgenden Tabelle sind die Aktions Daten Meldungen für die einzelnen installierten Datenquellen aufgeführt.



| Feld       | BESCHREIBUNG                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Treiber Beschreibung. Der Schlüssel des ODBC-Treibers.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Registrierung: ODBC \_ Add \_ DSN oder ODBC \_ Add \_ sys \_ DSN.                     |
| \[4, 5,...\] | Attribut-Wert-Paare aus [ODB-Tribute](odbcattribute-table.md). |



 

## <a name="remarks"></a>Bemerkungen

Der ODBC-Treiber-Manager muss im Microsoft Installer-Paket erstellt werden, und es muss eine Komponente mit dem Namen "odbcdrivermanager" eingeschlossen werden. Der Manager wird bei Bedarf installiert.

Legen Sie zum Umbenennen der Komponente eine Eigenschaft mit dem Namen odbcdrivermanager auf den neuen Namen der Komponente fest. Wenn ein 64-Bit-ODBC-Treiber-Manager installiert werden soll, sollte die Komponente, die Sie enthält, den Namen ODBCDriverManager64 haben.

-   Mit der installodbc-Aktion werden die [ODBCDatasource-Tabelle](odbcdatasource-table.md) und die [odbcsourceattribute-Tabelle](odbcsourceattribute-table.md) für jede zu installierende Datenquelle sowie die Attribute der Datenquelle abgefragt.
-   Die installodbc-Aktion fragt die [odbcdriver-Tabelle](odbcdriver-table.md) und die [odbctranslator-Tabelle](odbctranslator-table.md) für jeden Treiber und Konvertierer ab, der für die Installation ausgewählt ist.
-   Die "installodbc"-Aktion fragt die [odbingtribute-Tabelle](odbcattribute-table.md) nach den Attributen der Treiber und Übersetzer ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer Beispiele](windows-installer-examples.md)
</dt> </dl>

 

 



