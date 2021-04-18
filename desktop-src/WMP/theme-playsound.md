---
title: Theme. PlaySound
description: Die PlaySound-Methode gibt die angegebene Audiodatei wieder.
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- Design. PlaySound-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372404"
---
# <a name="themeplaysound"></a><span data-ttu-id="8a7aa-104">Theme. PlaySound</span><span class="sxs-lookup"><span data-stu-id="8a7aa-104">THEME.playSound</span></span>

<span data-ttu-id="8a7aa-105">Die **PlaySound** -Methode gibt die angegebene Audiodatei wieder.</span><span class="sxs-lookup"><span data-stu-id="8a7aa-105">The **playSound** method plays the specified sound file.</span></span>

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a><span data-ttu-id="8a7aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a7aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a7aa-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span><span class="sxs-lookup"><span data-stu-id="8a7aa-107"><span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*</span></span>
</dt> <dd>

<span data-ttu-id="8a7aa-108">Eine **Zeichenfolge** , die den Namen der zu Wiedergabe enden Audiodatei angibt.</span><span class="sxs-lookup"><span data-stu-id="8a7aa-108">A **String** specifying the name of the sound file to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a7aa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a7aa-109">Return Value</span></span>

<span data-ttu-id="8a7aa-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a7aa-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a7aa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a7aa-111">Remarks</span></span>

<span data-ttu-id="8a7aa-112">Diese Methode ermöglicht das Hinzufügen von Soundeffekten zu einer Skin, wenn beispielsweise auf Schaltflächen geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="8a7aa-112">This method allows you to add sound effects to a skin for example, when buttons are clicked.</span></span> <span data-ttu-id="8a7aa-113">Der Sound wird vom Betriebssystem direkt und nicht von Windows Media Player abgespielt.</span><span class="sxs-lookup"><span data-stu-id="8a7aa-113">The sound is played by the operating system directly and not by Windows Media Player.</span></span> <span data-ttu-id="8a7aa-114">Dies bedeutet, dass der Sound nicht mit Windows Media Player-Einstellungen und-Methoden gesteuert werden kann. er kann jedoch abgespielt werden, während Windows Media Player eine andere digitale Mediendatei wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="8a7aa-114">This means that the sound cannot be controlled with Windows Media Player settings and methods, but it can be played while Windows Media Player is playing another digital media file.</span></span>

<span data-ttu-id="8a7aa-115">Diese Methode unterstützt nur WAV-Dateien.</span><span class="sxs-lookup"><span data-stu-id="8a7aa-115">This method supports WAV files only.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7aa-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a7aa-116">Requirements</span></span>



| <span data-ttu-id="8a7aa-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a7aa-117">Requirement</span></span> | <span data-ttu-id="8a7aa-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8a7aa-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8a7aa-119">Version</span><span class="sxs-lookup"><span data-stu-id="8a7aa-119">Version</span></span><br/> | <span data-ttu-id="8a7aa-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="8a7aa-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a7aa-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a7aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7aa-122">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="8a7aa-122">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





