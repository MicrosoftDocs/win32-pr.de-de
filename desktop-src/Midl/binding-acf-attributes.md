---
title: Binden von ACF-Attributen
description: Geben Sie an, wie der Client für Remote Prozedur Aufrufe mit den in der folgenden Tabelle aufgeführten Attributen eine Verbindung mit dem Server herstellt.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF-Mittell, Attribute, Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037360"
---
# <a name="binding-acf-attributes"></a><span data-ttu-id="efa0d-104">Binden von ACF-Attributen</span><span class="sxs-lookup"><span data-stu-id="efa0d-104">Binding ACF Attributes</span></span>

<span data-ttu-id="efa0d-105">Geben Sie an, wie der Client für Remote Prozedur Aufrufe mit den in der folgenden Tabelle aufgeführten Attributen eine Verbindung mit dem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="efa0d-105">Specify how the client connects to the server for remote procedure calls with the attributes listed in the following table.</span></span>



| <span data-ttu-id="efa0d-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="efa0d-106">Attribute</span></span>                                                          | <span data-ttu-id="efa0d-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="efa0d-107">Usage</span></span>                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efa0d-108">**async**</span><span class="sxs-lookup"><span data-stu-id="efa0d-108">**async**</span></span>](async.md)                                             | <span data-ttu-id="efa0d-109">Definiert ein Handle, das dem Aufrufer das Ausführen eines asynchronen Aufrufs ermöglicht und sofort zurückgegeben wird, ohne auf Ergebnisse zu warten</span><span class="sxs-lookup"><span data-stu-id="efa0d-109">Defines a handle that allows the caller to make an asynchronous call and return immediately without waiting for results, and then resynchronize with the called function to receive data after the call completes.</span></span> |
| [<span data-ttu-id="efa0d-110">**Automatisches \_ handle**</span><span class="sxs-lookup"><span data-stu-id="efa0d-110">**auto\_handle**</span></span>](auto-handle.md)                                | <span data-ttu-id="efa0d-111">Weist die-Klasse an, den Stub-Code das automatische Steuern der Bindung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="efa0d-111">Tells MIDL to let the stub code control the binding automatically.</span></span> <span data-ttu-id="efa0d-112">Dies ist die Standardeinstellung, wenn Sie kein Bindungs Handle angeben.</span><span class="sxs-lookup"><span data-stu-id="efa0d-112">This is the default if you don't specify any binding handle.</span></span>                                                                                    |
| [<span data-ttu-id="efa0d-113">**Kontext \_ handle \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="efa0d-113">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md) | <span data-ttu-id="efa0d-114">Gewährleistet, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung niemals serialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="efa0d-114">Guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>                                                                                                       |
| [<span data-ttu-id="efa0d-115">**Kontext \_ handle- \_ Serialisierung**</span><span class="sxs-lookup"><span data-stu-id="efa0d-115">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)     | <span data-ttu-id="efa0d-116">Gewährleistet, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung immer serialisiert wird</span><span class="sxs-lookup"><span data-stu-id="efa0d-116">Guarantees that a context handle will always be serialized, regardless of the application's default behavior</span></span>                                                                                                       |
| [<span data-ttu-id="efa0d-117">**explizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="efa0d-117">**explicit\_handle**</span></span>](explicit-handle.md)                        | <span data-ttu-id="efa0d-118">Ermöglicht es der Client Anwendung, die Bindung mit einem expliziten Parameter in den einzelnen Prozeduren zu steuern.</span><span class="sxs-lookup"><span data-stu-id="efa0d-118">Lets the client application control the binding with an explicit parameter in each procedure.</span></span>                                                                                                                      |
| [<span data-ttu-id="efa0d-119">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="efa0d-119">**implicit\_handle**</span></span>](implicit-handle.md)                        | <span data-ttu-id="efa0d-120">Gibt ein Handle für Prozeduren an, die keinen expliziten handle-Parameter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="efa0d-120">Specifies a handle for procedures that do not have an explicit handle parameter.</span></span> <span data-ttu-id="efa0d-121">Die Client Anwendung steuert die Bindung weiterhin.</span><span class="sxs-lookup"><span data-stu-id="efa0d-121">The client application still controls the binding.</span></span>                                                                                |
| [<span data-ttu-id="efa0d-122">**Strict- \_ Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="efa0d-122">**strict\_context\_handle**</span></span>](strict-context-handle.md)           | <span data-ttu-id="efa0d-123">Gewährleistet, dass die Methoden in der-Schnittstelle nur Kontext Handles akzeptieren, die von einer-Methode dieser Schnittstelle erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="efa0d-123">Guarantees that the methods in the interface will only accept context handles that were created by a method of that interface.</span></span>                                                                                     |



 

 

 




