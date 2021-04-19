---
title: Iwmpwiedergabe-Methode "muveitem"
description: Die Methode "muveitem" ändert den Speicherort eines Medien Elements in der Wiedergabeliste.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Windows-Media Player für die Windows-
- muveitem-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, Methode "muveitem"
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362039"
---
# <a name="iwmpplaylistmoveitem-method"></a><span data-ttu-id="fd6df-106">Iwmpwiedergabe:: muveitem-Methode</span><span class="sxs-lookup"><span data-stu-id="fd6df-106">IWMPPlaylist::moveItem method</span></span>

<span data-ttu-id="fd6df-107">Die Methode " **muveitem** " ändert den Speicherort eines Medien Elements in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="fd6df-107">The **moveItem** method changes the location of a media item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6df-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd6df-108">Syntax</span></span>


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a><span data-ttu-id="fd6df-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd6df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6df-110">*lindexold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6df-110">*lIndexOld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6df-111">Ein **System. Int32** -Wert, der der ursprüngliche Index ist.</span><span class="sxs-lookup"><span data-stu-id="fd6df-111">A **System.Int32** that is the original index.</span></span>

</dd> <dt>

<span data-ttu-id="fd6df-112">*lindexnew* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6df-112">*lIndexNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6df-113">Ein **System. Int32** -Wert, der der neue Index ist.</span><span class="sxs-lookup"><span data-stu-id="fd6df-113">A **System.Int32** that is the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6df-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd6df-114">Return value</span></span>

<span data-ttu-id="fd6df-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fd6df-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd6df-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd6df-116">Remarks</span></span>

<span data-ttu-id="fd6df-117">Alle Elemente nach dem eingefügten Element werden die Indexnummern um 1 erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fd6df-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="fd6df-118">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="fd6df-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="fd6df-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fd6df-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6df-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd6df-120">Requirements</span></span>



| <span data-ttu-id="fd6df-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd6df-121">Requirement</span></span> | <span data-ttu-id="fd6df-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fd6df-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6df-123">Version</span><span class="sxs-lookup"><span data-stu-id="fd6df-123">Version</span></span><br/>   | <span data-ttu-id="fd6df-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="fd6df-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fd6df-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd6df-125">Namespace</span></span><br/> | <span data-ttu-id="fd6df-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fd6df-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fd6df-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="fd6df-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fd6df-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fd6df-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6df-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd6df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6df-130">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fd6df-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fd6df-131">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fd6df-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fd6df-132">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fd6df-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





