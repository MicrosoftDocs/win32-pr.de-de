---
title: TLS_HANDLE
description: Stellt ein Handle für einen Remotedesktop-Lizenzserver dar.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740713"
---
# <a name="tls_handle"></a><span data-ttu-id="e3054-104">TLS- \_ handle</span><span class="sxs-lookup"><span data-stu-id="e3054-104">TLS\_HANDLE</span></span>

<span data-ttu-id="e3054-105">Stellt ein Handle für einen Remotedesktop-Lizenzserver dar.</span><span class="sxs-lookup"><span data-stu-id="e3054-105">Represents a handle to a Remote Desktop license server.</span></span> <span data-ttu-id="e3054-106">Dieses Handle wird von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3054-106">This handle is returned by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="e3054-107">Diesem Datentyp ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e3054-107">This data type has no associated header file.</span></span> <span data-ttu-id="e3054-108">Um es zu verwenden, müssen Sie es selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3054-108">To use it, you must define it yourself as shown in this topic.</span></span>

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="e3054-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3054-109">Requirements</span></span>



| <span data-ttu-id="e3054-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3054-110">Requirement</span></span> | <span data-ttu-id="e3054-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e3054-111">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e3054-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3054-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e3054-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3054-113">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e3054-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3054-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e3054-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3054-115">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3054-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3054-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3054-117">**Tlsconnecttolsserver**</span><span class="sxs-lookup"><span data-stu-id="e3054-117">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="e3054-118">**Tlsdisconnectfromserver**</span><span class="sxs-lookup"><span data-stu-id="e3054-118">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





