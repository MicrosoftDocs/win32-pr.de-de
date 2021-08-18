---
title: Verwenden von ADO für den Bereichsabruf
description: Wenn eine Automatisierungssprache verwendet wird, sollte die ActiveX Directory Objects (ADO) verwendet werden, um einen Bereich von Eigenschaftswerten abzurufen. Wenn Sie ADO für den Bereichsabruf verwenden, gibt es ein Problem, das speziell behoben werden muss.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Verwenden von ADO für Range Retrieval ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523cd65e7d26a82b9b647913c919bef374b1c76ddf1a18fd9f99384b4ae6e483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023048"
---
# <a name="using-ado-for-range-retrieval"></a>Verwenden von ADO für den Bereichsabruf

Wenn eine Automatisierungssprache verwendet wird, sollte die ActiveX Directory Objects (ADO) verwendet werden, um einen Bereich von Eigenschaftswerten abzurufen.

Wenn Sie ADO für den Bereichsabruf verwenden, gibt es ein Problem, das speziell behoben werden muss. Beim Abfragen der endgültigen Gruppe von Eigenschaftswerten ruft das ADO-Objekt 0 Objekte ab, auch wenn mehr verbleiben. Um die verbleibenden Werte abzurufen, verwenden Sie den Bereichs-Platzhalter " \* "". Wenn eine Gruppe beispielsweise 150 Elemente enthält, können die Elementwerte 0 bis 100 mithilfe des Bereichsabrufs normal abgerufen werden. Wenn dann der Bereich 101 bis 200 angefordert wird, gibt das ADO-Objekt null Objekte zurück. An diesem Punkt ist es erforderlich, die Abfrage so zu ändern, dass der Bereich 101– angefordert \* wird. Dadurch werden Werte zwischen 101 und 150 abgerufen. Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode für die Verwendung von Ranging zum Abrufen von Mitgliedern einer Gruppe.](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

Weitere Informationen zur Verwendung von ADO für den Bereichsabruf finden Sie unter:

-   [ADO LDAP Ranging Dialect](ado-ldap-ranging-dialect.md)
-   [ADO SQL Ranging Dialect](ado-sql-ranging-dialect.md)
-   [Beispielcode für die Verwendung von Ranging zum Abrufen von Mitgliedern einer Gruppe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




