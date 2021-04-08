---
description: Der ETYPE/SAP-Teil des Erfassungs Filters benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine bestimmte Kombination von ETYPEs und Dienst Zugriffs Punkten (SAPS) verfügen.
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Der ETYPE/SAP-Filter Teil wird geschrieben.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960341"
---
# <a name="writing-etypesap-filter-portion"></a><span data-ttu-id="a7e38-103">Der ETYPE/SAP-Filter Teil wird geschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7e38-103">Writing Etype/SAP Filter Portion</span></span>

<span data-ttu-id="a7e38-104">Der ETYPE/SAP-Teil des Erfassungs Filters benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine bestimmte Kombination von ETYPEs und [*Dienst Zugriffs Punkten*](s.md) (SAPS) verfügen.</span><span class="sxs-lookup"><span data-stu-id="a7e38-104">The Etype/SAP portion of the capture filter notifies the Network Monitor driver to accept frames that have a specific combination of Etypes and [*service access points*](s.md) (SAPs).</span></span> <span data-ttu-id="a7e38-105">ETYPEs und SAPS sind beide Möglichkeiten, wie Protokolle auf niedriger Ebene, z. b. Ethernet, LLC und Snap, welches Protokoll befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="a7e38-105">Etypes and SAPs are both ways that low-level protocols such as Ethernet, LLC, and Snap indicate which protocol follows them.</span></span> <span data-ttu-id="a7e38-106">Dies gilt insbesondere in folgenden Fällen:</span><span class="sxs-lookup"><span data-stu-id="a7e38-106">Specifically:</span></span>

-   <span data-ttu-id="a7e38-107">Ethernet gibt einen ETYPE an</span><span class="sxs-lookup"><span data-stu-id="a7e38-107">Ethernet specifies an Etype</span></span>
-   <span data-ttu-id="a7e38-108">LLC gibt einen SAP an</span><span class="sxs-lookup"><span data-stu-id="a7e38-108">LLC specifies a SAP</span></span>
-   <span data-ttu-id="a7e38-109">"Snap" gibt einen ETYPE an</span><span class="sxs-lookup"><span data-stu-id="a7e38-109">Snap specifies an Etype</span></span>

## <a name="etypesap-capture-filter-flags"></a><span data-ttu-id="a7e38-110">ETYPE-/SAP-Erfassungs Filter-Flags</span><span class="sxs-lookup"><span data-stu-id="a7e38-110">Etype/SAP Capture Filter Flags</span></span>

<span data-ttu-id="a7e38-111">Verwenden Sie die folgenden Informationen, um die Flags im **Filterflags** -Member der [**capturefilter**](capturefilter.md) -Struktur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a7e38-111">Use the following information to set the flags in the **FilterFlags** member of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="a7e38-112">Flag</span><span class="sxs-lookup"><span data-stu-id="a7e38-112">Flag</span></span>                                         | <span data-ttu-id="a7e38-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a7e38-113">Meaning</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e38-114">capturefilter- \_ Flags \_ enthalten \_ alle \_ SAPS</span><span class="sxs-lookup"><span data-stu-id="a7e38-114">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_SAPS</span></span>   | <span data-ttu-id="a7e38-115">Übergibt alle SAP-Werte und benachrichtigt den Treiber, dass alle SAP-Werte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="a7e38-115">Passes all SAP values and notifies the driver that all SAP values are valid.</span></span> <span data-ttu-id="a7e38-116">In Kombination mit Werten im **lpsaptable** -Element benachrichtigt das Flag den Treiber, dass alle SAP-Werte außer den in der **lpsaptable** gültigen sind.</span><span class="sxs-lookup"><span data-stu-id="a7e38-116">If combined with any values in the **lpSapTable** member, this flag notifies the driver that all SAP values except those in the **lpSapTable** are valid.</span></span><br/>           |
| <span data-ttu-id="a7e38-117">capturefilter- \_ Flags \_ enthalten \_ alle \_ ETYPEs</span><span class="sxs-lookup"><span data-stu-id="a7e38-117">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_ETYPES</span></span> | <span data-ttu-id="a7e38-118">Übergibt alle ETYPE-Werte und benachrichtigt den Treiber, dass alle ETYPE-Werte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="a7e38-118">Passes all Etype values and notifies the driver that all Etype values are valid.</span></span> <span data-ttu-id="a7e38-119">Wenn Sie mit Werten im **lpeer typetable** -Member kombiniert werden, benachrichtigt dieses Flag den Treiber, dass alle ETYPE-Werte außer den Werten in der **lpeer typetable** gültig sind.</span><span class="sxs-lookup"><span data-stu-id="a7e38-119">If combined with any values in the **lpEtypeTable** member, this flag notifies the driver that all Etype values except those in the **lpEtypeTable** are valid.</span></span><br/> |
| <span data-ttu-id="a7e38-120">capturefilter \_ - \_ Flags \_ nur lokal</span><span class="sxs-lookup"><span data-stu-id="a7e38-120">CAPTUREFILTER\_ FLAGS\_LOCAL\_ONLY</span></span>           | <span data-ttu-id="a7e38-121">Wenn Sie dieses Flag festlegen, wird eine NIC nicht auf den P-Modus festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a7e38-121">Setting this flag will not set a NIC to P-Mode.</span></span> <span data-ttu-id="a7e38-122">Es wird nur lokaler Datenverkehr (alle Frames zum lokalen Computer) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a7e38-122">You will only see local traffic (any frames to the local machine).</span></span>                                                                                                                                          |
| <span data-ttu-id="a7e38-123">capturefilter- \_ Flags \_ bleiben \_ RAW</span><span class="sxs-lookup"><span data-stu-id="a7e38-123">CAPTUREFILTER\_ FLAGS\_KEEP\_RAW</span></span>             | <span data-ttu-id="a7e38-124">Speichert SMT-und TokenRing-Mac-Frames.</span><span class="sxs-lookup"><span data-stu-id="a7e38-124">Keeps SMT and Token Ring MAC frames.</span></span>                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a><span data-ttu-id="a7e38-125">ETYPE/SAP-Erfassungs Filter Einstellungen</span><span class="sxs-lookup"><span data-stu-id="a7e38-125">Etype/SAP Capture Filter Settings</span></span>

<span data-ttu-id="a7e38-126">Verwenden Sie die folgenden Informationen, um die **lpsaptable** -und **lpetypetable** -Elemente der [**capturefilter**](capturefilter.md) -Struktur festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a7e38-126">Use the following information to set the **lpSapTable** and **lpEtypeTable** members of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="a7e38-127">Einstellung</span><span class="sxs-lookup"><span data-stu-id="a7e38-127">Setting</span></span>          | <span data-ttu-id="a7e38-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a7e38-128">Meaning</span></span>                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e38-129">**lpsaptable**</span><span class="sxs-lookup"><span data-stu-id="a7e38-129">**lpSapTable**</span></span>   | <span data-ttu-id="a7e38-130">Listet die SAP-Werte auf, die der Treiber übergeben soll.</span><span class="sxs-lookup"><span data-stu-id="a7e38-130">Lists the SAP values that you want the driver to pass.</span></span> <span data-ttu-id="a7e38-131">Diese Liste weist den Netzwerkmonitor Treiber an, einen Frame zu validieren, der eine Entsprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="a7e38-131">This list tells the Network Monitor driver to validate any frame that contains a match.</span></span> <span data-ttu-id="a7e38-132">Wenn die capturefilter- \_ Flags \_ \_ alle \_ SAPS enthalten, wird dies zu einer Ausnahmeliste (sofern gefunden, nicht bestanden).</span><span class="sxs-lookup"><span data-stu-id="a7e38-132">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (if found, do not pass).</span></span>           |
| <span data-ttu-id="a7e38-133">**lpeer typetable**</span><span class="sxs-lookup"><span data-stu-id="a7e38-133">**lpEtypeTable**</span></span> | <span data-ttu-id="a7e38-134">Listet die ETYPE-Werte auf, die der Netzwerkmonitor Treiber übergeben soll.</span><span class="sxs-lookup"><span data-stu-id="a7e38-134">Lists the Etype values that you want the Network Monitor driver to pass.</span></span> <span data-ttu-id="a7e38-135">Diese Liste allein weist den Treiber an, einen Frame zu validieren, der eine Entsprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="a7e38-135">This list alone tells the driver to validate any frame that contains a match.</span></span> <span data-ttu-id="a7e38-136">Wenn die capturefilter- \_ Flags \_ \_ alle \_ ETYPEs festgelegt sind, wird dies zu einer Ausnahmeliste (sofern gefunden, nicht bestanden).</span><span class="sxs-lookup"><span data-stu-id="a7e38-136">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (if found, do not pass).</span></span> |



 

 

 




