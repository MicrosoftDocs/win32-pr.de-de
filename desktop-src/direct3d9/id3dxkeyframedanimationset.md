---
description: Eine Anwendung verwendet die Methoden dieser Schnittstelle, um einen Keyframe-Animations Satz zu implementieren.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: ID3DXKeyframedAnimationSet-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360232"
---
# <a name="id3dxkeyframedanimationset-interface"></a><span data-ttu-id="d73ea-103">ID3DXKeyframedAnimationSet-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d73ea-103">ID3DXKeyframedAnimationSet interface</span></span>

<span data-ttu-id="d73ea-104">Eine Anwendung verwendet die Methoden dieser Schnittstelle, um einen Keyframe-Animations Satz zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d73ea-104">An application uses the methods of this interface to implement a key frame animation set.</span></span>

## <a name="members"></a><span data-ttu-id="d73ea-105">Member</span><span class="sxs-lookup"><span data-stu-id="d73ea-105">Members</span></span>

<span data-ttu-id="d73ea-106">Die **ID3DXKeyframedAnimationSet** -Schnittstelle erbt von [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="d73ea-106">The **ID3DXKeyframedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="d73ea-107">**ID3DXKeyframedAnimationSet** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d73ea-107">**ID3DXKeyframedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="d73ea-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="d73ea-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d73ea-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d73ea-109">Methods</span></span>

<span data-ttu-id="d73ea-110">Die **ID3DXKeyframedAnimationSet** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d73ea-110">The **ID3DXKeyframedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="d73ea-111">Methode</span><span class="sxs-lookup"><span data-stu-id="d73ea-111">Method</span></span>                                                                                   | <span data-ttu-id="d73ea-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d73ea-112">Description</span></span>                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d73ea-113">**Komprimieren**</span><span class="sxs-lookup"><span data-stu-id="d73ea-113">**Compress**</span></span>](id3dxkeyframedanimationset--compress.md)                                 | <span data-ttu-id="d73ea-114">Wandelt Animationen in einem Animations Satz in ein komprimiertes Format um und gibt einen Zeiger auf den Puffer zurück, in dem die komprimierten Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d73ea-114">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span><br/> |
| [<span data-ttu-id="d73ea-115">**Getcallbackkey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-115">**GetCallbackKey**</span></span>](id3dxkeyframedanimationset--getcallbackkey.md)                     | <span data-ttu-id="d73ea-116">Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="d73ea-116">Gets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="d73ea-117">**Getcallbackkeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-117">**GetCallbackKeys**</span></span>](id3dxkeyframedanimationset--getcallbackkeys.md)                   | <span data-ttu-id="d73ea-118">Füllt ein Array mit Rückruf Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d73ea-118">Fills an array with callback key data used for key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="d73ea-119">**Getnumcallbackkeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-119">**GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | <span data-ttu-id="d73ea-120">Ruft die Anzahl der Rückruf Schlüssel im Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="d73ea-120">Gets the number of callback keys in the animation set.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d73ea-121">**Getnumrotationkeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-121">**GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)             | <span data-ttu-id="d73ea-122">Ruft die Anzahl von Rotations Schlüsseln in der angegebenen Keyframe-Animation ab.</span><span class="sxs-lookup"><span data-stu-id="d73ea-122">Gets the number of rotation keys in the specified key frame animation.</span></span><br/>                                                                  |
| [<span data-ttu-id="d73ea-123">**Getnumscalekeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-123">**GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)                   | <span data-ttu-id="d73ea-124">Ruft die Anzahl der Skalierungs Schlüssel in der angegebenen Keyframe-Animation ab.</span><span class="sxs-lookup"><span data-stu-id="d73ea-124">Gets the number of scale keys in the specified key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="d73ea-125">**Getnumtranslationkeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-125">**GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | <span data-ttu-id="d73ea-126">Ruft die Anzahl der Übersetzungsschlüssel in der angegebenen Keyframe-Animation ab.</span><span class="sxs-lookup"><span data-stu-id="d73ea-126">Gets the number of translation keys in the specified key frame animation.</span></span><br/>                                                               |
| [<span data-ttu-id="d73ea-127">**Getplaybacktype**</span><span class="sxs-lookup"><span data-stu-id="d73ea-127">**GetPlaybackType**</span></span>](id3dxkeyframedanimationset--getplaybacktype.md)                   | <span data-ttu-id="d73ea-128">Ruft den Typ der Wiedergabe Schleife für Animations Sätze ab.</span><span class="sxs-lookup"><span data-stu-id="d73ea-128">Gets the type of the animation set playback loop.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d73ea-129">**Getrotationkey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-129">**GetRotationKey**</span></span>](id3dxkeyframedanimationset--getrotationkey.md)                     | <span data-ttu-id="d73ea-130">Sie erhalten die Rotations Informationen für einen bestimmten Keyframe im Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="d73ea-130">Get rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="d73ea-131">**Getrotationkeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-131">**GetRotationKeys**</span></span>](id3dxkeyframedanimationset--getrotationkeys.md)                   | <span data-ttu-id="d73ea-132">Füllt ein Array mit rotierenden Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d73ea-132">Fills an array with rotational key data used for key frame animation.</span></span><br/>                                                                   |
| [<span data-ttu-id="d73ea-133">**Getscalekey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-133">**GetScaleKey**</span></span>](id3dxkeyframedanimationset--getscalekey.md)                           | <span data-ttu-id="d73ea-134">Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz erhalten.</span><span class="sxs-lookup"><span data-stu-id="d73ea-134">Get scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="d73ea-135">**Getscalekeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-135">**GetScaleKeys**</span></span>](id3dxkeyframedanimationset--getscalekeys.md)                         | <span data-ttu-id="d73ea-136">Füllt ein Array mit Skalierungs Schlüsseldaten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d73ea-136">Fills an array with scale key data used for key frame animation.</span></span><br/>                                                                        |
| [<span data-ttu-id="d73ea-137">**Getsourcetickspersecond**</span><span class="sxs-lookup"><span data-stu-id="d73ea-137">**GetSourceTicksPerSecond**</span></span>](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | <span data-ttu-id="d73ea-138">Ruft die Anzahl der pro Sekunde auftretenden Animations Tastatur-Frame Ticks ab.</span><span class="sxs-lookup"><span data-stu-id="d73ea-138">Gets the number of animation key frame ticks that occur per second.</span></span><br/>                                                                     |
| [<span data-ttu-id="d73ea-139">**Gettranslationkey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-139">**GetTranslationKey**</span></span>](id3dxkeyframedanimationset--gettranslationkey.md)               | <span data-ttu-id="d73ea-140">Sie erhalten Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="d73ea-140">Get translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="d73ea-141">**Gettranslationkeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-141">**GetTranslationKeys**</span></span>](id3dxkeyframedanimationset--gettranslationkeys.md)             | <span data-ttu-id="d73ea-142">Füllt ein Array mit Translational Key-Daten, die für die Keyframe-Animation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d73ea-142">Fills an array with translational key data used for key frame animation.</span></span><br/>                                                                |
| [<span data-ttu-id="d73ea-143">**Registeranimationsrtkeys**</span><span class="sxs-lookup"><span data-stu-id="d73ea-143">**RegisterAnimationSRTKeys**</span></span>](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | <span data-ttu-id="d73ea-144">Registrieren der schlüsselrahmen Daten für die Skalierung, Drehung und Übersetzung (SRT) für eine Animation.</span><span class="sxs-lookup"><span data-stu-id="d73ea-144">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span><br/>                                                        |
| [<span data-ttu-id="d73ea-145">**Setcallbackkey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-145">**SetCallbackKey**</span></span>](id3dxkeyframedanimationset--setcallbackkey.md)                     | <span data-ttu-id="d73ea-146">Legt Informationen zu einem bestimmten Rückruf im Animations Satz fest.</span><span class="sxs-lookup"><span data-stu-id="d73ea-146">Sets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="d73ea-147">**"".**</span><span class="sxs-lookup"><span data-stu-id="d73ea-147">**SetRotationKey**</span></span>](id3dxkeyframedanimationset--setrotationkey.md)                     | <span data-ttu-id="d73ea-148">Legen Sie die Rotations Informationen für einen bestimmten Keyframe im Animations Satz fest.</span><span class="sxs-lookup"><span data-stu-id="d73ea-148">Set rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="d73ea-149">**Setscalekey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-149">**SetScaleKey**</span></span>](id3dxkeyframedanimationset--setscalekey.md)                           | <span data-ttu-id="d73ea-150">Legen Sie Skalierungsinformationen für einen bestimmten Keyframe im Animations Satz fest.</span><span class="sxs-lookup"><span data-stu-id="d73ea-150">Set scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="d73ea-151">**Settranslationkey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-151">**SetTranslationKey**</span></span>](id3dxkeyframedanimationset--settranslationkey.md)               | <span data-ttu-id="d73ea-152">Legen Sie Übersetzungs Informationen für einen bestimmten Keyframe im Animations Satz fest.</span><span class="sxs-lookup"><span data-stu-id="d73ea-152">Set translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="d73ea-153">**Unregisteranimation**</span><span class="sxs-lookup"><span data-stu-id="d73ea-153">**UnregisterAnimation**</span></span>](id3dxkeyframedanimationset--unregisteranimation.md)           | <span data-ttu-id="d73ea-154">Entfernen Sie die Animationsdaten aus dem Animations Satz.</span><span class="sxs-lookup"><span data-stu-id="d73ea-154">Remove the animation data from the animation set.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d73ea-155">**Unregisterrotationkey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-155">**UnregisterRotationKey**</span></span>](id3dxkeyframedanimationset--unregisterrotationkey.md)       | <span data-ttu-id="d73ea-156">Entfernt die Rotationsdaten am angegebenen Keyframe.</span><span class="sxs-lookup"><span data-stu-id="d73ea-156">Removes the rotation data at the specified key frame.</span></span><br/>                                                                                   |
| [<span data-ttu-id="d73ea-157">**Unregisterscalekey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-157">**UnregisterScaleKey**</span></span>](id3dxkeyframedanimationset--unregisterscalekey.md)             | <span data-ttu-id="d73ea-158">Entfernt die Skalierungs Daten am angegebenen Keyframe.</span><span class="sxs-lookup"><span data-stu-id="d73ea-158">Removes the scale data at the specified key frame.</span></span><br/>                                                                                      |
| [<span data-ttu-id="d73ea-159">**Unregistertranslationkey**</span><span class="sxs-lookup"><span data-stu-id="d73ea-159">**UnregisterTranslationKey**</span></span>](id3dxkeyframedanimationset--unregistertranslationkey.md) | <span data-ttu-id="d73ea-160">Entfernt die Übersetzungs Daten am angegebenen Keyframe.</span><span class="sxs-lookup"><span data-stu-id="d73ea-160">Removes the translation data at the specified key frame.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="d73ea-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d73ea-161">Remarks</span></span>

<span data-ttu-id="d73ea-162">Erstellen Sie einen keyframed-Animations Satz mit [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="d73ea-162">Create a keyframed animation set with [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span></span>

<span data-ttu-id="d73ea-163">Der LPD3DXKEYFRAMEDANIMATIONSET-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="d73ea-163">The LPD3DXKEYFRAMEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="d73ea-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d73ea-164">Requirements</span></span>



| <span data-ttu-id="d73ea-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d73ea-165">Requirement</span></span> | <span data-ttu-id="d73ea-166">Wert</span><span class="sxs-lookup"><span data-stu-id="d73ea-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d73ea-167">Header</span><span class="sxs-lookup"><span data-stu-id="d73ea-167">Header</span></span><br/>  | <dl> <span data-ttu-id="d73ea-168"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d73ea-168"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d73ea-169">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d73ea-169">Library</span></span><br/> | <dl> <span data-ttu-id="d73ea-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d73ea-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d73ea-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d73ea-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73ea-172">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="d73ea-172">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="d73ea-173">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d73ea-173">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




