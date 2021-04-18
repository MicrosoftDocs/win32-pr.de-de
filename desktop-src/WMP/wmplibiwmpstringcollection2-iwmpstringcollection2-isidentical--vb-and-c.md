---
title: IWMPStringCollection2 isidentical-Methode
description: Die isidentical-Methode gibt einen Wert zurück, der angibt, ob das durch die angegebene Schnittstelle dargestellte Objekt mit dem aktuellen identisch ist.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- isidentical-Methode, Windows Media Player
- isidentical-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface, Windows Media Player, isidentical-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365747"
---
# <a name="iwmpstringcollection2isidentical-method"></a><span data-ttu-id="3445d-106">IWMPStringCollection2:: isidentical-Methode</span><span class="sxs-lookup"><span data-stu-id="3445d-106">IWMPStringCollection2::isIdentical method</span></span>

<span data-ttu-id="3445d-107">Die **isidentical** -Methode gibt einen Wert zurück, der angibt, ob das durch die angegebene Schnittstelle dargestellte Objekt mit dem aktuellen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="3445d-107">The **isIdentical** method returns a value indicating whether the object represented by the supplied interface is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="3445d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3445d-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="3445d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3445d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3445d-110">*pIWMPStringCollection2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3445d-110">*pIWMPStringCollection2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3445d-111">Die **WMPLib. IWMPStringCollection2** -Schnittstelle, die das Objekt darstellt, das mit dem aktuellen verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3445d-111">The **WMPLib.IWMPStringCollection2** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3445d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3445d-112">Return value</span></span>

<span data-ttu-id="3445d-113">Der **System. Boolean** -Wert, der das Ergebnis des Vergleichs ist.</span><span class="sxs-lookup"><span data-stu-id="3445d-113">The **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="3445d-114">Der Wert **true** gibt an, dass die Zeichen folgen Auflistungs Objekte identisch sind.</span><span class="sxs-lookup"><span data-stu-id="3445d-114">A value of **true** indicates that the string collection objects are the same.</span></span>

## <a name="remarks"></a><span data-ttu-id="3445d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3445d-115">Remarks</span></span>

<span data-ttu-id="3445d-116">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3445d-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3445d-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3445d-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3445d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3445d-118">Requirements</span></span>



| <span data-ttu-id="3445d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3445d-119">Requirement</span></span> | <span data-ttu-id="3445d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3445d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3445d-121">Version</span><span class="sxs-lookup"><span data-stu-id="3445d-121">Version</span></span><br/>   | <span data-ttu-id="3445d-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="3445d-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="3445d-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3445d-123">Namespace</span></span><br/> | <span data-ttu-id="3445d-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3445d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3445d-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="3445d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3445d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3445d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3445d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3445d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3445d-128">**IWMPStringCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3445d-128">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





