---
description: Der keysvcc \_ handle-Datentyp definiert ein Schlüsseldienst handle. Ein keysvcc \_ handle-Handle wird von den Funktionen rkeyopenkeyservice und rkeyclosekeyservice verwendet.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1427a4ffd4637e073e517e5df54af72191992d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349621"
---
# <a name="keysvcc_handle"></a><span data-ttu-id="c8065-104">keysvcc- \_ handle</span><span class="sxs-lookup"><span data-stu-id="c8065-104">KEYSVCC\_HANDLE</span></span>

<span data-ttu-id="c8065-105">Der **keysvcc \_ handle** -Datentyp definiert ein Schlüsseldienst handle.</span><span class="sxs-lookup"><span data-stu-id="c8065-105">The **KEYSVCC\_HANDLE** data type defines a key service handle.</span></span> <span data-ttu-id="c8065-106">Ein **keysvcc \_ handle** -Handle wird von den Funktionen [**rkeyopenkeyservice**](rkeyopenkeyservice.md) und [**rkeyclosekeyservice**](rkeyclosekeyservice.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8065-106">A **KEYSVCC\_HANDLE** handle is used by the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) and [**RKeyCloseKeyService**](rkeyclosekeyservice.md) functions.</span></span>


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="c8065-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8065-107">Requirements</span></span>



| <span data-ttu-id="c8065-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8065-108">Requirement</span></span> | <span data-ttu-id="c8065-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c8065-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8065-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8065-110">Minimum supported client</span></span><br/> | <span data-ttu-id="c8065-111">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8065-111">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c8065-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8065-112">Minimum supported server</span></span><br/> | <span data-ttu-id="c8065-113">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8065-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8065-114">Header</span><span class="sxs-lookup"><span data-stu-id="c8065-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8065-115"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8065-115"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8065-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8065-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8065-117">**Rkeyclosekeyservice**</span><span class="sxs-lookup"><span data-stu-id="c8065-117">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="c8065-118">**Rkeyopenkeyservice**</span><span class="sxs-lookup"><span data-stu-id="c8065-118">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




