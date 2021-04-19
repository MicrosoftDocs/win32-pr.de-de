---
title: Media. SourceUrl
description: Die SourceUrl-Eigenschaft ruft die URL des Medien Elements ab.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. SourceUrl-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359666"
---
# <a name="mediasourceurl"></a><span data-ttu-id="5b018-104">Media. SourceUrl</span><span class="sxs-lookup"><span data-stu-id="5b018-104">Media.sourceURL</span></span>

<span data-ttu-id="5b018-105">Die **SourceUrl** -Eigenschaft ruft die URL des Medien Elements ab.</span><span class="sxs-lookup"><span data-stu-id="5b018-105">The **sourceURL** property retrieves the URL of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b018-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b018-106">Syntax</span></span>

<span data-ttu-id="5b018-107">*Player*. *currentMedia*. SourceUrl</span><span class="sxs-lookup"><span data-stu-id="5b018-107">*player*.*currentMedia*.sourceURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="5b018-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="5b018-108">Possible Values</span></span>

<span data-ttu-id="5b018-109">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="5b018-109">This property is a read-only **String**.</span></span>

## <a name="examples"></a><span data-ttu-id="5b018-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b018-110">Examples</span></span>

<span data-ttu-id="5b018-111">Im folgenden JScript-Beispiel werden *Medien* verwendet. **SourceUrl** zum Abrufen der URL des ersten Medien Elements in der Beispiel Wiedergabeliste die URL des Medien Elements wird dann der Eigenschaft "Player Object **URL** " zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5b018-111">The following JScript example uses *Media*.**sourceURL** to retrieve the URL of the first media item in the sample playlist; the URL of the media item is then assigned to the player object **URL** property.</span></span> <span data-ttu-id="5b018-112">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b018-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="5b018-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b018-113">Requirements</span></span>



| <span data-ttu-id="5b018-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b018-114">Requirement</span></span> | <span data-ttu-id="5b018-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5b018-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b018-116">Version</span><span class="sxs-lookup"><span data-stu-id="5b018-116">Version</span></span><br/> | <span data-ttu-id="5b018-117">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5b018-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5b018-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5b018-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b018-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b018-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b018-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b018-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b018-121">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="5b018-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





