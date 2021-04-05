---
title: Gemeinsame Nutzung der Internetverbindung
description: Mit Bits kann eine DFÜ-Verbindung für Heimnetzwerke erzwungen werden, die die Freigabe von Microsoft-Internet Verbindungen verwenden, wenn die Verbindungs Freigabe so konfiguriert ist, dass die Computer im Netzwerk auf das Internet zugreifen.
ms.assetid: a0a05ddb-6ce4-4cf5-8953-cb7122702d17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f92538f0317ac1b198b69069c4041c562ce368c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707841"
---
# <a name="internet-connection-sharing"></a><span data-ttu-id="bdd6d-103">Gemeinsame Nutzung der Internetverbindung</span><span class="sxs-lookup"><span data-stu-id="bdd6d-103">Internet Connection Sharing</span></span>

<span data-ttu-id="bdd6d-104">Mit Bits kann eine DFÜ-Verbindung für Heimnetzwerke erzwungen werden, die die Freigabe von Microsoft-Internet Verbindungen verwenden, wenn die Verbindungs Freigabe so konfiguriert ist, dass die Computer im Netzwerk auf das Internet zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bdd6d-104">BITS can force a dial-up connection for home networks that use Microsoft Internet Connection Sharing if Connection Sharing is configured to dial out when computers on the network access the Internet.</span></span> <span data-ttu-id="bdd6d-105">Um eine erzwungene DFÜ-Verbindung zu verhindern, deaktivieren Sie die Option eine DFÜ **-Verbindung herstellen, wenn ein Computer in meinem Netzwerk versucht** , auf die Option Internet auf dem Verbindungs Freigabe Host Computer zuzugreifen, der die Internetverbindung gemeinsam nutzt.</span><span class="sxs-lookup"><span data-stu-id="bdd6d-105">To prevent a forced dial-up connection, disable the **Establish a dial-up connection whenever a computer on my network attempts to access the Internet** option on the Connection Sharing host computer that shares its Internet connection.</span></span>

<span data-ttu-id="bdd6d-106">Für Computer, die mit dem Verbindungs Freigabe-Host Computer verbunden sind, wird angenommen, dass Sie über eine Netzwerkverbindung verfügen</span><span class="sxs-lookup"><span data-stu-id="bdd6d-106">Computers connected to the Connection Sharing host computer assume they have a network connection, so BITS will try to transfer files.</span></span> <span data-ttu-id="bdd6d-107">Wenn die DFÜ-Option auf dem Host Computer deaktiviert ist und der Host Computer nicht über eine aktive Verbindung verfügt, tritt bei der Übertragung ein vorübergehender Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bdd6d-107">If the dial-up option is disabled on the host computer and the host computer does not have an active connection, the transfers will fail with a transient error.</span></span> <span data-ttu-id="bdd6d-108">Bits führt die Übertragungen regelmäßig wiederholt aus.</span><span class="sxs-lookup"><span data-stu-id="bdd6d-108">BITS will retry the transfers periodically.</span></span>

 

 




