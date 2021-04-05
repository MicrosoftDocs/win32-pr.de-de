---
title: Verwenden von ADO für den Bereichs Abruf
description: Wenn eine Automatisierungs Sprache verwendet wird, sollte die ActiveX-Verzeichnisobjekte (ADO) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden. Wenn ADO für den Bereichs Abruf verwendet wird, besteht ein Problem, das speziell behandelt werden muss.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Verwenden von ADO für den Bereichs Abruf (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707367"
---
# <a name="using-ado-for-range-retrieval"></a>Verwenden von ADO für den Bereichs Abruf

Wenn eine Automatisierungs Sprache verwendet wird, sollte die ActiveX-Verzeichnisobjekte (ADO) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden.

Wenn ADO für den Bereichs Abruf verwendet wird, besteht ein Problem, das speziell behandelt werden muss. Beim Abfragen der endgültigen Gruppe von Eigenschafts Werten Ruft das ADO-Objekt NULL-Objekte ab, auch wenn mehr übrig sind. Um die restlichen Werte abzurufen, verwenden Sie den Bereichs Platzhalter " \* ". Wenn eine Gruppe z. b. 150 Mitglieder enthält, können die Mitglieds Werte 0-100 normalerweise mithilfe des Bereichs Abrufs abgerufen werden. Wenn der Bereich 101-200 dann angefordert wird, gibt das ADO-Objekt NULL-Objekte zurück. An diesem Punkt ist es erforderlich, die Abfrage in den Anforderungs Bereich 101-zu ändern \* . Dadurch werden Werte von 101 zu 150 abgerufen. Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode für die Verwendung von Bereichen zum Abrufen von Mitgliedern einer Gruppe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Weitere Informationen zur Verwendung von ADO für den Bereichs Abruf finden Sie unter:

-   [ADO LDAP-Bereich-Dialekt](ado-ldap-ranging-dialect.md)
-   [ADO-SQL-Bereich-Dialekt](ado-sql-ranging-dialect.md)
-   [Beispiel Code für die Verwendung von Bereichen zum Abrufen von Mitgliedern einer Gruppe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




