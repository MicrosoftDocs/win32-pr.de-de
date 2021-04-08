---
description: Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über Structured Query Language (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: Wssql
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862160"
---
# <a name="wssql"></a>Wssql

Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über Structured Query Language (SQL).

Dieses Thema enthält folgende Abschnitte:

- [Anforderungen](#requirements)
- [Herunterladen des Beispiels](#downloading-the-sample)
- [Beispiel zum Aufbau](#building-the-sample)
- [Ausführen des Beispiels](#running-the-sample)
- [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen

| Produkt     | Produktversion          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 oder 10    |
| Windows SDK | 7,0 oder höher           |

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im folgenden Speicherort verfügbar.

| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Wssql-Beispiel](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

## <a name="building-the-sample"></a>Erstellen des Beispiels

1. Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis von **wssql** .
2. Doppelklicken Sie auf das Symbol für die Datei wssql. sln, um das Projekt in Visual Studio zu öffnen.
    > [!NOTE]  
    > Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen. Dies wirkt sich nicht auf das Verhalten des Beispiels aus.

3. Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1. Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2. Geben Sie an der Eingabeaufforderung ein, `WSSQL.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für WSSQL.exe.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="conceptual"></a>Konzept

[Verwenden der Windows Search-SQL-Syntax](-search-sql-windowssearch-entry.md)

[Allgemeine Informationen zur Abfragesprache](-search-sql-generalqueryinfo.md)

[Übersicht über OLE DB Programmierung](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Weitere Beispiele

[Code Beispiele durchsuchen](-search-samples-ovw.md)
