---
description: ATM fällt in die Kategorie der Stammdaten und der rooting-steuerungsflächen.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: ATM Point to Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360040"
---
# <a name="atm-point-to-multipoint"></a><span data-ttu-id="1c53b-103">ATM Point to Multipoint</span><span class="sxs-lookup"><span data-stu-id="1c53b-103">ATM Point to Multipoint</span></span>

<span data-ttu-id="1c53b-104">ATM fällt in die Kategorie der Stammdaten und der rooting-steuerungsflächen.</span><span class="sxs-lookup"><span data-stu-id="1c53b-104">ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="1c53b-105">Eine Anwendung, die als Stamm fungiert, erstellt c \_ -Stamm Sockets, und Gegenstücke, die auf Blattknoten ausgeführt werden, würden c- \_ Blatt Sockets verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c53b-105">An application acting as the root would create c\_root sockets and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="1c53b-106">Die Stamm Anwendung verwendet [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) , um neue Blattknoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c53b-106">The root application uses [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="1c53b-107">Die entsprechenden Anwendungen auf den Blattknoten haben ihre c- \_ Blatt Sockets in den Abhör Modus festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c53b-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into listen mode.</span></span> <span data-ttu-id="1c53b-108">**Wsajoinleaf** mit einem angegebenen c-Stamm- \_ Socket wird der Q. 2931 addparty-Nachricht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1c53b-108">**WSAJoinLeaf** with a c\_root socket specified is mapped to the Q.2931 ADDPARTY message.</span></span> <span data-ttu-id="1c53b-109">Der Blatt initiierte Join wird in ATM Uni 3,1 nicht unterstützt, wird jedoch in ATM-Uni 4,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c53b-109">The leaf-initiated join is not supported in ATM UNI 3.1, but is supported in ATM UNI 4.0.</span></span> <span data-ttu-id="1c53b-110">Daher wird **wsajoinleaf** mit einem \_ angegebenen c-Blatt Socket der entsprechenden ATM-Uni 4,0-Nachricht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1c53b-110">Thus **WSAJoinLeaf** with a c\_leaf socket specified is mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="1c53b-111">Es gibt weitere Überlegungen, die Sie bei der Point-to-Multipoint-Funktion von ATM berücksichtigen sollten:</span><span class="sxs-lookup"><span data-stu-id="1c53b-111">There are additional considerations to bear in mind for ATM point-to-multipoint:</span></span>

-   <span data-ttu-id="1c53b-112">Das Hinzufügen neuer Blätter zur ATM-Point-to-Multipoint-Sitzung ist nur Einladungs basiert.</span><span class="sxs-lookup"><span data-stu-id="1c53b-112">The addition of new leaves to the ATM point-to-multipoint session is invitation-based only.</span></span> <span data-ttu-id="1c53b-113">Die Root-Einladungen erhalten –, die bereits ihren [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -Funktionsaufruf – haben, indem Sie die [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1c53b-113">The root invites leaves — which have already their [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function call — by calling the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="1c53b-114">Der Datenfluss in einer ATM-zu-Multipoint-Sitzung erfolgt nur von der Stamm-zu-Blätter-Sitzung. Blätter können nicht dieselbe Sitzung verwenden, um Informationen an den Stamm zu senden.</span><span class="sxs-lookup"><span data-stu-id="1c53b-114">The flow of data in an ATM point-to-multipoint session is from root-to-leaves only; leaves cannot use the same session to send information to the root.</span></span>
-   <span data-ttu-id="1c53b-115">Pro ATM-Adapter ist nur ein Blatt zulässig.</span><span class="sxs-lookup"><span data-stu-id="1c53b-115">Only one leaf per ATM adapter is allowed.</span></span>

 

 



