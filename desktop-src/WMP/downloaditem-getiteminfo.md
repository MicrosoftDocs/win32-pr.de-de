---
title: Downloader. getiteminfo-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die getiteminfo-Methode ruft den Wert eines Attributs für das Download Element ab.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, Downloader-Klasse
- Downloader-Klasse, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367624"
---
# <a name="downloaditemgetiteminfo-method"></a><span data-ttu-id="c6a97-108">Downloader. getiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="c6a97-108">DownloadItem.getItemInfo method</span></span>

> [!Note]  
> <span data-ttu-id="c6a97-109">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="c6a97-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c6a97-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6a97-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c6a97-111">Die **getiteminfo** -Methode ruft den Wert eines Attributs für das Download Element ab.</span><span class="sxs-lookup"><span data-stu-id="c6a97-111">The **getItemInfo** method retrieves the value of an attribute for the download item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a97-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6a97-112">Syntax</span></span>


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a><span data-ttu-id="c6a97-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6a97-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a97-114">*ItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6a97-114">*itemname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a97-115">**Zeichenfolge** , die den Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="c6a97-115">**String** containing the attribute name.</span></span> <span data-ttu-id="c6a97-116">Unterstützte Werte sind albumartist, Album, Duration, WM/Provider, Title, userrating und WM/tracknumber.</span><span class="sxs-lookup"><span data-stu-id="c6a97-116">Supported values are AlbumArtist, Album, Duration, WM/Provider, Title, UserRating, and WM/TrackNumber.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6a97-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6a97-117">Return value</span></span>

<span data-ttu-id="c6a97-118">Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des durch *ItemName* angegebenen Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="c6a97-118">This method returns a **String** containing the value of the attribute specified by *itemname*.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a97-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6a97-119">Remarks</span></span>

<span data-ttu-id="c6a97-120">Diese Methode ruft mithilfe der Bits-Beschreibungs Zeichenfolge angegebene Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="c6a97-120">This method retrieves attributes specified using the BITS description string.</span></span> <span data-ttu-id="c6a97-121">Weitere Informationen finden Sie unter [Windows Media Player Bits-Auftrags Konvention](windows-media-player-bits-job-convention.md).</span><span class="sxs-lookup"><span data-stu-id="c6a97-121">See [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md).</span></span>

<span data-ttu-id="c6a97-122">Diese Methode wird für das Herunterladen im Hintergrund unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6a97-122">This method is supported for background downloading.</span></span> <span data-ttu-id="c6a97-123">Der Code sollte diese Methode bei Verwendung von Echt Zeit Downloads nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6a97-123">Your code should not call this method when using real-time downloading.</span></span>

<span data-ttu-id="c6a97-124">Diese Methode kann nur Informationen für BITS-Aufträge abrufen, die während der aktuellen Windows Media Player-Sitzung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="c6a97-124">This method can retrieve information for BITS jobs added during the current Windows Media Player session only.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a97-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6a97-125">Requirements</span></span>



| <span data-ttu-id="c6a97-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6a97-126">Requirement</span></span> | <span data-ttu-id="c6a97-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c6a97-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a97-128">Version</span><span class="sxs-lookup"><span data-stu-id="c6a97-128">Version</span></span><br/> | <span data-ttu-id="c6a97-129">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="c6a97-129">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="c6a97-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c6a97-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="c6a97-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6a97-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a97-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6a97-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a97-133">**Download Item. Type**</span><span class="sxs-lookup"><span data-stu-id="c6a97-133">**DownloadItem.type**</span></span>](downloaditem-type.md)
</dt> <dt>

[<span data-ttu-id="c6a97-134">**Download Item-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c6a97-134">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





