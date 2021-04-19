---
description: Im folgenden finden Sie eine Liste der lib-Dateien, die zum Kompilieren verschiedener TAPI 3-Anwendungen (ab 1/22/01) erforderlich sind.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Erforderliche Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350495"
---
# <a name="libraries-required"></a><span data-ttu-id="6a2ed-103">Erforderliche Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="6a2ed-103">Libraries Required</span></span>

<span data-ttu-id="6a2ed-104">Eine Liste von lib-Dateien, die erforderlich sind, um verschiedene TAPI 3-Anwendungen zu kompilieren, wie 1/22/01:</span><span class="sxs-lookup"><span data-stu-id="6a2ed-104">A list of .lib files required to compile various TAPI 3 applications, as of 1/22/01:</span></span>

-   <span data-ttu-id="6a2ed-105">Advapi32. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-105">Advapi32.lib</span></span>
-   <span data-ttu-id="6a2ed-106">Amstrinmid. lib (ActiveMovie-GUIDs)</span><span class="sxs-lookup"><span data-stu-id="6a2ed-106">Amstrmid.lib (ActiveMovie GUIDs)</span></span>
-   <span data-ttu-id="6a2ed-107">Kernel32.lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-107">Kernel32.lib</span></span>
-   <span data-ttu-id="6a2ed-108">Mdhcpid. lib (Multicast-GUIDs)</span><span class="sxs-lookup"><span data-stu-id="6a2ed-108">Mdhcpid.lib (multicast GUIDs)</span></span>
-   <span data-ttu-id="6a2ed-109">Ole32. lib (com)</span><span class="sxs-lookup"><span data-stu-id="6a2ed-109">Ole32.lib (COM)</span></span>
-   <span data-ttu-id="6a2ed-110">Oleaut32. lib (com-Automatisierung)</span><span class="sxs-lookup"><span data-stu-id="6a2ed-110">Oleaut32.lib (COM Automation)</span></span>
-   <span data-ttu-id="6a2ed-111">Rendid. lib (Rendezvous-GUIDs)</span><span class="sxs-lookup"><span data-stu-id="6a2ed-111">Rendid.lib (Rendezvous GUIDs)</span></span>
-   <span data-ttu-id="6a2ed-112">Rpcndr. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-112">Rpcndr.lib</span></span>
-   <span data-ttu-id="6a2ed-113">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-113">Rpcns4.lib</span></span>
-   <span data-ttu-id="6a2ed-114">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-114">Rpcrt4.lib</span></span>
-   <span data-ttu-id="6a2ed-115">Sdpblbid. lib (Sitzungs Deskriptor Protocol (SDP) GUIDs)</span><span class="sxs-lookup"><span data-stu-id="6a2ed-115">Sdpblbid.lib (Session Descriptor Protocol (SDP) GUIDs)</span></span>
-   <span data-ttu-id="6a2ed-116">"" "" ". Lib"</span><span class="sxs-lookup"><span data-stu-id="6a2ed-116">Strmiids.lib</span></span>
-   <span data-ttu-id="6a2ed-117">User32. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-117">User32.lib</span></span>
-   <span data-ttu-id="6a2ed-118">UUID. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-118">Uuid.lib</span></span>
-   <span data-ttu-id="6a2ed-119">Wldap32. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-119">Wldap32.lib</span></span>
-   <span data-ttu-id="6a2ed-120">Ws2 \_ 32. lib</span><span class="sxs-lookup"><span data-stu-id="6a2ed-120">Ws2\_32.lib</span></span>

<span data-ttu-id="6a2ed-121">Wenn Sie Microsoft Visual Studio verwenden, müssen Sie möglicherweise Ihre Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6a2ed-121">If you are using Microsoft Visual Studio, you may need to update your version.</span></span> <span data-ttu-id="6a2ed-122">Insbesondere muss Link.exe ein Datum von 3/19/98 oder höher aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6a2ed-122">In particular, Link.exe must carry a date of 3/19/98 or later.</span></span>

<span data-ttu-id="6a2ed-123">Compilerdefinitionen müssen \_ Win32 \_ Winnt enthalten, das auf mindestens 0x500 und \_ Win32 DCOM festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="6a2ed-123">Compiler defines must include \_WIN32\_WINNT set to at least 0x500 and \_WIN32\_DCOM.</span></span>

 

 



