---
title: Wiedergabeliste. AttributeName
description: Die AttributeName-Eigenschaft ruft den Namen eines Attributs an einem angegebenen Index ab.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Wiedergabeliste. AttributeName Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366692"
---
# <a name="playlistattributename"></a><span data-ttu-id="7c07e-104">Wiedergabeliste. AttributeName</span><span class="sxs-lookup"><span data-stu-id="7c07e-104">Playlist.attributeName</span></span>

<span data-ttu-id="7c07e-105">Die **attributeName** -Eigenschaft ruft den Namen eines Attributs an einem angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="7c07e-105">The **attributeName** property retrieves the name of an attribute at a specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c07e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c07e-106">Syntax</span></span>

<span data-ttu-id="7c07e-107">*Player*. *currentwiedergabe*. **attributeName**( *Index* )</span><span class="sxs-lookup"><span data-stu-id="7c07e-107">*player*.*currentPlaylist*.**attributeName**( *index* )</span></span>

## <a name="parameters"></a><span data-ttu-id="7c07e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c07e-108">Parameters</span></span>

<span data-ttu-id="7c07e-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="7c07e-109">*index*</span></span>

<span data-ttu-id="7c07e-110">Die **Zahl** (**Long**), die den Index enthält.</span><span class="sxs-lookup"><span data-stu-id="7c07e-110">**Number** (**long**) containing the index.</span></span>

## <a name="possible-values"></a><span data-ttu-id="7c07e-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7c07e-111">Possible Values</span></span>

<span data-ttu-id="7c07e-112">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="7c07e-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c07e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c07e-113">Remarks</span></span>

<span data-ttu-id="7c07e-114">Die Anzahl der Attribute wird von der **AttributeCount** -Eigenschaft abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7c07e-114">The number of attributes is retrieved by the **attributeCount** property.</span></span> <span data-ttu-id="7c07e-115">Bei einem Index gibt **attributeName** eine **Zeichenfolge** zurück, die zusammen mit "stiteminfo" oder " **getiteminfo** " verwendet werden kann, um einen Wert für das Attribut anzugeben oder abzurufen. </span><span class="sxs-lookup"><span data-stu-id="7c07e-115">Given an index, **attributeName** returns a **String** that can be used in conjunction with **setItemInfo** or **getItemInfo** to specify or retrieve a value for the attribute.</span></span>

<span data-ttu-id="7c07e-116">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7c07e-116">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="7c07e-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7c07e-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7c07e-118">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="7c07e-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="7c07e-119">Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](playlist-attributecount.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7c07e-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c07e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c07e-120">Requirements</span></span>



| <span data-ttu-id="7c07e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c07e-121">Requirement</span></span> | <span data-ttu-id="7c07e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7c07e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c07e-123">Version</span><span class="sxs-lookup"><span data-stu-id="7c07e-123">Version</span></span><br/> | <span data-ttu-id="7c07e-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7c07e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7c07e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7c07e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c07e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c07e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c07e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c07e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c07e-128">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="7c07e-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="7c07e-129">**Wiedergabeliste. AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="7c07e-129">**Playlist.attributeCount**</span></span>](playlist-attributecount.md)
</dt> <dt>

[<span data-ttu-id="7c07e-130">**Wiedergabeliste. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="7c07e-130">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="7c07e-131">**Wiedergabeliste. Einstellungs Element**</span><span class="sxs-lookup"><span data-stu-id="7c07e-131">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="7c07e-132">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="7c07e-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7c07e-133">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="7c07e-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





