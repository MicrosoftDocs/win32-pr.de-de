---
title: RAS-Dienst Datentypen (RAS. h)
description: Die folgenden Datentypen werden von der RAS-Dienst-API verwendet.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956434"
---
# <a name="remote-access-service-data-types"></a><span data-ttu-id="36e1b-105">RAS-Dienst Datentypen</span><span class="sxs-lookup"><span data-stu-id="36e1b-105">Remote Access Service Data Types</span></span>

<span data-ttu-id="36e1b-106">Die folgenden Datentypen werden von der RAS-Dienst-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="36e1b-106">The following data types are used by the Remote Access Service API.</span></span>


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

<span data-ttu-id="36e1b-107">**RASIPV4ADDR**</span><span class="sxs-lookup"><span data-stu-id="36e1b-107">**RASIPV4ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="36e1b-108">Ein [**in \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) , das eine IPv4-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="36e1b-108">A [**in\_addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) that contains an IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="36e1b-109">Unterstützt in Windows Vista oder höheren Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="36e1b-109">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> <dt>

<span data-ttu-id="36e1b-110">**RASIPV6ADDR**</span><span class="sxs-lookup"><span data-stu-id="36e1b-110">**RASIPV6ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="36e1b-111">Eine [**IN6 \_ addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) , die eine IPv6-Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="36e1b-111">A [**in6\_addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) that contains an IPv6 address.</span></span>

> [!Note]  
> <span data-ttu-id="36e1b-112">Unterstützt in Windows Vista oder höheren Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="36e1b-112">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36e1b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36e1b-113">Requirements</span></span>



| <span data-ttu-id="36e1b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36e1b-114">Requirement</span></span> | <span data-ttu-id="36e1b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="36e1b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36e1b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36e1b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36e1b-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36e1b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="36e1b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36e1b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36e1b-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36e1b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="36e1b-120">Header</span><span class="sxs-lookup"><span data-stu-id="36e1b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="36e1b-121"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="36e1b-121"><dt>Ras.h</dt></span></span> </dl> |



 

