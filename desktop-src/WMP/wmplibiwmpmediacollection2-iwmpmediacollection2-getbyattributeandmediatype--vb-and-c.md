---
title: IWMPMediaCollection2 getbyattributeandmediatype-Methode
description: Die getbyattributeandmediatype-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die den Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp ermöglicht.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- getbyattributeandmediatype-Methode, Windows Media Player
- getbyattributeandmediatype-Methode, Windows Media Player, IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2 Interface, Windows Media Player, getbyattributeandmediatype-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365405"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a><span data-ttu-id="80707-106">IWMPMediaCollection2:: getbyattributeandmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="80707-106">IWMPMediaCollection2::getByAttributeAndMediaType method</span></span>

<span data-ttu-id="80707-107">Die- `getByAttributeAndMediaType` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="80707-107">The `getByAttributeAndMediaType` method returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="80707-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="80707-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a><span data-ttu-id="80707-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="80707-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80707-110">*bstrattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80707-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80707-111">Die **System. String** -Eigenschaft, die das angegebene Attribut ist.</span><span class="sxs-lookup"><span data-stu-id="80707-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="80707-112">*bstrauvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80707-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80707-113">Die **System. String** , die den angegebenen Wert für das in *bstrattribute* angegebene Attribut ist.</span><span class="sxs-lookup"><span data-stu-id="80707-113">The **System.String** that is the specified value for the attribute that is specified in *bstrAttribute*.</span></span>

</dd> <dt>

<span data-ttu-id="80707-114">*bstraumediatype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80707-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80707-115">Die **System. String** , die den angegebenen Medientyp ist.</span><span class="sxs-lookup"><span data-stu-id="80707-115">The **System.String** that is the specified media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80707-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80707-116">Return value</span></span>

<span data-ttu-id="80707-117">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufene Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="80707-117">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="80707-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80707-118">Requirements</span></span>



| <span data-ttu-id="80707-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80707-119">Requirement</span></span> | <span data-ttu-id="80707-120">Wert</span><span class="sxs-lookup"><span data-stu-id="80707-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80707-121">Version</span><span class="sxs-lookup"><span data-stu-id="80707-121">Version</span></span><br/>   | <span data-ttu-id="80707-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="80707-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="80707-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="80707-123">Namespace</span></span><br/> | <span data-ttu-id="80707-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="80707-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="80707-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="80707-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="80707-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="80707-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80707-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80707-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80707-128">**IWMPMediaCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="80707-128">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="80707-129">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="80707-129">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





