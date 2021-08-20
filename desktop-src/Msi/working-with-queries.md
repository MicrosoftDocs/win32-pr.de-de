---
description: Da das Installationsprogramm eine relationale Datenbank verwendet, gibt es Funktionen zum Strukturierte Abfragesprache (SQL) Abfragen an die Datenbank. Im folgenden Verfahren wird beschrieben, wie sie SQL datenbankabfragen.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Arbeiten mit Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b6ea5a2f0b962b195fde531216f4b57fd5834162e31c1e34fc9ff1dd3695df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942125"
---
# <a name="working-with-queries"></a>Arbeiten mit Abfragen

Da das Installationsprogramm eine relationale Datenbank verwendet, gibt es Funktionen zum Strukturierte Abfragesprache (SQL) Abfragen an die Datenbank. Im folgenden Verfahren wird beschrieben, wie sie SQL datenbankabfragen.

**So fragen Sie eine Datenbank mit SQL**

1.  Öffnen Sie [**das View-Objekt**](view-object.md) mit der entsprechenden SQL, indem Sie die [**MsiDatabaseOpenView-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) aufrufen.

    Ein [**View-Objekt**](view-object.md) ist die logische Tabelle, die durch Anwenden einer Abfrage auf eine Gruppe von Tabellen erstellt wird. SQL Abfragen müssen der vom Installationsprogramm [SQL](sql-syntax.md) Syntax entsprechen. Diese SQL-Anweisung kann Parametermarkierungen enthalten, die erst angegeben werden, wenn das **View-Objekt** ausgeführt wird.

2.  Führen Sie das [**View-Objekt**](view-object.md) aus, indem Sie die [**MsiViewExecute-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) aufrufen.
3.  Rufen Sie den nächsten Datensatz aus einem [**View-Objekt ab,**](view-object.md) indem Sie die [**MsiViewFetch-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) aufrufen.
4.  Ändern Sie das [**View-Objekt,**](view-object.md) indem Sie die [**MsiViewModify-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) aufrufen.

    Sie können Daten auch mit [**MsiViewModify überprüfen,**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) indem Sie die entsprechenden Flags übergeben. Wenn **MsiViewModify** ERROR \_ INVALID DATA aus einer \_ Validierungsanforderung zurückgibt, sind die zugrunde liegenden Daten beschädigt.

5.  Rufen Sie ausführliche Fehlerinformationen zum [**View-Objekt ab,**](view-object.md) indem Sie die [**MsiViewGetError-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) aufrufen.
6.  Schließen [](view-object.md) Sie das View-Objekt, indem Sie die [**MsiViewClose-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) aufrufen.

Weitere Informationen finden Sie unter [Beispiele für Datenbankabfragen mit SQL und Skript](examples-of-database-queries-using-sql-and-script.md).

 

 



