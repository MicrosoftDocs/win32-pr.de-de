---
description: PGM verwendet Socketoptionen, um den Status festzulegen, Multicast Parameter bereitzustellen und anderweitig seine Multicast Funktionen zu implementieren.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: PGM-Socketoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862544"
---
# <a name="pgm-socket-options"></a><span data-ttu-id="21edf-103">PGM-Socketoptionen</span><span class="sxs-lookup"><span data-stu-id="21edf-103">PGM Socket Options</span></span>

<span data-ttu-id="21edf-104">PGM verwendet Socketoptionen, um den Status festzulegen, Multicast Parameter bereitzustellen und anderweitig seine Multicast Funktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="21edf-104">PGM uses socket options to set state, provide multicast parameters, and otherwise implement its multicast capabilities.</span></span> <span data-ttu-id="21edf-105">Diese Seite gibt an, wie PGM-Socketoptionen festgelegt werden sollen, listet die für PGM verfügbaren Socketoptionen auf und stellt Verwendungs Beispiele sowie zusätzliche Informationen für verschiedene Optionen bereit.</span><span class="sxs-lookup"><span data-stu-id="21edf-105">This page specifies how PGM socket options should be set, enumerates the socket options available for PGM, and where appropriate, provides usage examples and additional information for various options.</span></span> <span data-ttu-id="21edf-106">Grundlegende Definitionen der einzelnen PCM-Socketoptionen finden Sie unter [Socketoptionen](socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="21edf-106">For basic definitions of each PCM socket option, see [Socket Options](socket-options.md).</span></span>

<span data-ttu-id="21edf-107">**Windows XP:** Die zuverlässige Multicast Programmierung (PGM) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21edf-107">**Windows XP:** Reliable Multicast Programming (PGM) is not supported.</span></span>

<span data-ttu-id="21edf-108">Die folgenden Socketoptionen sind für PGM-Absender verfügbar:</span><span class="sxs-lookup"><span data-stu-id="21edf-108">The following socket options are available for PGM senders:</span></span>

<dl> <span data-ttu-id="21edf-109">RM- \_ latejoin</span><span class="sxs-lookup"><span data-stu-id="21edf-109">RM\_LATEJOIN</span></span>  
<span data-ttu-id="21edf-110">\_ \_ Fenster \_ Größe für RM-Rate</span><span class="sxs-lookup"><span data-stu-id="21edf-110">RM\_RATE\_WINDOW\_SIZE</span></span>  
<span data-ttu-id="21edf-111">\_ \_ \_ ADV- \_ Rate der RM-Sendefenster</span><span class="sxs-lookup"><span data-stu-id="21edf-111">RM\_SEND\_WINDOW\_ADV\_RATE</span></span>  
<span data-ttu-id="21edf-112">RM- \_ Absender \_ Statistik</span><span class="sxs-lookup"><span data-stu-id="21edf-112">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="21edf-113">vorab Methode des RM- \_ Absender \_ Fensters \_ \_</span><span class="sxs-lookup"><span data-stu-id="21edf-113">RM\_SENDER\_WINDOW\_ADVANCE\_METHOD</span></span>  
<span data-ttu-id="21edf-114">RM \_ - \_ mcast- \_ TTL festlegen</span><span class="sxs-lookup"><span data-stu-id="21edf-114">RM\_SET\_MCAST\_TTL</span></span>  
<span data-ttu-id="21edf-115">RM \_ Festlegen der \_ Nachrichten \_ Grenze</span><span class="sxs-lookup"><span data-stu-id="21edf-115">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="21edf-116">RM \_ Set \_ Send \_ if</span><span class="sxs-lookup"><span data-stu-id="21edf-116">RM\_SET\_SEND\_IF</span></span>  
<span data-ttu-id="21edf-117">RM- \_ Verwendung von \_ FEC</span><span class="sxs-lookup"><span data-stu-id="21edf-117">RM\_USE\_FEC</span></span>  
</dl>

<span data-ttu-id="21edf-118">Die Option für die erweiterte Methode des RM- \_ Sender \_ Fensters \_ gibt die Methode an, die \_ verwendet wird, wenn das nachfolgende Edge-Fenster</span><span class="sxs-lookup"><span data-stu-id="21edf-118">The RM\_SENDER\_WINDOW\_ADVANCE\_METHOD option specifies the method used when advancing the trailing edge send window.</span></span> <span data-ttu-id="21edf-119">Der optval-Parameter kann nur E \_ Fenster \_ vor \_ \_ der Zeit (Standard) sein.</span><span class="sxs-lookup"><span data-stu-id="21edf-119">The optval parameter can only be E\_WINDOW\_ADVANCE\_BY\_TIME (the default).</span></span> <span data-ttu-id="21edf-120">Beachten Sie, dass die E- \_ Window- \_ Verwendung \_ als \_ Daten \_ Cache nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="21edf-120">Note that E\_WINDOW\_USE\_AS\_DATA\_CACHE is not supported.</span></span>

<span data-ttu-id="21edf-121">Die folgenden Socketoptionen sind für PGM-Empfänger verfügbar:</span><span class="sxs-lookup"><span data-stu-id="21edf-121">The following socket options are available for PGM receivers:</span></span>

<dl> <span data-ttu-id="21edf-122">RM \_ Add \_ Receive \_ if</span><span class="sxs-lookup"><span data-stu-id="21edf-122">RM\_ADD\_RECEIVE\_IF</span></span>  
<span data-ttu-id="21edf-123">RM-ENTF \_ \_ empfangen, \_ Wenn</span><span class="sxs-lookup"><span data-stu-id="21edf-123">RM\_DEL\_RECEIVE\_IF</span></span>  
<span data-ttu-id="21edf-124">RM-Aktivierung mit \_ hoher \_ Geschwindigkeit im \_ Intranet \_</span><span class="sxs-lookup"><span data-stu-id="21edf-124">RM\_HIGH\_SPEED\_INTRANET\_OPT</span></span>  
<span data-ttu-id="21edf-125">RM- \_ Empfänger \_ Statistik</span><span class="sxs-lookup"><span data-stu-id="21edf-125">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

## <a name="setting-pgm-socket-options"></a><span data-ttu-id="21edf-126">Festlegen der PGM-Socketoptionen</span><span class="sxs-lookup"><span data-stu-id="21edf-126">Setting PGM Socket Options</span></span>

<span data-ttu-id="21edf-127">Der folgende Code Ausschnitt veranschaulicht eine Programmier Richtlinie zum Festlegen der PGM-Socketoptionen:</span><span class="sxs-lookup"><span data-stu-id="21edf-127">The following code snippet illustrates a programming guideline for setting PGM socket options:</span></span>


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



<span data-ttu-id="21edf-128">Im obigen Code Ausschnitt sind der Typ und der Inhalt von *optiondata* abhängig von der festgelegten Socketoption.</span><span class="sxs-lookup"><span data-stu-id="21edf-128">In the snippet above, the type and contents of *OptionData* are dependent on the socket option being set.</span></span> <span data-ttu-id="21edf-129">Bei allen PGM-Socketoptionen lautet die Socketebene ipproto \_ RM.</span><span class="sxs-lookup"><span data-stu-id="21edf-129">For all PGM socket options, the socket level is IPPROTO\_RM.</span></span> <span data-ttu-id="21edf-130">PGM-Socketoptionen müssen direkt nach dem Aufrufe der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion festgelegt werden, mit den folgenden Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="21edf-130">PGM socket options must be set immediately following the call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, with the following exceptions:</span></span>

<dl> <span data-ttu-id="21edf-131">RM \_ Festlegen der \_ Nachrichten \_ Grenze</span><span class="sxs-lookup"><span data-stu-id="21edf-131">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="21edf-132">RM- \_ Absender \_ Statistik</span><span class="sxs-lookup"><span data-stu-id="21edf-132">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="21edf-133">RM- \_ Empfänger \_ Statistik</span><span class="sxs-lookup"><span data-stu-id="21edf-133">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

 

 



