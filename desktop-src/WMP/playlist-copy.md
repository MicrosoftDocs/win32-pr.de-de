---
title: Wiedergabeliste. Kopieren
description: Die Copy-Methode startet einen Kopiervorgang von der CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- Wiedergabeliste. Windows-Media Player kopieren
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370687"
---
# <a name="playlistcopy"></a><span data-ttu-id="20b8d-104">Wiedergabeliste. Kopieren</span><span class="sxs-lookup"><span data-stu-id="20b8d-104">PLAYLIST.copy</span></span>

<span data-ttu-id="20b8d-105">Die **Copy** -Methode startet einen Kopiervorgang von der CD.</span><span class="sxs-lookup"><span data-stu-id="20b8d-105">The **copy** method begins a copy operation from the CD.</span></span>

``` syntax
        elementID.copy()
```

## <a name="parameters"></a><span data-ttu-id="20b8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20b8d-106">Parameters</span></span>

<span data-ttu-id="20b8d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="20b8d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20b8d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20b8d-108">Return Value</span></span>

<span data-ttu-id="20b8d-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="20b8d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20b8d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20b8d-110">Remarks</span></span>

<span data-ttu-id="20b8d-111">Diese Methode kopiert nur die aktivierten Elemente in der Wiedergabeliste und funktioniert auf die gleiche Weise wie im Bereich **aus CD kopieren** im vollständigen Modus von Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="20b8d-111">This method copies only the checked items in the playlist, and works the same way as in the **Copy from CD** pane in the full mode of Windows Media Player.</span></span> <span data-ttu-id="20b8d-112">Damit diese Methode funktioniert, muss sich eine CD auf dem CD-Laufwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="20b8d-112">For this method to work, a CD must be in the CD drive.</span></span> <span data-ttu-id="20b8d-113">Legen Sie das **checkboxesvisible** -Attribut auf "true" fest, damit Benutzer einzelne Elemente auf einer CD vor dem Kopieren auswählen können.</span><span class="sxs-lookup"><span data-stu-id="20b8d-113">Set the **checkboxesVisible** attribute to true to allow users to select individual items on a CD before copying.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b8d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20b8d-114">Requirements</span></span>



| <span data-ttu-id="20b8d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20b8d-115">Requirement</span></span> | <span data-ttu-id="20b8d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="20b8d-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="20b8d-117">Version</span><span class="sxs-lookup"><span data-stu-id="20b8d-117">Version</span></span><br/> | <span data-ttu-id="20b8d-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="20b8d-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20b8d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20b8d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b8d-120">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="20b8d-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="20b8d-121">**Wiedergabeliste. abortcopy**</span><span class="sxs-lookup"><span data-stu-id="20b8d-121">**PLAYLIST.abortCopy**</span></span>](playlist-abortcopy.md)
</dt> <dt>

[<span data-ttu-id="20b8d-122">**Wiedergabeliste. Kopieren**</span><span class="sxs-lookup"><span data-stu-id="20b8d-122">**PLAYLIST.copying**</span></span>](playlist-copying.md)
</dt> </dl>

 

 





