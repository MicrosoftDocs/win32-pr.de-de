---
title: Zuordnung von Dienst Beschreibungs Datentypen zu IDL-Datentypen
description: Die folgende Tabelle zeigt die Zuordnung der in einer Dienst Beschreibung angegebenen XML-Datentypen zu den entsprechenden Datentypen, die in IDL verwendet werden.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037425"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a><span data-ttu-id="7e7db-103">Zuordnung von Dienst Beschreibungs Datentypen zu IDL-Datentypen</span><span class="sxs-lookup"><span data-stu-id="7e7db-103">Mapping Service Description Data Types to IDL Data Types</span></span>

<span data-ttu-id="7e7db-104">Die folgende Tabelle zeigt die Zuordnung der in einer Dienst Beschreibung angegebenen XML-Datentypen zu den entsprechenden Datentypen, die in IDL verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e7db-104">The following table shows the mapping of XML data types specified in a service description to the corresponding data types used in IDL.</span></span>



| <span data-ttu-id="7e7db-105">XML-Datentyp</span><span class="sxs-lookup"><span data-stu-id="7e7db-105">XML Data Type</span></span> | <span data-ttu-id="7e7db-106">IDL-Datentyp</span><span class="sxs-lookup"><span data-stu-id="7e7db-106">IDL Data Type</span></span>  |
|---------------|----------------|
| <span data-ttu-id="7e7db-107">bin.base64</span><span class="sxs-lookup"><span data-stu-id="7e7db-107">bin.base64</span></span>    | <span data-ttu-id="7e7db-108">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="7e7db-108">SAFEARRAY</span></span>      |
| <span data-ttu-id="7e7db-109">bin.hex</span><span class="sxs-lookup"><span data-stu-id="7e7db-109">bin.hex</span></span>       | <span data-ttu-id="7e7db-110">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="7e7db-110">SAFEARRAY</span></span>      |
| <span data-ttu-id="7e7db-111">boolean</span><span class="sxs-lookup"><span data-stu-id="7e7db-111">boolean</span></span>       | <span data-ttu-id="7e7db-112">Variant \_ bool</span><span class="sxs-lookup"><span data-stu-id="7e7db-112">VARIANT\_BOOL</span></span>  |
| <span data-ttu-id="7e7db-113">char</span><span class="sxs-lookup"><span data-stu-id="7e7db-113">char</span></span>          | <span data-ttu-id="7e7db-114">WCHAR \_ t</span><span class="sxs-lookup"><span data-stu-id="7e7db-114">wchar\_t</span></span>       |
| <span data-ttu-id="7e7db-115">date</span><span class="sxs-lookup"><span data-stu-id="7e7db-115">date</span></span>          | <span data-ttu-id="7e7db-116">DATE</span><span class="sxs-lookup"><span data-stu-id="7e7db-116">DATE</span></span>           |
| <span data-ttu-id="7e7db-117">dateTime</span><span class="sxs-lookup"><span data-stu-id="7e7db-117">dateTime</span></span>      | <span data-ttu-id="7e7db-118">DATE</span><span class="sxs-lookup"><span data-stu-id="7e7db-118">DATE</span></span>           |
| <span data-ttu-id="7e7db-119">dateTime.tz</span><span class="sxs-lookup"><span data-stu-id="7e7db-119">dateTime.tz</span></span>   | <span data-ttu-id="7e7db-120">DATE</span><span class="sxs-lookup"><span data-stu-id="7e7db-120">DATE</span></span>           |
| <span data-ttu-id="7e7db-121">fixed.14.4</span><span class="sxs-lookup"><span data-stu-id="7e7db-121">fixed.14.4</span></span>    | <span data-ttu-id="7e7db-122">CY</span><span class="sxs-lookup"><span data-stu-id="7e7db-122">CY</span></span>             |
| <span data-ttu-id="7e7db-123">float</span><span class="sxs-lookup"><span data-stu-id="7e7db-123">float</span></span>         | <span data-ttu-id="7e7db-124">float</span><span class="sxs-lookup"><span data-stu-id="7e7db-124">float</span></span>          |
| <span data-ttu-id="7e7db-125">i1</span><span class="sxs-lookup"><span data-stu-id="7e7db-125">i1</span></span>            | <span data-ttu-id="7e7db-126">char</span><span class="sxs-lookup"><span data-stu-id="7e7db-126">char</span></span>           |
| <span data-ttu-id="7e7db-127">i2</span><span class="sxs-lookup"><span data-stu-id="7e7db-127">i2</span></span>            | <span data-ttu-id="7e7db-128">short</span><span class="sxs-lookup"><span data-stu-id="7e7db-128">short</span></span>          |
| <span data-ttu-id="7e7db-129">i4</span><span class="sxs-lookup"><span data-stu-id="7e7db-129">i4</span></span>            | <span data-ttu-id="7e7db-130">long</span><span class="sxs-lookup"><span data-stu-id="7e7db-130">long</span></span>           |
| <span data-ttu-id="7e7db-131">INT</span><span class="sxs-lookup"><span data-stu-id="7e7db-131">int</span></span>           | <span data-ttu-id="7e7db-132">long</span><span class="sxs-lookup"><span data-stu-id="7e7db-132">long</span></span>           |
| <span data-ttu-id="7e7db-133">number</span><span class="sxs-lookup"><span data-stu-id="7e7db-133">number</span></span>        | <span data-ttu-id="7e7db-134">BSTR</span><span class="sxs-lookup"><span data-stu-id="7e7db-134">BSTR</span></span>           |
| <span data-ttu-id="7e7db-135">r4</span><span class="sxs-lookup"><span data-stu-id="7e7db-135">r4</span></span>            | <span data-ttu-id="7e7db-136">float</span><span class="sxs-lookup"><span data-stu-id="7e7db-136">float</span></span>          |
| <span data-ttu-id="7e7db-137">r8</span><span class="sxs-lookup"><span data-stu-id="7e7db-137">r8</span></span>            | <span data-ttu-id="7e7db-138">double</span><span class="sxs-lookup"><span data-stu-id="7e7db-138">double</span></span>         |
| <span data-ttu-id="7e7db-139">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7e7db-139">string</span></span>        | <span data-ttu-id="7e7db-140">BSTR</span><span class="sxs-lookup"><span data-stu-id="7e7db-140">BSTR</span></span>           |
| <span data-ttu-id="7e7db-141">time</span><span class="sxs-lookup"><span data-stu-id="7e7db-141">time</span></span>          | <span data-ttu-id="7e7db-142">DATE</span><span class="sxs-lookup"><span data-stu-id="7e7db-142">DATE</span></span>           |
| <span data-ttu-id="7e7db-143">time.tz</span><span class="sxs-lookup"><span data-stu-id="7e7db-143">time.tz</span></span>       | <span data-ttu-id="7e7db-144">DATE</span><span class="sxs-lookup"><span data-stu-id="7e7db-144">DATE</span></span>           |
| <span data-ttu-id="7e7db-145">ui1</span><span class="sxs-lookup"><span data-stu-id="7e7db-145">ui1</span></span>           | <span data-ttu-id="7e7db-146">unsigned char</span><span class="sxs-lookup"><span data-stu-id="7e7db-146">unsigned char</span></span>  |
| <span data-ttu-id="7e7db-147">ui2</span><span class="sxs-lookup"><span data-stu-id="7e7db-147">ui2</span></span>           | <span data-ttu-id="7e7db-148">unsigned short</span><span class="sxs-lookup"><span data-stu-id="7e7db-148">unsigned short</span></span> |
| <span data-ttu-id="7e7db-149">ui4</span><span class="sxs-lookup"><span data-stu-id="7e7db-149">ui4</span></span>           | <span data-ttu-id="7e7db-150">unsigned long</span><span class="sxs-lookup"><span data-stu-id="7e7db-150">unsigned long</span></span>  |
| <span data-ttu-id="7e7db-151">uri</span><span class="sxs-lookup"><span data-stu-id="7e7db-151">uri</span></span>           | <span data-ttu-id="7e7db-152">BSTR</span><span class="sxs-lookup"><span data-stu-id="7e7db-152">BSTR</span></span>           |
| <span data-ttu-id="7e7db-153">uuid</span><span class="sxs-lookup"><span data-stu-id="7e7db-153">uuid</span></span>          | <span data-ttu-id="7e7db-154">BSTR</span><span class="sxs-lookup"><span data-stu-id="7e7db-154">BSTR</span></span>           |



 

 

 




