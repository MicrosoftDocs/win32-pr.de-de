---
description: Wenn Sie eine registrierte Netzwerkschnittstellenkarte (NIC) auswählen, die auf einem lokalen Computer aufgeführt ist, können Sie einen filterblob verwenden, um die NICs zu ignorieren, an denen Sie nicht interessiert sind.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Angeben eines filterblobs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349021"
---
# <a name="specifying-a-filter-blob"></a>Angeben eines filterblobs

Wenn Sie eine registrierte Netzwerkschnittstellenkarte (NIC) auswählen, die auf einem lokalen Computer aufgeführt ist, können Sie einen [*filterblob*](f.md) verwenden, um die NICs zu ignorieren, an denen Sie nicht interessiert sind. Beispielsweise können Sie die Suche nach einem bestimmten Kartentyp (z. b. Ethernet) oder auf eine bestimmte MAC-Adresse einschränken.

Während der Suche nach einer NIC muss jeder Eintrag im filterblob mit einem entsprechenden Eintrag im NPP-BLOB übereinstimmen, der die NIC darstellt. Filterblobzeichen können auch [*spezielle blobzeichen*](s.md)sein.

Wenn die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufgerufen wird, schränkt das filterblob die im Dialogfeld " **Netzwerk auswählen** " angezeigten NICs ein. Wenn die [**getnppblobtable**](getnppblobtable.md) -Funktion aufgerufen wird, schränkt das filterblob die in der BLOB-Tabelle zurückgegebenen NICs ein.

Wenn Sie den Filter verwenden möchten, müssen Sie ein filterblob erstellen, die Werte der Eigenschaften festlegen, nach denen Sie filtern möchten (einschließlich aller speziellen BLOB-Einträge), und dann den blobfilter und einen Aufrufen der [**getnppblobtable**](getnppblobtable.md) -oder [**getnppblobfromui**](getnppblobfromui.md) -Funktion angeben.



| Für Informationen zu                                 | Siehe                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Auswählen einer auf einem lokalen Computer registrierten NIC | [Auswählen einer registrierten NIC](selecting-a-registered-nic.md)                                         |
| Abrufen einer NPP-BLOB-Tabelle                       | [Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



