---
title: Iwmpplaylistcollection (IsDeleted-Methode)
description: Die IsDeleted-Methode gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner Gelöschte Elemente befindet.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- IsDeleted-Methode (Windows Media Player)
- IsDeleted-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle, Windows Media Player, IsDeleted-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367417"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a><span data-ttu-id="2813d-106">Iwmpplaylistcollection:: IsDeleted-Methode</span><span class="sxs-lookup"><span data-stu-id="2813d-106">IWMPPlaylistCollection::isDeleted method</span></span>

<span data-ttu-id="2813d-107">Die **isDeleted** -Methode gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner Gelöschte Elemente befindet.</span><span class="sxs-lookup"><span data-stu-id="2813d-107">The **isDeleted** method returns a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2813d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2813d-108">Syntax</span></span>


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a><span data-ttu-id="2813d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2813d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2813d-110">*pitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2813d-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2813d-111">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgefragte Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="2813d-111">A **WMPLib.IWMPPlaylist** interface for the queried playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2813d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2813d-112">Return value</span></span>

<span data-ttu-id="2813d-113">Ein **System. Boolean** -Wert, der angibt, ob die Wiedergabeliste gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="2813d-113">A **System.Boolean** that specifies whether the playlist was deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="2813d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2813d-114">Requirements</span></span>



| <span data-ttu-id="2813d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2813d-115">Requirement</span></span> | <span data-ttu-id="2813d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2813d-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2813d-117">Version</span><span class="sxs-lookup"><span data-stu-id="2813d-117">Version</span></span><br/>   | <span data-ttu-id="2813d-118">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2813d-118">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="2813d-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="2813d-119">Namespace</span></span><br/> | <span data-ttu-id="2813d-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2813d-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2813d-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="2813d-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2813d-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2813d-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2813d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2813d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2813d-124">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2813d-124">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2813d-125">**Iwmpplaylistcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2813d-125">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





