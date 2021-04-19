---
title: Iwmplibrary (isidentical-Methode)
description: Die isidentical-Methode gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- isidentical-Methode, Windows Media Player
- isidentical-Methode, Windows Media Player, iwmplibrary-Schnittstelle
- Iwmplibrary-Schnittstelle, Windows Media Player, isidentical-Methode
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370801"
---
# <a name="iwmplibraryisidentical-method"></a><span data-ttu-id="da4d9-106">Iwmplibrary:: isidentical-Methode</span><span class="sxs-lookup"><span data-stu-id="da4d9-106">IWMPLibrary::isIdentical method</span></span>

<span data-ttu-id="da4d9-107">Die **isidentical** -Methode gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="da4d9-107">The **isIdentical** method returns a value that indicates whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="da4d9-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="da4d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="da4d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4d9-110">*piwmplibrary* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da4d9-110">*pIWMPLibrary* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4d9-111">Eine **WMPLib. iwmplibrary** -Schnittstelle, die das Objekt darstellt, das mit dem aktuellen verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="da4d9-111">A **WMPLib.IWMPLibrary** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4d9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da4d9-112">Return value</span></span>

<span data-ttu-id="da4d9-113">Ein **System. Boolean** -Wert, der das Ergebnis des Vergleichs ist.</span><span class="sxs-lookup"><span data-stu-id="da4d9-113">A **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="da4d9-114">Der Wert **true** gibt an, dass die Objekte identisch sind.</span><span class="sxs-lookup"><span data-stu-id="da4d9-114">The value **true** indicates that the objects are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4d9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da4d9-115">Requirements</span></span>



| <span data-ttu-id="da4d9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da4d9-116">Requirement</span></span> | <span data-ttu-id="da4d9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="da4d9-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4d9-118">Version</span><span class="sxs-lookup"><span data-stu-id="da4d9-118">Version</span></span><br/>   | <span data-ttu-id="da4d9-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="da4d9-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="da4d9-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="da4d9-120">Namespace</span></span><br/> | <span data-ttu-id="da4d9-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="da4d9-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="da4d9-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="da4d9-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="da4d9-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="da4d9-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4d9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da4d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4d9-125">**Iwmplibrary-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="da4d9-125">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





