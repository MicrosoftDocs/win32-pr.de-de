---
description: Bevor ein Socket verwendet werden kann, um eine Verbindung einzurichten oder eine Verbindungsanforderung zu empfangen, muss er an eine lokale Adresse gebunden werden.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Binden an eine lokale Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348394"
---
# <a name="binding-to-a-local-address"></a><span data-ttu-id="dd688-103">Binden an eine lokale Adresse</span><span class="sxs-lookup"><span data-stu-id="dd688-103">Binding to a Local Address</span></span>

<span data-ttu-id="dd688-104">Bevor ein Socket verwendet werden kann, um eine Verbindung einzurichten oder eine Verbindungsanforderung zu empfangen, muss er an eine lokale Adresse gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="dd688-104">Before a socket can be used to set up a connection or receive a connection request, it needs to be bound to a local address.</span></span> <span data-ttu-id="dd688-105">Dies kann explizit durch Aufrufen von [**wspbind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))oder implizit durch [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) erfolgen, wenn der Socket beim Aufrufen dieser Funktion nicht gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="dd688-105">This could be done explicitly by calling [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), or implicitly by [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) if the socket is unbound when this function is called.</span></span>

 

 
