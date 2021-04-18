---
title: Auf den Parameter angewendete direktionale Attribute
description: Die direktionalen Attribute \ in \ und \ out \ bestimmen, wie der Client und der Server Arbeitsspeicher zuordnen und freigeben. In der folgenden Tabelle werden die Auswirkungen der direktionalen Attribute auf die Speicher Belegung zusammengefasst.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340929"
---
# <a name="directional-attributes-applied-to-the-parameter"></a><span data-ttu-id="777d2-104">Auf den Parameter angewendete direktionale Attribute</span><span class="sxs-lookup"><span data-stu-id="777d2-104">Directional Attributes Applied to the Parameter</span></span>

<span data-ttu-id="777d2-105">Die direktionalen Attribute \[ [in](/windows/desktop/Midl/in) \] und \[ [out](/windows/desktop/Midl/out-idl) \] bestimmen, wie der Client und der Server Arbeitsspeicher zuordnen und freigeben.</span><span class="sxs-lookup"><span data-stu-id="777d2-105">The directional attributes \[ [in](/windows/desktop/Midl/in)\] and \[ [out](/windows/desktop/Midl/out-idl)\] determine how the client and server allocate and free memory.</span></span> <span data-ttu-id="777d2-106">In der folgenden Tabelle werden die Auswirkungen der direktionalen Attribute auf die Speicher Belegung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="777d2-106">The following table summarizes the effect of directional attributes on memory allocation.</span></span>



| <span data-ttu-id="777d2-107">Direktionales Attribut</span><span class="sxs-lookup"><span data-stu-id="777d2-107">Directional attribute</span></span>    | <span data-ttu-id="777d2-108">Arbeitsspeicher auf dem Client</span><span class="sxs-lookup"><span data-stu-id="777d2-108">Memory on client</span></span>                                                                                            | <span data-ttu-id="777d2-109">Arbeitsspeicher auf dem Server</span><span class="sxs-lookup"><span data-stu-id="777d2-109">Memory on server</span></span>                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="777d2-110">\[[in](/windows/desktop/Midl/in)\]</span><span class="sxs-lookup"><span data-stu-id="777d2-110">\[ [in](/windows/desktop/Midl/in)\]</span></span>       | <span data-ttu-id="777d2-111">Die Client Anwendung muss vor dem-Befehl zuordnen.</span><span class="sxs-lookup"><span data-stu-id="777d2-111">Client application must allocate before the call.</span></span>                                                           | <span data-ttu-id="777d2-112">Server-Stub zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="777d2-112">Server stub allocates.</span></span>                                                                                                                                  |
| <span data-ttu-id="777d2-113">\[[out](/windows/desktop/Midl/out-idl)\]</span><span class="sxs-lookup"><span data-stu-id="777d2-113">\[ [out](/windows/desktop/Midl/out-idl)\]</span></span> | <span data-ttu-id="777d2-114">Der Clientstub ordnet bei der Rückgabe zu.</span><span class="sxs-lookup"><span data-stu-id="777d2-114">Client stub allocates on return.</span></span>                                                                            | <span data-ttu-id="777d2-115">Der Serverstub weist nur Zeiger der obersten Ebene zu. die Serveranwendung muss alle eingebetteten Zeiger zuordnen.</span><span class="sxs-lookup"><span data-stu-id="777d2-115">Server stub allocates top-level pointer only; the server application must allocate all embedded pointers.</span></span> <span data-ttu-id="777d2-116">Der Server ordnet bei Bedarf auch neue Daten zu.</span><span class="sxs-lookup"><span data-stu-id="777d2-116">The server also allocates new data as needed.</span></span> |
| <span data-ttu-id="777d2-117">\[**in**, **out**\]</span><span class="sxs-lookup"><span data-stu-id="777d2-117">\[**in**, **out**\]</span></span>      | <span data-ttu-id="777d2-118">Die Client Anwendung muss die dem Server übertragenen anfänglichen Daten zuordnen. der Clientstub ordnet zusätzliche Daten zu.</span><span class="sxs-lookup"><span data-stu-id="777d2-118">Client application must allocate initial data transmitted to server; client stub allocates additional data.</span></span> | <span data-ttu-id="777d2-119">Der Serverstub ordnet anfängliche Daten zu, die vom Client gesendet werden. die Serveranwendung ordnet bei Bedarf neue Daten zu.</span><span class="sxs-lookup"><span data-stu-id="777d2-119">Server stub allocates initial data transmitted from client; the server application allocates new data as needed.</span></span>                                        |



 

<span data-ttu-id="777d2-120">In all diesen Fällen gibt der Clientstub keinen Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="777d2-120">In all of these cases the client stub does not free memory.</span></span> <span data-ttu-id="777d2-121">Die Client Anwendung muss den Arbeitsspeicher freigeben, bevor Sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="777d2-121">The client application must free the memory before it terminates.</span></span> <span data-ttu-id="777d2-122">Der Serverstub gibt Arbeitsspeicher frei, wenn der Remote Prozedur Rückruf zurückkehrt (unterliegt dem \[ [](/windows/desktop/Midl/allocate) \] ACF-Attribut "zuordnen").</span><span class="sxs-lookup"><span data-stu-id="777d2-122">The server stub frees memory when the remote procedure call returns (subject to the \[ [allocate](/windows/desktop/Midl/allocate)\] ACF attribute).</span></span>

 

 