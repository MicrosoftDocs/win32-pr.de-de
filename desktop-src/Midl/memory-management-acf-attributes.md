---
title: ACF-Attribute für die Speicherverwaltung
description: Mithilfe der in der folgenden Tabelle aufgeführten Attribute können Sie die Arbeitsspeicher Verwaltung von der Clientseite aus durchführen.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF-Mittell, Attribute, Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948686"
---
# <a name="memory-management-acf-attributes"></a><span data-ttu-id="0af31-104">ACF-Attribute für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="0af31-104">Memory Management ACF Attributes</span></span>

<span data-ttu-id="0af31-105">Mithilfe der in der folgenden Tabelle aufgeführten Attribute können Sie die Arbeitsspeicher Verwaltung von der Clientseite aus durchführen.</span><span class="sxs-lookup"><span data-stu-id="0af31-105">The attributes listed in the following table enable you to perform memory management from the client side.</span></span>



| <span data-ttu-id="0af31-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="0af31-106">Attribute</span></span>                                   | <span data-ttu-id="0af31-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0af31-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0af31-108">**allocate**</span><span class="sxs-lookup"><span data-stu-id="0af31-108">**allocate**</span></span>](allocate.md)                | <span data-ttu-id="0af31-109">Gibt an, wie die Client Anwendung und der Stub Speicher für Zeiger zuweisen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="0af31-109">Specifies the way the client application and stub allocate and release memory for pointers.</span></span> <span data-ttu-id="0af31-110">Dieses Attribut ist besonders nützlich, wenn Sie möchten, dass bestimmte Zeiger Strukturen für die Serveranwendung zugänglich bleiben, nachdem der Remote Prozedur Aufruf an den Client zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0af31-110">This attribute is particularly useful when you want certain pointer structures to remain accessible to the server application after the remote procedure call returns to the client.</span></span> <span data-ttu-id="0af31-111">Sie können auch das Attribut " [**zuordnen**](allocate.md) " verwenden, um den Stub anzuweisen, die Größe des gesamten Speichers zu berechnen, auf den über den Zeiger des angegebenen Typs verwiesen wird, und einen einzelnen aufzurufenden [**Mittel l- \_ Benutzer \_ zuzuordnen**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="0af31-111">You can also use the [**allocate**](allocate.md) attribute to direct the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span> |
| [<span data-ttu-id="0af31-112">**Byte \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="0af31-112">**byte\_count**</span></span>](byte-count.md)           | <span data-ttu-id="0af31-113">Ermöglicht es Ihnen, einen permanenten, zusammenhängenden Speicherblock zu erstellen, der über mehrere Remote Prozedur Aufrufe wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0af31-113">Enables you to create a persistent, contiguous block of memory that can be reused over multiple remote procedure calls.</span></span> <span data-ttu-id="0af31-114">Dadurch wird die Client Anwendung vom mehr Aufwand für das wiederholte Zuweisen und Freigeben von Arbeitsspeicher, der mehrere Zeiger und andere komplexe Datenstrukturen enthalten kann, freigegeben.</span><span class="sxs-lookup"><span data-stu-id="0af31-114">This frees the client application from the overhead of repeatedly allocating and releasing memory that may include multiple pointers and other complex data structures.</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="0af31-115">**\_zuordnen aktivieren**</span><span class="sxs-lookup"><span data-stu-id="0af31-115">**enable\_allocate**</span></span>](enable-allocate.md) | <span data-ttu-id="0af31-116">Gibt an, dass der Serverstub-Code die Stub-Speicher Verwaltungs Umgebung aktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="0af31-116">Specifies that the server stub code should enable the stub memory-management environment.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 