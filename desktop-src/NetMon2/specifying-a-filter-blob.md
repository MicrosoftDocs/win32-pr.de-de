---
description: Wenn Sie eine registrierte Netzwerkschnittstellenkarte (Network Interface Card, NIC) auswählen, die auf einem lokalen Computer aufgeführt ist, können Sie ein FilterBLOB verwenden, um die NICs zu ignorieren, an denen Sie nicht interessiert sind.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Angeben eines FilterBLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486a5dfe318da50a921560c92b82a3a3bf05a9434a4ac609b7f135afd7bf5a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555350"
---
# <a name="specifying-a-filter-blob"></a>Angeben eines FilterBLOBs

Wenn Sie eine registrierte Netzwerkschnittstellenkarte (Network Interface Card, NIC) auswählen, die auf einem lokalen Computer aufgeführt ist, können Sie ein FilterBLOB verwenden, um die NICs zu ignorieren, an denen Sie nicht interessiert sind. [](f.md) Beispielsweise können Sie die Suche nach einem bestimmten Kartentyp (z. B. ETHERNET) oder einer bestimmten MAC-Adresse einschränken.

Während der Suche nach einer NIC muss jeder Eintrag im FilterBLOB mit einem entsprechenden Eintrag im NPP-BLOB übereinstimmen, der die NIC darstellt. Filterblobs können auch spezielle [*BLOBs sein.*](s.md)

Wenn die [**GetNPPBlobFromUI-Funktion**](getnppblobfromui.md) aufgerufen wird, schränkt das FilterBLOB die NICs ein, die im Dialogfeld **Netzwerk auswählen** angezeigt werden. Wenn die [**GetNPPBlobTable-Funktion**](getnppblobtable.md) aufgerufen wird, schränkt das FilterBLOB die niCs ein, die in der BLOB-Tabelle zurückgegeben werden.

Um den Filter zu verwenden, müssen Sie ein Filterblob erstellen, die Werte der Eigenschaften festlegen, nach denen Sie filtern möchten (einschließlich spezieller BLOB-Einträge), und dann den BLOB-Filter und einen Aufruf der [**GetNPPBlobTable-**](getnppblobtable.md) oder [**GetNPPBlobFromUI-Funktion**](getnppblobfromui.md) angeben.



| Für Informationen zu                                 | Siehe                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Auswählen einer auf einem lokalen Computer registrierten NIC | [Auswählen einer registrierten NIC](selecting-a-registered-nic.md)                                         |
| Abrufen einer NPP-BLOB-Tabelle                       | [Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



