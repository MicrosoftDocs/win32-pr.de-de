---
title: Mediacollection. getmediaatom-Methode
description: Die getmediaatom-Methode ruft den Index ab, bei dem ein angegebenes Attribut innerhalb des Satzes verfügbarer Attribute liegt.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- getmediaatom-Methode, Windows-Media Player
- getmediaatom-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getmediaatom-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370066"
---
# <a name="mediacollectiongetmediaatom-method"></a><span data-ttu-id="1386c-106">Mediacollection. getmediaatom-Methode</span><span class="sxs-lookup"><span data-stu-id="1386c-106">MediaCollection.getMediaAtom method</span></span>

<span data-ttu-id="1386c-107">Die **getmediaatom** -Methode ruft den Index ab, bei dem ein angegebenes Attribut innerhalb des Satzes verfügbarer Attribute liegt.</span><span class="sxs-lookup"><span data-stu-id="1386c-107">The **getMediaAtom** method retrieves the index at which a specified attribute resides within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1386c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1386c-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="1386c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1386c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1386c-110">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1386c-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1386c-111">**Zeichenfolge** , die den Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="1386c-111">**String** containing the attribute name.</span></span> <span data-ttu-id="1386c-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="1386c-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1386c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1386c-113">Return value</span></span>

<span data-ttu-id="1386c-114">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="1386c-114">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="1386c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1386c-115">Remarks</span></span>

<span data-ttu-id="1386c-116">Die mit dieser Methode abgerufene Indexnummer kann an die *Medien* übermittelt werden. die **getiteminfobyatom** -Methode, um auf Attributwerte zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1386c-116">The index number retrieved with this method can be passed to the *Media*.**getItemInfoByAtom** method to access attribute values.</span></span> <span data-ttu-id="1386c-117">Diese Technik ist in der Regel effizienter, wenn Sie mit großen Wiedergabelisten arbeiten, als der Zugriff auf einen Attribut Wert nach Namen über das *Medium*. **getiteminfo** oder *Medium*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="1386c-117">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span>

<span data-ttu-id="1386c-118">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1386c-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="1386c-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1386c-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1386c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1386c-120">Requirements</span></span>



| <span data-ttu-id="1386c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1386c-121">Requirement</span></span> | <span data-ttu-id="1386c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1386c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1386c-123">Version</span><span class="sxs-lookup"><span data-stu-id="1386c-123">Version</span></span><br/> | <span data-ttu-id="1386c-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="1386c-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1386c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1386c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1386c-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1386c-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1386c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1386c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1386c-128">**Media. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="1386c-128">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1386c-129">**Media. getiteminfobyatom**</span><span class="sxs-lookup"><span data-stu-id="1386c-129">**Media.getItemInfoByAtom**</span></span>](media-getiteminfobyatom.md)
</dt> <dt>

[<span data-ttu-id="1386c-130">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="1386c-130">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="1386c-131">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1386c-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="1386c-132">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="1386c-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1386c-133">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="1386c-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





