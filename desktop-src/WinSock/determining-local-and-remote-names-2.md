---
description: Wspgetsockname wird verwendet, um die lokale Adresse für gebundene Sockets abzurufen.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Bestimmen von lokalen und Remote Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041732"
---
# <a name="determining-local-and-remote-names"></a><span data-ttu-id="248ed-103">Bestimmen von lokalen und Remote Namen</span><span class="sxs-lookup"><span data-stu-id="248ed-103">Determining Local and Remote Names</span></span>

<span data-ttu-id="248ed-104">[**Wspgetsockname**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) wird verwendet, um die lokale Adresse für gebundene Sockets abzurufen.</span><span class="sxs-lookup"><span data-stu-id="248ed-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) is used to retrieve the local address for bound sockets.</span></span> <span data-ttu-id="248ed-105">Dies ist besonders nützlich, wenn ein [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) -Befehl ausgeführt wurde, ohne zuerst [**wspbind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) durchgeführt zu haben. **Wspgetsockname** stellt die einzige Möglichkeit dar, die lokale Zuordnung zu bestimmen, die vom Anbieter implizit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="248ed-105">This is especially useful when a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) call has been made without doing a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) first; **WSPGetSockName** provides the only means to determine the local association which has been set implicitly by the provider.</span></span>

<span data-ttu-id="248ed-106">Nachdem eine Verbindung eingerichtet wurde, kann [**wspgetpeername**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) verwendet werden, um die Adresse des Peers zu ermitteln, mit dem ein Socket verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="248ed-106">After a connection has been set up, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) can be used to determine the address of the peer to which a socket is connected.</span></span>

 

 
