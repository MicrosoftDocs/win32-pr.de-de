---
title: IWMPMediaCollection2 getplaylistbyquery-Methode
description: Die getplaylistbyquery-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die Zugriff auf Medienelemente bietet, die den Abfragebedingungen entsprechen.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- getplaylistbyquery-Methode, Windows-Media Player
- getplaylistbyquery-Methode, Windows Media Player, IWMPMediaCollection2-Schnittstelle
- IWMPMediaCollection2 Interface, Windows Media Player, getplaylistbyquery-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370745"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a><span data-ttu-id="c1c44-106">IWMPMediaCollection2:: getplaylistbyquery-Methode</span><span class="sxs-lookup"><span data-stu-id="c1c44-106">IWMPMediaCollection2::getPlaylistByQuery method</span></span>

<span data-ttu-id="c1c44-107">Die- `getPlaylistByQuery` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die Zugriff auf Medienelemente bietet, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c1c44-107">The `getPlaylistByQuery` method returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c44-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1c44-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a><span data-ttu-id="c1c44-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1c44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c44-110">*pquery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1c44-110">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c44-111">Die **WMPLib. iwmpquery** -Schnittstelle, die die Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1c44-111">The **WMPLib.IWMPQuery** interface that represents the query.</span></span>

</dd> <dt>

<span data-ttu-id="c1c44-112">*bstraumediatype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1c44-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c44-113">Die **System. String** , die den Medientyp ist.</span><span class="sxs-lookup"><span data-stu-id="c1c44-113">The **System.String** that is the media type.</span></span> <span data-ttu-id="c1c44-114">Muss einen der folgenden Werte enthalten: "Audiodatei", "Video", "Photo", "Wiedergabeliste" oder "Other".</span><span class="sxs-lookup"><span data-stu-id="c1c44-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="c1c44-115">*bstrausortattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1c44-115">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c44-116">Die **System. String** , die der für die Sortierung verwendete Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="c1c44-116">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="c1c44-117">Eine Zeichenfolge der Länge 0 (null) bedeutet, dass keine Sortierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1c44-117">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="c1c44-118">*fsortascending* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1c44-118">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c44-119">Der **System. Boolean** -Wert, der angibt, ob die Wiedergabeliste in aufsteigender Reihenfolge sortiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c1c44-119">The **System.Boolean** value that indicates whether the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c44-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1c44-120">Return value</span></span>

<span data-ttu-id="c1c44-121">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufene Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="c1c44-121">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1c44-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1c44-122">Remarks</span></span>

<span data-ttu-id="c1c44-123">Bei Verbund Abfragen mit **iwmpquery** wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="c1c44-123">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="c1c44-124">Wenn die durch den *pquery* -Parameter angegebene Verbund Abfrage eine Bedingung enthält, die auf dem **mediaType** -Attribut basiert, wird diese Bedingung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c1c44-124">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="c1c44-125">Der Wert für den *bstraumediatype* -Parameter wird immer verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1c44-125">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="c1c44-126">Wenn die Verbund Abfrage z. b. die Bedingung "MediaType ist mit Audiodaten" enthält und der Wert für den *botmediatype* -Parameter "Video" ist, enthält die resultierende Wiedergabeliste nur Video Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1c44-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c44-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1c44-127">Requirements</span></span>



| <span data-ttu-id="c1c44-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1c44-128">Requirement</span></span> | <span data-ttu-id="c1c44-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c1c44-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c44-130">Version</span><span class="sxs-lookup"><span data-stu-id="c1c44-130">Version</span></span><br/>   | <span data-ttu-id="c1c44-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="c1c44-131">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="c1c44-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1c44-132">Namespace</span></span><br/> | <span data-ttu-id="c1c44-133">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c1c44-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c1c44-134">Assembly</span><span class="sxs-lookup"><span data-stu-id="c1c44-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c1c44-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c1c44-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c44-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1c44-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c44-137">**IWMPMediaCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c1c44-137">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1c44-138">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c1c44-138">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1c44-139">**Iwmpquery-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c1c44-139">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1c44-140">**MediaType-Attribut**</span><span class="sxs-lookup"><span data-stu-id="c1c44-140">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





