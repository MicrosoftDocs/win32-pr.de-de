---
description: Basierend auf der Taxonomie, die für Protokoll unabhängige Multipoint-/Multicast Schemas von Windows Sockets 2 definiert ist, fällt ATM in die Kategorie der Stammdaten und der Stamm steuerungsflächen.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Details der Winsock-ATM-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130405"
---
# <a name="winsock-atm-function-details"></a><span data-ttu-id="50f80-103">Details der Winsock-ATM-Funktion</span><span class="sxs-lookup"><span data-stu-id="50f80-103">Winsock ATM Function Details</span></span>

<span data-ttu-id="50f80-104">Basierend auf der Taxonomie, die für Protokoll unabhängige Multipoint-/Multicast Schemas von Windows Sockets 2 definiert ist, fällt ATM in die Kategorie der Stammdaten und der Stamm steuerungsflächen.</span><span class="sxs-lookup"><span data-stu-id="50f80-104">Based on the taxonomy defined for Windows Sockets 2 protocol-independent multipoint/multicast schemes, ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="50f80-105">(Weitere Informationen finden Sie in der API-Spezifikation von Windows Sockets 2 (Anhang D).) Eine Anwendung, die als Stamm fungiert, würde c \_ -stammsockets erstellen, und Gegenstücke, die auf Blattknoten ausgeführt werden, würden c- \_ Blatt Sockets verwenden.</span><span class="sxs-lookup"><span data-stu-id="50f80-105">(See the Windows Sockets 2 API Specification, Appendix D for more information.) An application acting as the root would create c\_root sockets, and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="50f80-106">Die Stamm Anwendung verwendet [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) , um neue Blattknoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="50f80-106">The root application will use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="50f80-107">Die entsprechenden Anwendungen auf den Blattknoten haben ihre c- \_ Blatt-Sockets in den Empfangsmodus festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50f80-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into the listening mode.</span></span> <span data-ttu-id="50f80-108">**Wsajoinleaf** mit einem angegebenen c-Stamm- \_ Socket wird der Q. 2931-Setup Nachricht (für das erste Blatt) oder der Nachricht zum Hinzufügen von Parteien (für nachfolgende Blätter) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="50f80-108">**WSAJoinLeaf** with a c\_root socket specified will be mapped to the Q.2931 SETUP message (for the first leaf) or ADD PARTY message (for any subsequent leaves).</span></span>

> [!Note]  
> <span data-ttu-id="50f80-109">Die in **wsajoinleaf** angegebenen QoS-Parameter für nachfolgende Blätter sollten gemäß der Uni-Spezifikation des ATM-Forums ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="50f80-109">The QoS parameters specified in **WSAJoinLeaf** for any subsequent leaves should be ignored per the ATM Forum UNI specification.</span></span>

 

<span data-ttu-id="50f80-110">Der Blatt initiierte Join ist nicht Teil der ATM-Uni 3,1, wird jedoch in der ATM-Uni 4,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50f80-110">The leaf-initiated join is not part of the ATM UNI 3.1, but is supported in the ATM UNI 4.0.</span></span> <span data-ttu-id="50f80-111">Daher kann [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) mit einem \_ angegebenen c-Blatt Socket der entsprechenden ATM-Uni 4,0-Nachricht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="50f80-111">Thus [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) with a c\_leaf socket specified can be mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="50f80-112">Der Aal-Parameter und die B-lli-Aushandlung werden durch die Änderung der entsprechenden IES im *lpsqos* -Parameter nach dem Aufruf der in [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)angegebenen Bedingungs Funktion unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50f80-112">The AAL Parameter and B-LLI negotiation is supported through the modification of the corresponding IEs in the *lpSQOS* parameter upon the invocation of the condition function specified in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span></span>

> [!Note]  
> <span data-ttu-id="50f80-113">Nur bestimmte Felder in diesen beiden IES können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="50f80-113">Only certain fields in those two IEs can be modified.</span></span> <span data-ttu-id="50f80-114">Weitere Informationen finden Sie im ATM-Forum in der Uni-Spezifikation Anhang C und Anhang F.</span><span class="sxs-lookup"><span data-stu-id="50f80-114">See the ATM Forum UNI specification Appendix C and Appendix F for details.</span></span>

 

 

 



