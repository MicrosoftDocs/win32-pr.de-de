---
description: Um eine der auf dem lokalen Computer registrierten NICs auszuwählen, müssen Sie die getnppblobfromui-Funktion aufrufen.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Auswählen einer registrierten NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367863"
---
# <a name="selecting-a-registered-nic"></a>Auswählen einer registrierten NIC

Um eine der auf dem lokalen Computer registrierten NICs auszuwählen, müssen Sie die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufrufen. Diese Funktion verwendet die Netzwerkmonitor-Benutzeroberfläche, um die registrierten NICs anzuzeigen, und gibt das NPP-BLOB zurück, das die ausgewählte NIC darstellt. Sie können alle auf dem lokalen Computer registrierten NICs oder einen kleineren Satz gefilterter NICs anzeigen. Wenn Sie die angezeigten NICs filtern möchten, geben Sie einen [*filterblob*](f.md) an, wenn der-Befehl aufgerufen wird.

> [!Note]  
> Wenn die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufgerufen wird, kommuniziert der [*NPP-Finder*](n.md) mit den NPP-DLLs, um die NPP-BLOB-Strukturen abzurufen, die die registrierten NICs darstellen. Weitere Informationen und eine Vorgehensweise zur direkten Verwendung der Netzwerkmonitor-Benutzeroberfläche finden Sie im Thema "Auswählen eines Netzwerks" in der Netzwerkmonitor-Online Hilfe.

 

Wenn Sie die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufrufen, wird das Dialogfeld **Netzwerk auswählen** angezeigt. Darin können Sie die Details der NPPs anzeigen, die auf dem lokalen Computer registriert sind. Diese Informationen umfassen sowohl lokale NPPs als auch Remote-NPPs. Im Dialogfeld können Sie eine bestimmte NIC auswählen und die Details der zugehörigen NPP-BLOB-Struktur anzeigen.

In der folgenden Abbildung werden typische Einstellungen eines NDIS-NPP dargestellt, der von Netzwerkmonitor bereitgestellt wird.

![typische Einstellungen eines vom Netzwerkmonitor bereitgestellten NDIS-NPP](images/networkdb.png)

In der folgenden Tabelle sind Themen aufgeführt, in denen jede NIC-Auswahlmethode beschrieben wird.



| Informationen über                                                                          | Finden Sie unter                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Gibt an, wie ein Filter angegeben wird, der die im Dialogfeld " **Netzwerk auswählen** " angezeigten NICs einschränkt. | [Angeben eines filterblobs](specifying-a-filter-blob.md)                                             |
| So wählen Sie eine NIC aus, indem Sie die [**getnppblobfromui**](getnppblobfromui.md) -Funktion aufrufen.      | [Auswählen einer NIC mithilfe von getnppblobfromui](getnppblobfromui.md)                                       |
| Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle.                                            | [Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



