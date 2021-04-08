---
description: Die getsprm-Methode ruft das angegebene Systemparameter Register ab.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Getsprm-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957722"
---
# <a name="getsprm-method"></a><span data-ttu-id="3263b-103">Getsprm-Methode</span><span class="sxs-lookup"><span data-stu-id="3263b-103">GetSPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="3263b-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3263b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3263b-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3263b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3263b-106">Die- `GetSPRM` Methode ruft das angegebene Systemparameter Register ab.</span><span class="sxs-lookup"><span data-stu-id="3263b-106">The `GetSPRM` method retrieves the specified system parameter register.</span></span>

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="3263b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3263b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3263b-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="3263b-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="3263b-109">Gibt das Register an, dessen Wert Sie als ganze Zahl abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="3263b-109">Specifies the register whose value you want to retrieve as an Integer.</span></span> <span data-ttu-id="3263b-110">Der ganzzahlige Wert muss zwischen 0 und 23 liegen.</span><span class="sxs-lookup"><span data-stu-id="3263b-110">The Integer must range from 0 through 23.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3263b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3263b-111">Return Value</span></span>

<span data-ttu-id="3263b-112">Gibt einen ganzzahligen Wert zurück, der den Inhalt des angegebenen Registers darstellt.</span><span class="sxs-lookup"><span data-stu-id="3263b-112">Returns an integer value representing the contents of the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3263b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3263b-113">Remarks</span></span>

<span data-ttu-id="3263b-114">Der Disc steuert die Systemparameter Register (sprms).</span><span class="sxs-lookup"><span data-stu-id="3263b-114">The disc controls system parameter registers (SPRMs).</span></span> <span data-ttu-id="3263b-115">Eine Player Anwendung muss nicht auf diese Register für eine standardmäßige Navigations Funktionalität zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3263b-115">A player application doesn't need to access these registers for any standard navigation functionality.</span></span> <span data-ttu-id="3263b-116">Sprms stellt den Status des Players dar.</span><span class="sxs-lookup"><span data-stu-id="3263b-116">SPRMs represent the status of the player.</span></span> <span data-ttu-id="3263b-117">Jede verfügt über eine Bedeutung, die durch Benutzereinstellungen, Disk-Befehle und andere vorkommen, auf die eine Anwendung keine direkte Kontrolle hat, festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3263b-117">Each one has a meaning, set by user preferences, disc commands, and other occurrences that an application has no direct control over.</span></span> <span data-ttu-id="3263b-118">Eine Anwendung kann diese Register lesen, aber nicht in Sie schreiben.</span><span class="sxs-lookup"><span data-stu-id="3263b-118">An application can read these registers but cannot write to them.</span></span> <span data-ttu-id="3263b-119">Um diese Register effektiv zu verwenden, benötigen Sie wahrscheinlich ausführlichere Informationen über die DVD-Navigations Befehle als in dieser Dokumentation bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3263b-119">To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation.</span></span> <span data-ttu-id="3263b-120">In der folgenden Tabelle werden die Inhalte der einzelnen Register aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3263b-120">The following table shows the contents of each register.</span></span> <span data-ttu-id="3263b-121">Ausführlichere Informationen zum Register Inhalt finden Sie unter [ **IDvdInfo2:: getallsprms**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span><span class="sxs-lookup"><span data-stu-id="3263b-121">For more detailed information on the register contents, see [**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span></span>



| <span data-ttu-id="3263b-122">Registrieren</span><span class="sxs-lookup"><span data-stu-id="3263b-122">Register</span></span> | <span data-ttu-id="3263b-123">Inhalte</span><span class="sxs-lookup"><span data-stu-id="3263b-123">Contents</span></span>                        |
|----------|---------------------------------|
| <span data-ttu-id="3263b-124">0</span><span class="sxs-lookup"><span data-stu-id="3263b-124">0</span></span>        | <span data-ttu-id="3263b-125">Menü Sprachcode</span><span class="sxs-lookup"><span data-stu-id="3263b-125">Menu language code</span></span>              |
| <span data-ttu-id="3263b-126">1</span><span class="sxs-lookup"><span data-stu-id="3263b-126">1</span></span>        | <span data-ttu-id="3263b-127">Audiostreamnummer</span><span class="sxs-lookup"><span data-stu-id="3263b-127">Audio stream number</span></span>             |
| <span data-ttu-id="3263b-128">2</span><span class="sxs-lookup"><span data-stu-id="3263b-128">2</span></span>        | <span data-ttu-id="3263b-129">Subbild-streamnummer</span><span class="sxs-lookup"><span data-stu-id="3263b-129">Subpicture stream number</span></span>        |
| <span data-ttu-id="3263b-130">3</span><span class="sxs-lookup"><span data-stu-id="3263b-130">3</span></span>        | <span data-ttu-id="3263b-131">Aktuelle Winkel Zahl</span><span class="sxs-lookup"><span data-stu-id="3263b-131">Current angle number</span></span>            |
| <span data-ttu-id="3263b-132">4</span><span class="sxs-lookup"><span data-stu-id="3263b-132">4</span></span>        | <span data-ttu-id="3263b-133">Aktuelle Titel Nummer</span><span class="sxs-lookup"><span data-stu-id="3263b-133">Current title number</span></span>            |
| <span data-ttu-id="3263b-134">5</span><span class="sxs-lookup"><span data-stu-id="3263b-134">5</span></span>        | <span data-ttu-id="3263b-135">Titel Nummer</span><span class="sxs-lookup"><span data-stu-id="3263b-135">Title number</span></span>                    |
| <span data-ttu-id="3263b-136">6</span><span class="sxs-lookup"><span data-stu-id="3263b-136">6</span></span>        | <span data-ttu-id="3263b-137">PGC-Nummer</span><span class="sxs-lookup"><span data-stu-id="3263b-137">PGC number</span></span>                      |
| <span data-ttu-id="3263b-138">7</span><span class="sxs-lookup"><span data-stu-id="3263b-138">7</span></span>        | <span data-ttu-id="3263b-139">Aktuelle Kapitel Nummer (PTT)</span><span class="sxs-lookup"><span data-stu-id="3263b-139">Current chapter number (PTT)</span></span>    |
| <span data-ttu-id="3263b-140">8</span><span class="sxs-lookup"><span data-stu-id="3263b-140">8</span></span>        | <span data-ttu-id="3263b-141">Markierte Schaltflächen Nummer</span><span class="sxs-lookup"><span data-stu-id="3263b-141">Highlighted button number</span></span>       |
| <span data-ttu-id="3263b-142">9</span><span class="sxs-lookup"><span data-stu-id="3263b-142">9</span></span>        | <span data-ttu-id="3263b-143">Navigationszeit Geber</span><span class="sxs-lookup"><span data-stu-id="3263b-143">Navigation timer</span></span>                |
| <span data-ttu-id="3263b-144">10</span><span class="sxs-lookup"><span data-stu-id="3263b-144">10</span></span>       | <span data-ttu-id="3263b-145">PGC-Sprung für Navigations Tool.</span><span class="sxs-lookup"><span data-stu-id="3263b-145">PGC jump for nav.</span></span> <span data-ttu-id="3263b-146">Timer</span><span class="sxs-lookup"><span data-stu-id="3263b-146">timer</span></span>         |
| <span data-ttu-id="3263b-147">11</span><span class="sxs-lookup"><span data-stu-id="3263b-147">11</span></span>       | <span data-ttu-id="3263b-148">Modus für die Karaoke-Audiopräsentation</span><span class="sxs-lookup"><span data-stu-id="3263b-148">Karaoke audio presentation mode</span></span> |
| <span data-ttu-id="3263b-149">12</span><span class="sxs-lookup"><span data-stu-id="3263b-149">12</span></span>       | <span data-ttu-id="3263b-150">PML-Land-/Regionscode</span><span class="sxs-lookup"><span data-stu-id="3263b-150">PML country/region code</span></span>         |
| <span data-ttu-id="3263b-151">13</span><span class="sxs-lookup"><span data-stu-id="3263b-151">13</span></span>       | <span data-ttu-id="3263b-152">PML</span><span class="sxs-lookup"><span data-stu-id="3263b-152">PML</span></span>                             |
| <span data-ttu-id="3263b-153">14</span><span class="sxs-lookup"><span data-stu-id="3263b-153">14</span></span>       | <span data-ttu-id="3263b-154">Video Einstellung</span><span class="sxs-lookup"><span data-stu-id="3263b-154">Video setting</span></span>                   |
| <span data-ttu-id="3263b-155">15</span><span class="sxs-lookup"><span data-stu-id="3263b-155">15</span></span>       | <span data-ttu-id="3263b-156">Audiofunktion</span><span class="sxs-lookup"><span data-stu-id="3263b-156">Audio capability</span></span>                |
| <span data-ttu-id="3263b-157">16</span><span class="sxs-lookup"><span data-stu-id="3263b-157">16</span></span>       | <span data-ttu-id="3263b-158">Audiosprache</span><span class="sxs-lookup"><span data-stu-id="3263b-158">Audio language</span></span>                  |
| <span data-ttu-id="3263b-159">17</span><span class="sxs-lookup"><span data-stu-id="3263b-159">17</span></span>       | <span data-ttu-id="3263b-160">Erweiterung für Audiosprache</span><span class="sxs-lookup"><span data-stu-id="3263b-160">Audio language extension</span></span>        |
| <span data-ttu-id="3263b-161">18</span><span class="sxs-lookup"><span data-stu-id="3263b-161">18</span></span>       | <span data-ttu-id="3263b-162">Unter Bildsprache</span><span class="sxs-lookup"><span data-stu-id="3263b-162">Subpicture language</span></span>             |
| <span data-ttu-id="3263b-163">19</span><span class="sxs-lookup"><span data-stu-id="3263b-163">19</span></span>       | <span data-ttu-id="3263b-164">Teil Bild Spracherweiterung</span><span class="sxs-lookup"><span data-stu-id="3263b-164">Subpicture language extension</span></span>   |
| <span data-ttu-id="3263b-165">20</span><span class="sxs-lookup"><span data-stu-id="3263b-165">20</span></span>       | <span data-ttu-id="3263b-166">Player Regions Code</span><span class="sxs-lookup"><span data-stu-id="3263b-166">Player region code</span></span>              |
| <span data-ttu-id="3263b-167">21</span><span class="sxs-lookup"><span data-stu-id="3263b-167">21</span></span>       | <span data-ttu-id="3263b-168">Reserviert</span><span class="sxs-lookup"><span data-stu-id="3263b-168">Reserved</span></span>                        |
| <span data-ttu-id="3263b-169">22</span><span class="sxs-lookup"><span data-stu-id="3263b-169">22</span></span>       | <span data-ttu-id="3263b-170">Reserviert</span><span class="sxs-lookup"><span data-stu-id="3263b-170">Reserved</span></span>                        |
| <span data-ttu-id="3263b-171">23</span><span class="sxs-lookup"><span data-stu-id="3263b-171">23</span></span>       | <span data-ttu-id="3263b-172">Reserviert</span><span class="sxs-lookup"><span data-stu-id="3263b-172">Reserved</span></span>                        |



 

## <a name="see-also"></a><span data-ttu-id="3263b-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3263b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3263b-174">**Getgprm**</span><span class="sxs-lookup"><span data-stu-id="3263b-174">**GetGPRM**</span></span>](getgprm-method.md)
</dt> <dt>

[<span data-ttu-id="3263b-175">**Setgprm**</span><span class="sxs-lookup"><span data-stu-id="3263b-175">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



