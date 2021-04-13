---
title: Kommunikation zwischen NAP-Client und Server seitiger Komponente
description: Kommunikation zwischen NAP-Client und Server seitiger Komponente
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388657"
---
# <a name="nap-client-and-server-side-component-communication"></a><span data-ttu-id="c66b3-103">Kommunikation zwischen NAP-Client und Server seitiger Komponente</span><span class="sxs-lookup"><span data-stu-id="c66b3-103">NAP Client and Server-side Component Communication</span></span>

> [!Note]  
> <span data-ttu-id="c66b3-104">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c66b3-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c66b3-105">Die NAP-Agent-Komponente kann über den folgenden Prozess mit der NAP-Verwaltungs Server Komponente kommunizieren:</span><span class="sxs-lookup"><span data-stu-id="c66b3-105">The NAP Agent component can communicate with the NAP Administration Server component through the following process:</span></span>

1.  <span data-ttu-id="c66b3-106">Der NAP-Agent übergibt die SSOH an die NAP ec.</span><span class="sxs-lookup"><span data-stu-id="c66b3-106">The NAP Agent passes the SSoH to the NAP EC.</span></span>
2.  <span data-ttu-id="c66b3-107">Der NAP EC übergibt die SSOH an die NAP es.</span><span class="sxs-lookup"><span data-stu-id="c66b3-107">The NAP EC passes the SSoH to the NAP ES.</span></span>
3.  <span data-ttu-id="c66b3-108">Der NAP es übergibt die SSOH an den Netzwerk Richtlinien Server (NPS)-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c66b3-108">The NAP ES passes the SSoH to the Network Policy Server (NPS) service.</span></span>
4.  <span data-ttu-id="c66b3-109">Der NPS-Dienst übergibt die SSOH an den NAP-Verwaltungs Server.</span><span class="sxs-lookup"><span data-stu-id="c66b3-109">The NPS service passes the SSoH to the NAP Administration Server.</span></span>

<span data-ttu-id="c66b3-110">Ein SHA kann über den folgenden Prozess mit dem entsprechenden SHV kommunizieren:</span><span class="sxs-lookup"><span data-stu-id="c66b3-110">An SHA can communicate with its corresponding SHV through the following process:</span></span>

1.  <span data-ttu-id="c66b3-111">Der SHA übergibt seine SoH an den NAP-Agent.</span><span class="sxs-lookup"><span data-stu-id="c66b3-111">The SHA passes its SoH to the NAP Agent.</span></span>
2.  <span data-ttu-id="c66b3-112">Der NAP-Agent übergibt das SoH, das in SSOH enthalten ist, an die NAP ec.</span><span class="sxs-lookup"><span data-stu-id="c66b3-112">The NAP Agent passes the SoH, contained within the SSoH, to the NAP EC.</span></span>
3.  <span data-ttu-id="c66b3-113">Der NAP EC übergibt das SoH an die NAP es.</span><span class="sxs-lookup"><span data-stu-id="c66b3-113">The NAP EC passes the SoH to the NAP ES.</span></span>
4.  <span data-ttu-id="c66b3-114">Der NAP es übergibt das SoH an den NAP-Verwaltungs Server.</span><span class="sxs-lookup"><span data-stu-id="c66b3-114">The NAP ES passes the SoH to the NAP Administration Server.</span></span>
5.  <span data-ttu-id="c66b3-115">Der NAP-Verwaltungs Server übergibt das SoH an den SHV.</span><span class="sxs-lookup"><span data-stu-id="c66b3-115">The NAP Administration Server passes the SoH to the SHV.</span></span>

<span data-ttu-id="c66b3-116">Die folgende Abbildung zeigt den Kommunikationsprozess von NAP-Client Komponenten mit NAP-serverseitigen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c66b3-116">The figure below shows the communication process from NAP client components to NAP server-side components.</span></span>

![Architektur der Kommunikation zwischen Client und Server auf der NAP-Plattform](images/nap-client-to-server-comm.png)

<span data-ttu-id="c66b3-118">Der NAP-Verwaltungs Server kann über den folgenden Prozess mit dem NAP-Agent kommunizieren:</span><span class="sxs-lookup"><span data-stu-id="c66b3-118">The NAP Administration Server can communicate with the NAP Agent through the following process:</span></span>

1.  <span data-ttu-id="c66b3-119">Der NAP-Verwaltungs Server übergibt die sostd an den NPS-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c66b3-119">The NAP Administration Server passes the SoHRs to the NPS service.</span></span>
2.  <span data-ttu-id="c66b3-120">Der NPS-Dienst übergibt die SSoHR an den NAP es.</span><span class="sxs-lookup"><span data-stu-id="c66b3-120">The NPS service passes the SSoHR to the NAP ES.</span></span>
3.  <span data-ttu-id="c66b3-121">Der NAP es übergibt die SSoHR an die NAP ec.</span><span class="sxs-lookup"><span data-stu-id="c66b3-121">The NAP ES passes the SSoHR to the NAP EC.</span></span>
4.  <span data-ttu-id="c66b3-122">Der NAP EC übergibt die SSoHR an den NAP-Agent.</span><span class="sxs-lookup"><span data-stu-id="c66b3-122">The NAP EC passes the SSoHR to the NAP Agent.</span></span>

<span data-ttu-id="c66b3-123">Der SHV kann mit dem entsprechenden SHA über den folgenden Prozess kommunizieren:</span><span class="sxs-lookup"><span data-stu-id="c66b3-123">The SHV can communicate with its corresponding SHA through the following process:</span></span>

1.  <span data-ttu-id="c66b3-124">Der SHV übergibt seine Sohr an den NAP-Verwaltungs Server.</span><span class="sxs-lookup"><span data-stu-id="c66b3-124">The SHV passes its SoHR to the NAP Administration Server.</span></span>
2.  <span data-ttu-id="c66b3-125">Der NAP-Verwaltungs Server übergibt die Sohr an den NPS-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c66b3-125">The NAP Administration Server passes the SoHR to the NPS service.</span></span>
3.  <span data-ttu-id="c66b3-126">Der NPS-Dienst übergibt die im SSoHR enthaltene Sohr an die NAP es.</span><span class="sxs-lookup"><span data-stu-id="c66b3-126">The NPS service passes the SoHR, contained within the SSoHR, to the NAP ES.</span></span>
4.  <span data-ttu-id="c66b3-127">Der NAP es übergibt die Sohr an die NAP ec.</span><span class="sxs-lookup"><span data-stu-id="c66b3-127">The NAP ES passes the SoHR to the NAP EC.</span></span>
5.  <span data-ttu-id="c66b3-128">Der NAP EC übergibt die Sohr an den NAP-Agent.</span><span class="sxs-lookup"><span data-stu-id="c66b3-128">The NAP EC passes the SoHR to the NAP Agent.</span></span>
6.  <span data-ttu-id="c66b3-129">Der NAP-Agent übergibt die Sohr an den SHA.</span><span class="sxs-lookup"><span data-stu-id="c66b3-129">The NAP Agent passes the SoHR to the SHA.</span></span>

<span data-ttu-id="c66b3-130">Die folgende Abbildung zeigt den Kommunikationsprozess von NAP-serverseitigen Komponenten mit NAP-Client Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c66b3-130">The figure below shows the communication process from NAP server-side components to NAP client components.</span></span>

![Architektur der Server-zu-Client-Kommunikation auf der NAP-Plattform](images/nap-server-to-client-comm.png)

 

 




