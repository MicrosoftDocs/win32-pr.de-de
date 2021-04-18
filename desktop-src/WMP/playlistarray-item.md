---
title: Playlistarray. Item-Methode
description: Die Item-Methode ruft die Wiedergabeliste am angegebenen Index ab.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- Element-Methoden Fenster Media Player
- Item-Methode, Windows Media Player, playlistarray-Klasse
- Playlistarray-Klasse, Windows Media Player, Element-Methode
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360931"
---
# <a name="playlistarrayitem-method"></a><span data-ttu-id="29ae7-106">Playlistarray. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="29ae7-106">PlaylistArray.item method</span></span>

<span data-ttu-id="29ae7-107">Die **Item** -Methode ruft die Wiedergabeliste am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="29ae7-107">The **item** method retrieves the playlist at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ae7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="29ae7-108">Syntax</span></span>


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="29ae7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29ae7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ae7-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ae7-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ae7-111">**Zahl** (**Long**), die den Index der abzurufenden Wiedergabeliste enthält.</span><span class="sxs-lookup"><span data-stu-id="29ae7-111">**Number** (**long**) containing the index of the playlist to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ae7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29ae7-112">Return value</span></span>

<span data-ttu-id="29ae7-113">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="29ae7-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="29ae7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29ae7-114">Remarks</span></span>

<span data-ttu-id="29ae7-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29ae7-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="29ae7-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="29ae7-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29ae7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29ae7-117">Requirements</span></span>



| <span data-ttu-id="29ae7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29ae7-118">Requirement</span></span> | <span data-ttu-id="29ae7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="29ae7-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29ae7-120">Version</span><span class="sxs-lookup"><span data-stu-id="29ae7-120">Version</span></span><br/> | <span data-ttu-id="29ae7-121">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="29ae7-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="29ae7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="29ae7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="29ae7-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29ae7-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ae7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29ae7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ae7-125">**Playlistarray-Objekt**</span><span class="sxs-lookup"><span data-stu-id="29ae7-125">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="29ae7-126">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="29ae7-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="29ae7-127">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="29ae7-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





