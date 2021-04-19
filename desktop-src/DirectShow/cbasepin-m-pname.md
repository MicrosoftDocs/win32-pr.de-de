---
description: Der Name der PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Cbasepin:: m_pName Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362061"
---
# <a name="cbasepinm_pname-member"></a><span data-ttu-id="cd682-103">Cbasepin:: m \_ PName-Member</span><span class="sxs-lookup"><span data-stu-id="cd682-103">CBasePin::m\_pName member</span></span>

<span data-ttu-id="cd682-104">Der Name der PIN.</span><span class="sxs-lookup"><span data-stu-id="cd682-104">Pin name.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd682-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd682-105">Syntax</span></span>


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a><span data-ttu-id="cd682-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd682-106">Remarks</span></span>

<span data-ttu-id="cd682-107">Die [**cbasepin:: querypininfo**](cbasepin-querypininfo.md) -Methode gibt diese Zeichenfolge als Pin-Namen zurück, und die [**cbasepin:: QueryId**](cbasepin-queryid.md) -Methode gibt Sie als PIN-Bezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="cd682-107">The [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) method returns this string as the pin name, and the [**CBasePin::QueryId**](cbasepin-queryid.md) method returns it as the pin identifier.</span></span> <span data-ttu-id="cd682-108">Im Allgemeinen ist es jedoch nicht erforderlich, dass der PIN-Name und der PIN-Bezeichner identisch sind.</span><span class="sxs-lookup"><span data-stu-id="cd682-108">In general, however, the pin name and the pin identifier are not required to be the same.</span></span> <span data-ttu-id="cd682-109">Der PIN-Bezeichner wird für die Diagramm Persistenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd682-109">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="cd682-110">Weitere Informationen finden Sie unter [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span><span class="sxs-lookup"><span data-stu-id="cd682-110">For more information, see [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd682-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd682-111">Requirements</span></span>



| <span data-ttu-id="cd682-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd682-112">Requirement</span></span> | <span data-ttu-id="cd682-113">Wert</span><span class="sxs-lookup"><span data-stu-id="cd682-113">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd682-114">Header</span><span class="sxs-lookup"><span data-stu-id="cd682-114">Header</span></span><br/> | <dl> <span data-ttu-id="cd682-115"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd682-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd682-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd682-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd682-117">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cd682-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




