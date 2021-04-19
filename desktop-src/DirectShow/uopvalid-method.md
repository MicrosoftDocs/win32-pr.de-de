---
description: Die uopvalid-Methode ruft einen Wert ab, der angibt, ob der angegebene Benutzer Vorgang (User Operation, UOP) aktuell gültig ist.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Uopvalid-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359304"
---
# <a name="uopvalid-method"></a><span data-ttu-id="e0ef9-103">Uopvalid-Methode</span><span class="sxs-lookup"><span data-stu-id="e0ef9-103">UOPValid Method</span></span>

> [!Note]  
> <span data-ttu-id="e0ef9-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0ef9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e0ef9-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e0ef9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e0ef9-106">Die- `UOPValid` Methode ruft einen Wert ab, der angibt, ob der angegebene Benutzer Vorgang (User Operation, UOP) aktuell gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e0ef9-106">The `UOPValid` method retrieves a value that indicates whether the specified user operation (UOP) is currently valid.</span></span>

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a><span data-ttu-id="e0ef9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0ef9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0ef9-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iuop*</span><span class="sxs-lookup"><span data-stu-id="e0ef9-108"><span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*</span></span>
</dt> <dd>

<span data-ttu-id="e0ef9-109">Gibt den Benutzer Vorgang (User Operation, UOP) als ganze Zahl an.</span><span class="sxs-lookup"><span data-stu-id="e0ef9-109">Specifies the user operation (UOP) as an Integer.</span></span>



| <span data-ttu-id="e0ef9-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e0ef9-110">Value</span></span> | <span data-ttu-id="e0ef9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0ef9-111">Description</span></span>                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ef9-112">0</span><span class="sxs-lookup"><span data-stu-id="e0ef9-112">0</span></span>     | <span data-ttu-id="e0ef9-113">[**Playtitle**](playtitle-method.md), [**playattime**](playattime-method.md)[**playattimeingetitle**](playattimeintitle-method.md)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-113">[**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)</span></span>                                                                                      |
| <span data-ttu-id="e0ef9-114">1</span><span class="sxs-lookup"><span data-stu-id="e0ef9-114">1</span></span>     | [<span data-ttu-id="e0ef9-115">**Playchapter**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-115">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="e0ef9-116">2</span><span class="sxs-lookup"><span data-stu-id="e0ef9-116">2</span></span>     | [<span data-ttu-id="e0ef9-117">**Playtitle**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-117">**PlayTitle**</span></span>](playtitle-method.md)                                                                                                                                                                                    |
| <span data-ttu-id="e0ef9-118">3</span><span class="sxs-lookup"><span data-stu-id="e0ef9-118">3</span></span>     | [<span data-ttu-id="e0ef9-119">**Stop**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-119">**Stop**</span></span>](stop-method.md)                                                                                                                                                                                              |
| <span data-ttu-id="e0ef9-120">4</span><span class="sxs-lookup"><span data-stu-id="e0ef9-120">4</span></span>     | [<span data-ttu-id="e0ef9-121">**Returnfromsubmenu**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-121">**ReturnFromSubmenu**</span></span>](returnfromsubmenu-method.md)                                                                                                                                                                    |
| <span data-ttu-id="e0ef9-122">5</span><span class="sxs-lookup"><span data-stu-id="e0ef9-122">5</span></span>     | [<span data-ttu-id="e0ef9-123">**Playchapter**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-123">**PlayChapter**</span></span>](playchapter-method.md)                                                                                                                                                                                |
| <span data-ttu-id="e0ef9-124">6</span><span class="sxs-lookup"><span data-stu-id="e0ef9-124">6</span></span>     | <span data-ttu-id="e0ef9-125">[**Playprevchapter**](playprevchapter-method.md), [ **replaychapter**](replaychapter-method.md)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-125">[**PlayPrevChapter**](playprevchapter-method.md), [**ReplayChapter**](replaychapter-method.md)</span></span>                                                                                                                         |
| <span data-ttu-id="e0ef9-126">7</span><span class="sxs-lookup"><span data-stu-id="e0ef9-126">7</span></span>     | [<span data-ttu-id="e0ef9-127">**Playnextchapter**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-127">**PlayNextChapter**</span></span>](playnextchapter-method.md)                                                                                                                                                                        |
| <span data-ttu-id="e0ef9-128">8</span><span class="sxs-lookup"><span data-stu-id="e0ef9-128">8</span></span>     | [<span data-ttu-id="e0ef9-129">**Playforward**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-129">**PlayForwards**</span></span>](playforwards-method.md)                                                                                                                                                                              |
| <span data-ttu-id="e0ef9-130">9</span><span class="sxs-lookup"><span data-stu-id="e0ef9-130">9</span></span>     | [<span data-ttu-id="e0ef9-131">**Playrückwärts**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-131">**PlayBackwards**</span></span>](playbackwards-method.md)                                                                                                                                                                            |
| <span data-ttu-id="e0ef9-132">10</span><span class="sxs-lookup"><span data-stu-id="e0ef9-132">10</span></span>    | <span data-ttu-id="e0ef9-133">[**Showmenu**](showmenu-method.md) mit dem Parameterwert 2 (DVD- \_ \_ Menütitel)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-133">[**ShowMenu**](showmenu-method.md) with a parameter value of 2 (DVD\_MENU\_Title)</span></span>                                                                                                                                       |
| <span data-ttu-id="e0ef9-134">11</span><span class="sxs-lookup"><span data-stu-id="e0ef9-134">11</span></span>    | <span data-ttu-id="e0ef9-135">[**Showmenu**](showmenu-method.md) mit einem Parameterwert von 3 (DVD- \_ Menü Stamm \_ )</span><span class="sxs-lookup"><span data-stu-id="e0ef9-135">[**ShowMenu**](showmenu-method.md) with a parameter value of 3 (DVD\_MENU\_Root)</span></span>                                                                                                                                        |
| <span data-ttu-id="e0ef9-136">12</span><span class="sxs-lookup"><span data-stu-id="e0ef9-136">12</span></span>    | <span data-ttu-id="e0ef9-137">[**Showmenu**](showmenu-method.md) mit dem Parameterwert 4 (DVD- \_ Menü \_ Teilbild)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-137">[**ShowMenu**](showmenu-method.md) with a parameter value of 4 (DVD\_MENU\_Subpicture)</span></span>                                                                                                                                  |
| <span data-ttu-id="e0ef9-138">13</span><span class="sxs-lookup"><span data-stu-id="e0ef9-138">13</span></span>    | <span data-ttu-id="e0ef9-139">[**Showmenu**](showmenu-method.md) mit dem Parameterwert 5 (DVD \_ -Menü \_ Audiodatei)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-139">[**ShowMenu**](showmenu-method.md) with a parameter value of 5 (DVD\_MENU\_Audio)</span></span>                                                                                                                                       |
| <span data-ttu-id="e0ef9-140">14</span><span class="sxs-lookup"><span data-stu-id="e0ef9-140">14</span></span>    | <span data-ttu-id="e0ef9-141">[**Showmenu**](showmenu-method.md) mit dem Parameterwert 6 (DVD- \_ Menü \_ Winkel)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-141">[**ShowMenu**](showmenu-method.md) with a parameter value of 6 (DVD\_MENU\_Angle)</span></span>                                                                                                                                       |
| <span data-ttu-id="e0ef9-142">15</span><span class="sxs-lookup"><span data-stu-id="e0ef9-142">15</span></span>    | <span data-ttu-id="e0ef9-143">[**Showmenu**](showmenu-method.md) mit einem Parameterwert von 7 (DVD- \_ Menü \_ Kapitel)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-143">[**ShowMenu**](showmenu-method.md) with a parameter value of 7 (DVD\_MENU\_Chapter)</span></span>                                                                                                                                     |
| <span data-ttu-id="e0ef9-144">16</span><span class="sxs-lookup"><span data-stu-id="e0ef9-144">16</span></span>    | [<span data-ttu-id="e0ef9-145">**Fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-145">**Resume**</span></span>](resume-method.md)                                                                                                                                                                                          |
| <span data-ttu-id="e0ef9-146">17</span><span class="sxs-lookup"><span data-stu-id="e0ef9-146">17</span></span>    | <span data-ttu-id="e0ef9-147">[**Selecbuchstabftbutton**](selectleftbutton-method.md), [**selecseleghtbutton**](selectrightbutton-method.md), [**selectupperbutton**](selectupperbutton-method.md), [**selectlowerbutton**](selectlowerbutton-method.md)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-147">[**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md)</span></span> |
| <span data-ttu-id="e0ef9-148">18</span><span class="sxs-lookup"><span data-stu-id="e0ef9-148">18</span></span>    | [<span data-ttu-id="e0ef9-149">**Stilloff**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-149">**StillOff**</span></span>](stilloff-method.md)                                                                                                                                                                                      |
| <span data-ttu-id="e0ef9-150">19</span><span class="sxs-lookup"><span data-stu-id="e0ef9-150">19</span></span>    | [<span data-ttu-id="e0ef9-151">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-151">**Pause**</span></span>](pause-method.md)                                                                                                                                                                                            |
| <span data-ttu-id="e0ef9-152">20</span><span class="sxs-lookup"><span data-stu-id="e0ef9-152">20</span></span>    | [<span data-ttu-id="e0ef9-153">**Currentaudiostream**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-153">**CurrentAudioStream**</span></span>](currentaudiostream-property.md)                                                                                                                                                                |
| <span data-ttu-id="e0ef9-154">21</span><span class="sxs-lookup"><span data-stu-id="e0ef9-154">21</span></span>    | [<span data-ttu-id="e0ef9-155">**Currentsubpicturestream**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-155">**CurrentSubpictureStream**</span></span>](currentsubpicturestream-property.md)                                                                                                                                                      |
| <span data-ttu-id="e0ef9-156">22</span><span class="sxs-lookup"><span data-stu-id="e0ef9-156">22</span></span>    | <span data-ttu-id="e0ef9-157">[**Currentangle**](currentangle-property.md), [ **selectparamevel**](selectparentallevel-method.md)</span><span class="sxs-lookup"><span data-stu-id="e0ef9-157">[**CurrentAngle**](currentangle-property.md), [**SelectParentalLevel**](selectparentallevel-method.md)</span></span>                                                                                                                 |
| <span data-ttu-id="e0ef9-158">23</span><span class="sxs-lookup"><span data-stu-id="e0ef9-158">23</span></span>    | [<span data-ttu-id="e0ef9-159">**Karaokeaudiopressentiments ationmode**</span><span class="sxs-lookup"><span data-stu-id="e0ef9-159">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| <span data-ttu-id="e0ef9-160">24</span><span class="sxs-lookup"><span data-stu-id="e0ef9-160">24</span></span>    | <span data-ttu-id="e0ef9-161">Wählen Sie den Videomodus aus.</span><span class="sxs-lookup"><span data-stu-id="e0ef9-161">Select video mode preference.</span></span>                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0ef9-162">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0ef9-162">Return Value</span></span>

<span data-ttu-id="e0ef9-163">Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Vorgang von einem UOP-Steuerelement zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="e0ef9-163">Returns a Boolean value indicating whether the specified operation is permitted by UOP control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ef9-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ef9-164">Requirements</span></span>



| <span data-ttu-id="e0ef9-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0ef9-165">Requirement</span></span> | <span data-ttu-id="e0ef9-166">Wert</span><span class="sxs-lookup"><span data-stu-id="e0ef9-166">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ef9-167">Header</span><span class="sxs-lookup"><span data-stu-id="e0ef9-167">Header</span></span><br/> | <dl> <span data-ttu-id="e0ef9-168"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef9-168"><dt>Segment.h</dt></span></span> </dl> |



 

 




