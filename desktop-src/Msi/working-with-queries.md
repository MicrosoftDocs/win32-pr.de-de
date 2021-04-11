---
description: Da das Installationsprogramm eine relationale Datenbank verwendet, gibt es Funktionen zum Erstellen von Structured Query Language (SQL)-Abfragen an die Datenbank. Im folgenden Verfahren wird beschrieben, wie Sie SQL zum Abfragen einer Datenbank verwenden.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Arbeiten mit Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959976"
---
# <a name="working-with-queries"></a>Arbeiten mit Abfragen

Da das Installationsprogramm eine relationale Datenbank verwendet, gibt es Funktionen zum Erstellen von Structured Query Language (SQL)-Abfragen an die Datenbank. Im folgenden Verfahren wird beschrieben, wie Sie SQL zum Abfragen einer Datenbank verwenden.

**So Fragen Sie eine Datenbank mit SQL ab**

1.  Öffnen Sie das [**View**](view-object.md) -Objekt mit der entsprechenden SQL-Anweisung, indem Sie die [**msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) -Funktion aufrufen.

    Ein [**View**](view-object.md) -Objekt ist die logische Tabelle, die durch Anwenden einer Abfrage auf einen Tabellen Satz erstellt wird. SQL-Abfragen müssen der vom Installationsprogramm bereitgestellten [SQL-Syntax](sql-syntax.md) entsprechen. Diese SQL-Anweisung kann Parameter Markierungen enthalten, die nicht angegeben sind, bis das **View** -Objekt ausgeführt wird.

2.  Führen Sie das [**View**](view-object.md) -Objekt aus, indem Sie die [**msiviewexecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) -Funktion aufrufen.
3.  Rufen Sie den nächsten Datensatz aus einem [**Ansichts**](view-object.md) Objekt ab, indem Sie die [**msiviewfetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) -Funktion aufrufen.
4.  Ändern Sie das [**Ansichts**](view-object.md) Objekt, indem Sie die [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) -Funktion aufrufen.

    Sie können auch Daten mit [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) validieren, indem Sie die entsprechenden Flags übergeben. Wenn **msiviewmodify** \_ ungültige \_ Daten aus einer Validierungs Anforderung zurückgibt, sind die zugrunde liegenden Daten beschädigt.

5.  Rufen Sie ausführliche Fehlerinformationen zum [**View**](view-object.md) -Objekt ab, indem Sie die [**msiviewgeterror**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) -Funktion aufrufen.
6.  Schließen Sie das [**Ansichts**](view-object.md) Objekt, indem Sie die [**msiviewclose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) -Funktion aufrufen.

Weitere Informationen finden Sie unter [Beispiele für Datenbankabfragen mit SQL und Skript](examples-of-database-queries-using-sql-and-script.md).

 

 



