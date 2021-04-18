---
title: Iwmplibraryservices getlibrarybytype-Methode
description: Die getlibrarybytype-Methode gibt eine iwmplibrary-Schnittstelle zurück, die die Bibliothek mit dem angegebenen Typ und Index darstellt.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- getlibrarybytype-Methode, Windows Media Player
- getlibrarybytype-Methode, Windows Media Player, iwmplibraryservices-Schnittstelle
- Iwmplibraryservices Interface, Windows Media Player, getlibrarybytype-Methode
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361019"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a><span data-ttu-id="a3d10-106">Iwmplibraryservices:: getlibrarybytype-Methode</span><span class="sxs-lookup"><span data-stu-id="a3d10-106">IWMPLibraryServices::getLibraryByType method</span></span>

<span data-ttu-id="a3d10-107">Die **getlibrarybytype** -Methode gibt eine **iwmplibrary** -Schnittstelle zurück, die die Bibliothek mit dem angegebenen Typ und Index darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3d10-107">The **getLibraryByType** method returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d10-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d10-108">Syntax</span></span>


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a><span data-ttu-id="a3d10-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3d10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d10-110">*wmplt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d10-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d10-111">Ein Wert aus der **WMPLib. wmplibrarytype** -Enumeration, der den Typ der abzurufenden Bibliothek angibt.</span><span class="sxs-lookup"><span data-stu-id="a3d10-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a3d10-112">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d10-112">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d10-113">Ein **System. Int32** -Wert, der den Index der abzurufenden Bibliothek ist.</span><span class="sxs-lookup"><span data-stu-id="a3d10-113">A **System.Int32** that is the index of the library to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d10-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3d10-114">Return value</span></span>

<span data-ttu-id="a3d10-115">Eine **WMPLib. iwmplibrary** -Schnittstelle für die Bibliothek, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3d10-115">A **WMPLib.IWMPLibrary** interface for the library that is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d10-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3d10-116">Remarks</span></span>

<span data-ttu-id="a3d10-117">Es gibt nur eine lokale Bibliothek, und die Disk-Bibliotheken sind nur auf Daten-CDs und DVDs verfügbar, die Medieninhalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3d10-117">There is only one local library, and disc libraries are available only on data CDs and DVDs that contain media content.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d10-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3d10-118">Requirements</span></span>



| <span data-ttu-id="a3d10-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3d10-119">Requirement</span></span> | <span data-ttu-id="a3d10-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a3d10-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d10-121">Version</span><span class="sxs-lookup"><span data-stu-id="a3d10-121">Version</span></span><br/>   | <span data-ttu-id="a3d10-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="a3d10-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="a3d10-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3d10-123">Namespace</span></span><br/> | <span data-ttu-id="a3d10-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a3d10-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a3d10-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="a3d10-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a3d10-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a3d10-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d10-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3d10-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d10-128">**Iwmplibrary-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a3d10-128">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3d10-129">**Iwmplibraryservices-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a3d10-129">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a3d10-130">**Wmplibrarytype**</span><span class="sxs-lookup"><span data-stu-id="a3d10-130">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





