---
title: MCI_SETVIDEO Befehl (MMSYSTEM. h)
description: Der MCI \_ setvideo-Befehl legt Werte fest, die mit der Videowiedergabe verknüpft sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476881"
---
# <a name="mci_setvideo-command"></a><span data-ttu-id="8a190-105">Befehl "MCI \_ setvideo"</span><span class="sxs-lookup"><span data-stu-id="8a190-105">MCI\_SETVIDEO command</span></span>

<span data-ttu-id="8a190-106">Der MCI \_ setvideo-Befehl legt Werte fest, die mit der Videowiedergabe verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="8a190-106">The MCI\_SETVIDEO command sets values associated with video playback.</span></span> <span data-ttu-id="8a190-107">Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="8a190-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="8a190-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="8a190-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a><span data-ttu-id="8a190-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a190-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a190-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="8a190-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8a190-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="8a190-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8a190-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8a190-113">**MCI \_ Benachrichtigen**, **MCI- \_ Wartezeit** oder **MCI- \_ Test**.</span><span class="sxs-lookup"><span data-stu-id="8a190-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or **MCI\_TEST**.</span></span> <span data-ttu-id="8a190-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8a190-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8a190-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpsetvideo*</span><span class="sxs-lookup"><span data-stu-id="8a190-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span></span>
</dt> <dd>

<span data-ttu-id="8a190-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8a190-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8a190-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="8a190-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a190-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a190-118">Return Value</span></span>

<span data-ttu-id="8a190-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="8a190-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a190-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a190-120">Remarks</span></span>

<span data-ttu-id="8a190-121">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "Digitalvideo" verwendet:</span><span class="sxs-lookup"><span data-stu-id="8a190-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="8a190-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ setvideo \_ alg</span><span class="sxs-lookup"><span data-stu-id="8a190-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI\_DGV\_SETVIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="8a190-123">Der **lpstrinalgorithmus** -Member der Struktur, die von *lpsetvideo* identifiziert wird, enthält die Adresse eines Puffers, der den Namen eines Video Komprimierungs Algorithmus enthält.</span><span class="sxs-lookup"><span data-stu-id="8a190-123">The **lpstrAlgorithm** member of the structure identified by *lpSetVideo* contains an address of a buffer containing the name of a video compression algorithm.</span></span> <span data-ttu-id="8a190-124">Der Komprimierungs Algorithmus wird von nachfolgenden [MCI- \_ Reserve](mci-reserve.md) -oder [MCI- \_ Daten Satz](mci-record.md) Befehlen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a190-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="8a190-125">Die verfügbaren Algorithmen sind Geräte abhängig.</span><span class="sxs-lookup"><span data-stu-id="8a190-125">The available algorithms are device dependent.</span></span>

<span data-ttu-id="8a190-126">Wenn der angegebene Algorithmus nicht mit dem aktuellen Dateiformat kompatibel ist, wird das Dateiformat in das Standardformat für den Algorithmus geändert.</span><span class="sxs-lookup"><span data-stu-id="8a190-126">If the specified algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ setvideo \_ clocktime</span><span class="sxs-lookup"><span data-stu-id="8a190-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI\_DGV\_SETVIDEO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="8a190-128">Bei Verwendung mit **MCI \_ DGV \_ setvideo \_ over** gibt an, dass die Zeit in Millisekunden angegeben und die absolute Zeit ist.</span><span class="sxs-lookup"><span data-stu-id="8a190-128">When used with **MCI\_DGV\_SETVIDEO\_OVER**, indicates time is specified in milliseconds and is absolute time.</span></span> <span data-ttu-id="8a190-129">(Diese Zeit ist nicht im Schritt der Wiedergabe des Arbeitsbereichs.)</span><span class="sxs-lookup"><span data-stu-id="8a190-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="8a190-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI- \_ DGV- \_ setvideo- \_ Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a190-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI\_DGV\_SETVIDEO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="8a190-131">Ändert die **MCI \_ DGV \_ setvideo- \_ Helligkeit**, **MCI \_ DGV \_ setvideo- \_ Farbe**, **MCI \_ DGV \_ setvideo- \_ Kontrast**, **MCI \_ DGV \_ setvideo \_ Gamma**, **MCI \_ DGV \_ setvideo- \_ Schärfe** oder **MCI \_ DGV \_ setvideo \_ tint** , sodass Sie das Eingabe Signal beeinflussen und ändern, was aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="8a190-131">Modifies the **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="8a190-132">Wenn möglich, ist dies der Standardwert, wenn die Eingabe überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="8a190-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI- \_ DGV- \_ setvideo- \_ Element</span><span class="sxs-lookup"><span data-stu-id="8a190-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI\_DGV\_SETVIDEO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="8a190-134">Eine Video Konstante wird im **dwitem** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-134">A video constant is specified in the **dwItem** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-135">Die Konstante identifiziert den Wert, der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8a190-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="8a190-136">Sie können die folgenden Konstanten mit diesem Flag angeben:</span><span class="sxs-lookup"><span data-stu-id="8a190-136">You can specify the following constants with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="8a190-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI \_ AVI \_ setvideo \_ Draw- \_ Prozedur</span><span class="sxs-lookup"><span data-stu-id="8a190-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI\_AVI\_SETVIDEO\_DRAW\_PROCEDURE</span></span>
</dt> <dd>

<span data-ttu-id="8a190-138">Im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur wird eine neue Zeichnungs Prozedur Adresse angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-138">A new drawing procedure address is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-139">Sie können eine neue Zeichnungs Prozedur nur angeben, wenn sich das Gerät im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="8a190-139">You can specify a new drawing procedure only when the device is idle.</span></span> <span data-ttu-id="8a190-140">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="8a190-140">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="8a190-141">In der Zeichen folgen Befehlsschnittstelle gibt es keine Entsprechung für dieses Flag.</span><span class="sxs-lookup"><span data-stu-id="8a190-141">There is no equivalent to this flag in the string command interface.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI \_ AVI \_ setvideo \_ - \_ Palettenfarbe</span><span class="sxs-lookup"><span data-stu-id="8a190-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="8a190-143">In den Elementen **dwover** und **dwValue** der von *lpsetvideo* identifizierten Struktur wird eine neue Palettenfarbe angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-143">A new palette color is specified in the **dwOver** and **dwValue** members of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-144">Der Member **dwover** gibt den Palettenindex der zu ändernden Farbe an, und der **dwValue** -Member gibt die neue Farbe als RGB-Wert an.</span><span class="sxs-lookup"><span data-stu-id="8a190-144">The **dwOver** member specifies the palette index of the color to be changed and the **dwValue** member specifies the new color, as an RGB value.</span></span> <span data-ttu-id="8a190-145">Sie müssen auch die **MCI \_ DGV \_ setvideo \_ over** -und **MCI \_ DGV \_ setvideo- \_ wertflags** mit dem **MCI \_ DGV \_ setvideo- \_ Element** angeben, wenn Sie diese Konstante verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a190-145">You must also specify the **MCI\_DGV\_SETVIDEO\_OVER** and **MCI\_DGV\_SETVIDEO\_VALUE** flags with **MCI\_DGV\_SETVIDEO\_ITEM** when you use this constant.</span></span> <span data-ttu-id="8a190-146">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="8a190-146">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI \_ AVI \_ setvideo- \_ Palette \_ halbft1</span><span class="sxs-lookup"><span data-stu-id="8a190-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_HALFTONE</span></span>
</dt> <dd>

<span data-ttu-id="8a190-148">Gibt an, dass die "Halbton"-Palette anstelle der Standardpalette verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a190-148">Indicates that the halftone palette should be used, instead of the default palette.</span></span> <span data-ttu-id="8a190-149">Dieses Flag wird nur vom MCIAVI Digital-Video-Treiber erkannt.</span><span class="sxs-lookup"><span data-stu-id="8a190-149">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ setvideo \_ BitsPerPel</span><span class="sxs-lookup"><span data-stu-id="8a190-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI\_DGV\_SETVIDEO\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="8a190-151">Die Anzahl der Bits pro Pixel wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-151">The number of bits per pixel is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-152">Die Anzahl der Bits pro Pixel wird zum Speichern erfasster oder aufgezeichneter Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a190-152">The number of bits per pixel is used for saving captured or recorded data</span></span>

</dd> <dt>

<span data-ttu-id="8a190-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI \_ DGV \_ setvideo- \_ Helligkeit</span><span class="sxs-lookup"><span data-stu-id="8a190-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI\_DGV\_SETVIDEO\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="8a190-154">Die videohelligkeits Ebene wird als Faktor im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-154">The video brightness level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI- \_ DGV- \_ setvideo- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="8a190-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI\_DGV\_SETVIDEO\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="8a190-156">Die Farb Sättigungs Ebene der Farbe wird als Faktor für den **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-156">The video color saturation level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI- \_ DGV- \_ setvideo- \_ Kontrast</span><span class="sxs-lookup"><span data-stu-id="8a190-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI\_DGV\_SETVIDEO\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="8a190-158">Die Video Kontrast Ebene wird als Faktor für den **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-158">The video contrast level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI \_ DGV \_ setvideo- \_ Frame \_ Rate</span><span class="sxs-lookup"><span data-stu-id="8a190-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI\_DGV\_SETVIDEO\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="8a190-160">Im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur wird eine Frame Rate angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-160">A frame rate is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-161">Die Rate wird in den Rahmen Einheiten pro Sekunde 1000 angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-161">The rate is specified in units of frames per second times 1000.</span></span> <span data-ttu-id="8a190-162">Beispielsweise werden 29,97 Frames pro Sekunde als 29970 angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-162">For example, 29.97 frames per second is specified as 29970.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI \_ DGV \_ setvideo \_ Gamma</span><span class="sxs-lookup"><span data-stu-id="8a190-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI\_DGV\_SETVIDEO\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="8a190-164">Ein Gammakorrektur-Exponent-Wert wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-164">A gamma correction exponent value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-165">Gamma Korrektur passt die Zuordnung zwischen der in der Präsentations Quelle codierten Intensität und der angezeigten Helligkeit an.</span><span class="sxs-lookup"><span data-stu-id="8a190-165">Gamma correction adjusts the mapping between the intensity encoded in the presentation source and the displayed brightness.</span></span> <span data-ttu-id="8a190-166">Der Wert ist der Exponent multipliziert mit 1000.</span><span class="sxs-lookup"><span data-stu-id="8a190-166">The value is the exponent multiplied by 1000.</span></span> <span data-ttu-id="8a190-167">2200 gibt beispielsweise einen Exponenten von 2,2 an.</span><span class="sxs-lookup"><span data-stu-id="8a190-167">For example, 2200 indicates an exponent of 2.2.</span></span> <span data-ttu-id="8a190-168">Der Wert 1000 gibt einen Exponenten von 1 an, der keine Gammakorrektur anwendet.</span><span class="sxs-lookup"><span data-stu-id="8a190-168">A value of 1000 indicates an exponent of 1, which applies no gamma correction.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI- \_ DGV- \_ setvideo- \_ Schlüssel \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="8a190-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI\_DGV\_SETVIDEO\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="8a190-170">Im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur wird eine Schlüsselfarbe angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-170">A key color is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-171">Die Schlüsselfarbe ist ein RGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="8a190-171">The key color is an RGB value.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI- \_ DGV- \_ setvideo- \_ Schlüssel \_ Index</span><span class="sxs-lookup"><span data-stu-id="8a190-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI\_DGV\_SETVIDEO\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="8a190-173">Ein Schlüssel Indexwert wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-173">A key index value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-174">Der Index-Parameter ist ein physischer Palettenindex.</span><span class="sxs-lookup"><span data-stu-id="8a190-174">The index parameter is a physical palette index.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ setvideo \_ palhandle</span><span class="sxs-lookup"><span data-stu-id="8a190-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI\_DGV\_SETVIDEO\_PALHANDLE</span></span>
</dt> <dd>

<span data-ttu-id="8a190-176">Ein Palettenhandle wird im **dwValue** -Member der von *lpsetvideo* identifizierten-Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-176">A palette handle is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-177">Das Palettenhandle ist im nieder wertigen Wort enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a190-177">The palette handle is contained in the low-order word.</span></span> <span data-ttu-id="8a190-178">Digitale Videogeräte dürfen die mit diesem Befehl bestandene Palette nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-178">Digital-video devices should not free the palette passed with this command.</span></span> <span data-ttu-id="8a190-179">Anwendungen sollten Sie nach dem Schließen des Geräts freigeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-179">Applications should free it after they close the device.</span></span> <span data-ttu-id="8a190-180">Dieses Flag wird nur von Geräten unterstützt, die Paletten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a190-180">This flag is supported only by devices that use palettes.</span></span> <span data-ttu-id="8a190-181">Wenn das angegebene Palettenhandle 0 (null) ist, wird die Standardpalette verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a190-181">If this specified palette handle is zero, then the default palette is used.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI \_ DGV \_ setvideo- \_ Schärfe</span><span class="sxs-lookup"><span data-stu-id="8a190-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI\_DGV\_SETVIDEO\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="8a190-183">Ein Video-Schärfe Wert wird als Faktor im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-183">A video sharpness value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI- \_ DGV- \_ setvideo- \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="8a190-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI\_DGV\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="8a190-185">Eine Konstante, die die Quelle der Videoeingabe angibt, wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-185">A constant specifying the source of the video input is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-186">Die folgenden Konstanten sind definiert:</span><span class="sxs-lookup"><span data-stu-id="8a190-186">The following constants are defined:</span></span>

-   <span data-ttu-id="8a190-187">**MCI \_ DGV \_ setvideo \_ src \_ NTSC**: NTSC-TV.</span><span class="sxs-lookup"><span data-stu-id="8a190-187">**MCI\_DGV\_SETVIDEO\_SRC\_NTSC**: NTSC television.</span></span>
-   <span data-ttu-id="8a190-188">MCI \_ DGV \_ setvideo \_ src \_ PAL: PAL TV.</span><span class="sxs-lookup"><span data-stu-id="8a190-188">MCI\_DGV\_SETVIDEO\_SRC\_PAL: PAL television.</span></span>
-   <span data-ttu-id="8a190-189">MCI \_ DGV \_ setvideo \_ src \_ RGB: RGB-Video.</span><span class="sxs-lookup"><span data-stu-id="8a190-189">MCI\_DGV\_SETVIDEO\_SRC\_RGB: RGB video.</span></span>
-   <span data-ttu-id="8a190-190">MCI \_ DGV \_ setvideo \_ src \_ SECAM: SECAM-Fernsehen.</span><span class="sxs-lookup"><span data-stu-id="8a190-190">MCI\_DGV\_SETVIDEO\_SRC\_SECAM: SECAM television.</span></span>
-   <span data-ttu-id="8a190-191">MCI \_ DGV \_ setvideo \_ src \_ SVideo: S-Video.</span><span class="sxs-lookup"><span data-stu-id="8a190-191">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO: S-Video.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI- \_ DGV- \_ setvideo- \_ Stream</span><span class="sxs-lookup"><span data-stu-id="8a190-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI\_DGV\_SETVIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="8a190-193">Ein Videostream wird im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-193">A video stream is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-194">Der ganzzahlige Wert gibt den Videostream an, der im Arbeitsbereich wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8a190-194">The integer value specifies the video stream played back from the workspace.</span></span> <span data-ttu-id="8a190-195">Wenn der Stream nicht angegeben wird und das Dateiformat keinen Standardstream definiert, wird der erste physisch verschachtelte Videostream wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-195">If the stream is not specified and the file format does not define a default stream, the first physically interleaved video stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI \_ DGV \_ setvideo \_ tint</span><span class="sxs-lookup"><span data-stu-id="8a190-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI\_DGV\_SETVIDEO\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="8a190-197">Ein Video-Tönungs-Wert wird als Faktor im **dwValue** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-197">A video tint value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-198">Diese Anpassung wird in der Regel nach dem Tönungs-Steuerelement von vielen Farb Fernseh Sätzen modelliert, wobei 250 als grün, 750 als rot definiert und 0 (oder 1000) als Blau definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8a190-198">Typically, this adjustment is modeled after the tint control of many color television sets, with 250 defined as green, 750 defined as red, and 0 (or 1000) defined as blue.</span></span> <span data-ttu-id="8a190-199">Der nominale Wert ist immer 500.</span><span class="sxs-lookup"><span data-stu-id="8a190-199">The nominal value is always 500.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI- \_ DGV- \_ setvideo- \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8a190-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI\_DGV\_SETVIDEO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="8a190-201">Die **MCI \_ DGV \_ setvideo- \_ Helligkeit**, **MCI \_ DGV \_ setvideo \_ Color**, **MCI \_ DGV \_ setvideo- \_ Kontrast**, **MCI \_ DGV \_ setvideo \_ Gamma**, **MCI \_ DGV \_ setvideo- \_ Schärfe** oder das **MCI \_ DGV \_ setvideo \_ tint** -Flag wird so geändert, dass nur das angezeigte Signal und nicht was aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="8a190-201">The **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** flag is modified so that it affects only the displayed signal and not what is recorded.</span></span> <span data-ttu-id="8a190-202">Wenn möglich, ist dies die Standardeinstellung beim Überwachen einer Datei.</span><span class="sxs-lookup"><span data-stu-id="8a190-202">If possible, this is the default when monitoring a file.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ setvideo \_ over</span><span class="sxs-lookup"><span data-stu-id="8a190-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI\_DGV\_SETVIDEO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="8a190-204">Ein Parameter für die Übergangs Länge ist im Member **dwover** der von *lpsetvideo* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a190-204">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-205">Die Übergangs Länge gibt an, wie lange (im aktuellen Zeitformat) benötigt wird, um eine Änderung vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="8a190-205">The transition length specifies how long (in the current time format) it should take to make a change.</span></span> <span data-ttu-id="8a190-206">Wenn dieses Flag nicht verwendet wird, erfolgt die Änderung sofort.</span><span class="sxs-lookup"><span data-stu-id="8a190-206">If this flag is not used, the change occurs immediately.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI \_ DGV \_ setvideo- \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="8a190-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI\_DGV\_SETVIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="8a190-208">Der **lpstrauquality** -Member der Struktur, die von *lpsetvideo* identifiziert wird, enthält die Adresse eines Puffers, der die Videoqualität beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8a190-208">The **lpstrQuality** member of the structure identified by *lpSetVideo* contains an address of a buffer describing the video quality.</span></span> <span data-ttu-id="8a190-209">Eine Text Zeichenfolge im Puffer gibt die Merkmale des Video Komprimierungs Algorithmus an.</span><span class="sxs-lookup"><span data-stu-id="8a190-209">A text-string in the buffer specifies the characteristics of the video compression algorithm.</span></span>

<span data-ttu-id="8a190-210">Das **MCI \_ DGV \_ setvideo \_ ALG** -Flag kann verwendet werden, um einen Qualitäts Deskriptor für den angegebenen Algorithmus auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8a190-210">The **MCI\_DGV\_SETVIDEO\_ALG** flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="8a190-211">Wenn dieses Flag weggelassen wird, wird der aktuelle Algorithmus verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a190-211">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="8a190-212">Welche Algorithmen und Deskriptornamen verfügbar sind, hängt vom Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="8a190-212">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="8a190-213">Jedes Gerät bietet eine Dokumentation für die verfügbaren Algorithmen und eine Beschreibung der anwendbaren Deskriptornamen.</span><span class="sxs-lookup"><span data-stu-id="8a190-213">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="8a190-214">Mit dem [MCI- \_ Qualitäts](mci-quality.md) Befehl können zusätzliche Deskriptornamen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8a190-214">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span> <span data-ttu-id="8a190-215">Alle Geräte unterstützen die Deskriptoren "Low", "Medium" und "High".</span><span class="sxs-lookup"><span data-stu-id="8a190-215">All devices support the descriptors "low", "medium", and "high".</span></span> <span data-ttu-id="8a190-216">Der Standardwert ist Treiber spezifisch.</span><span class="sxs-lookup"><span data-stu-id="8a190-216">The default is driver specific.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI- \_ DGV- \_ setvideo- \_ Datensatz</span><span class="sxs-lookup"><span data-stu-id="8a190-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI\_DGV\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="8a190-218">Gibt an, ob Videodaten von der Aufzeichnung eingeschlossen oder ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8a190-218">Specifies whether recording includes or excludes video data.</span></span> <span data-ttu-id="8a190-219">In Kombination mit **MCI, das \_ \_ auf festgelegt** ist, werden Videodaten aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8a190-219">When combined with **MCI\_SET\_ON**, video data is recorded.</span></span> <span data-ttu-id="8a190-220">In Kombination mit der Deaktivierung **\_ \_ von MCI** werden Videodaten ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8a190-220">When combined with **MCI\_SET\_OFF**, video data is excluded.</span></span> <span data-ttu-id="8a190-221">Der Standardwert enthält Videodaten.</span><span class="sxs-lookup"><span data-stu-id="8a190-221">The default includes video data.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI \_ DGV \_ setvideo- \_ src- \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="8a190-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI\_DGV\_SETVIDEO\_SRC\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="8a190-223">Eine Zahl für die Videoquelle wird im **dwsourcenumber** -Member der von *lpsetvideo* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-223">A number for the video source is specified in the **dwSourceNumber** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-224">Wenn es mehr als eine Eingabe des Typs gibt, der durch den **MCI \_ DGV \_ setvideo- \_ Wert** angegeben wird, wählt der Wert die Eingabe aus.</span><span class="sxs-lookup"><span data-stu-id="8a190-224">If there is more than one input of the type specified by **MCI\_DGV\_SETVIDEO\_VALUE**, the value selects the input.</span></span> <span data-ttu-id="8a190-225">Dieses Flag muss immer mit der **MCI- \_ DGV- \_ setvideo- \_ Quelle** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a190-225">This flag must always be used with **MCI\_DGV\_SETVIDEO\_SOURCE**.</span></span> <span data-ttu-id="8a190-226">Wenn der **MCI \_ DGV- \_ setvideo- \_ Wert** weggelassen wird, gibt die angegebene Quellnummer jedoch die absolute zu verwendende Quelle an, wie im [MCI- \_ Listen](mci-list.md) Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-226">If **MCI\_DGV\_SETVIDEO\_VALUE** is omitted, however, the specified source number indicates the absolute source to use as specified in the [MCI\_LIST](mci-list.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI- \_ DGV- \_ setvideo \_ weiterhin</span><span class="sxs-lookup"><span data-stu-id="8a190-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI\_DGV\_SETVIDEO\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="8a190-228">Der angegebene Algorithmusname oder Qualitäts Wert gilt für weiterhin Bilder.</span><span class="sxs-lookup"><span data-stu-id="8a190-228">The algorithm name or quality value specified applies to still images.</span></span>

<span data-ttu-id="8a190-229">Jeder Gerätetreiber muss den Algorithmus "None" unterstützen, was bedeutet, dass keine Komprimierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8a190-229">Every device driver must support an algorithm of "none", which means no compression.</span></span> <span data-ttu-id="8a190-230">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="8a190-230">This is the default.</span></span> <span data-ttu-id="8a190-231">In diesem Fall speichern Digital Videogeräte weiterhin Images als RGB-geräteunabhängige Bitmaps (Disb).</span><span class="sxs-lookup"><span data-stu-id="8a190-231">In this case, digital-video devices save still images as RGB device-independent bitmaps (DIBs).</span></span>

</dd> <dt>

<span data-ttu-id="8a190-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI- \_ DGV- \_ setvideo- \_ Wert</span><span class="sxs-lookup"><span data-stu-id="8a190-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI\_DGV\_SETVIDEO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="8a190-233">Im **dwValue** -Member der durch *lpsetvideo* identifizierten Struktur ist ein Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a190-233">A value is included in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="8a190-234">Die Bedeutung des Werts wird durch das **MCI- \_ DGV- \_ setvideo \_** -elementflag angegeben.</span><span class="sxs-lookup"><span data-stu-id="8a190-234">The meaning of the value is specified by the **MCI\_DGV\_SETVIDEO\_ITEM** flag.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI- \_ festgelegt \_</span><span class="sxs-lookup"><span data-stu-id="8a190-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="8a190-236">Deaktiviert die Videoausgabe.</span><span class="sxs-lookup"><span data-stu-id="8a190-236">Disables video output.</span></span> <span data-ttu-id="8a190-237">Bei digitalen Videogeräten werden bei der Deaktivierung von Videos die Pixel im Ziel Rechteck, das durch den [MCI \_ Put](mci-put.md) -Befehl (oder der Standardwert, den Client Bereich des aktuellen Fensters) definiert ist, auf eine voll Tonfarbe festgelegt, aber Sie hat keine Auswirkung auf den Frame Puffer.</span><span class="sxs-lookup"><span data-stu-id="8a190-237">For digital-video devices, disabling video sets the pixels in the destination rectangle defined by the [MCI\_PUT](mci-put.md) command (or its default, the client region of the current window) to a solid color, but it has no effect on the frame buffer.</span></span> <span data-ttu-id="8a190-238">Wenn gewünscht, können Sie das Fenster mit dem [MCI- \_ Fenster](mci-window.md) Befehl ausblenden.</span><span class="sxs-lookup"><span data-stu-id="8a190-238">You can hide the window with the [MCI\_WINDOW](mci-window.md) command if desired.</span></span> <span data-ttu-id="8a190-239">Die Quelle des Videos, unabhängig davon, ob es sich um den Arbeitsbereich oder eine externe Eingabe handelt, speichert möglicherweise weiterhin neue Images im Frame Puffer, aber Sie werden erst angezeigt, wenn das Video aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8a190-239">The source of video, whether it's the workspace or an external input, might continue to store new images in the frame buffer, but they are not displayed until the video is enabled.</span></span> <span data-ttu-id="8a190-240">Wenngleich Anwendungen den MCI \_ setvideo-Befehl verwenden sollten, um diese Funktion zu steuern, müssen digitale Videogeräte dieses Flag weiterhin unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8a190-240">While applications should use the MCI\_SETVIDEO command to control this function, digital-video devices must still support this flag.</span></span> <span data-ttu-id="8a190-241">Der Standardwert, nachdem ein geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="8a190-241">The default value after an open is on.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ festgelegt \_ auf</span><span class="sxs-lookup"><span data-stu-id="8a190-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="8a190-243">Aktiviert die Videoausgabe.</span><span class="sxs-lookup"><span data-stu-id="8a190-243">Enables video output.</span></span>

</dd> </dl>

<span data-ttu-id="8a190-244">Für Digital Video-Geräte zeigt der *lpsetvideo* -Parameter auf eine [**MCI \_ DGV- \_ setvideo \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="8a190-244">For digital-video devices, the *lpSetVideo* parameter points to an [**MCI\_DGV\_SETVIDEO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) structure.</span></span>

<span data-ttu-id="8a190-245">Die folgenden zusätzlichen Flags werden mit dem Gerätetyp "VCR" verwendet:</span><span class="sxs-lookup"><span data-stu-id="8a190-245">The following additional flags are used with the "vcr" device type:</span></span>

<dl> <dt>

<span data-ttu-id="8a190-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI \_ VCR- \_ setvideo- \_ Datensatz</span><span class="sxs-lookup"><span data-stu-id="8a190-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI\_VCR\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="8a190-247">Legt die Videoaufzeichnung auf ein oder aus fest.</span><span class="sxs-lookup"><span data-stu-id="8a190-247">Sets the video recording to on or off.</span></span> <span data-ttu-id="8a190-248">Wird in Verbindung mit einem der folgenden Flags verwendet:</span><span class="sxs-lookup"><span data-stu-id="8a190-248">Used in conjunction with one of following flags:</span></span>

-   <span data-ttu-id="8a190-249">**MCI \_ Legen Sie \_ auf fest**.</span><span class="sxs-lookup"><span data-stu-id="8a190-249">**MCI\_SET\_ON**.</span></span> <span data-ttu-id="8a190-250">Video Aufzeichnung in.</span><span class="sxs-lookup"><span data-stu-id="8a190-250">Video recording on.</span></span>
-   <span data-ttu-id="8a190-251">**MCI \_ Legen Sie \_ aus fest**.</span><span class="sxs-lookup"><span data-stu-id="8a190-251">**MCI\_SET\_OFF**.</span></span> <span data-ttu-id="8a190-252">Video Aufzeichnung aus.</span><span class="sxs-lookup"><span data-stu-id="8a190-252">Video recording off.</span></span> <span data-ttu-id="8a190-253">Möglicherweise ist es erforderlich, zuerst die Assemblierung zu deaktivieren (mit dem Befehl [MCI \_ set](mci-set.md) , wobei das Flag **MCI \_ VCR Set assemblierungsdatensatz \_ \_ \_** auf OFF festgelegt ist), bevor die Videoaufzeichnung ausgeschaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a190-253">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the **MCI\_VCR\_SET\_ASSEMBLE\_RECORD** flag set to off) before the video recording can be turned off.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI- \_ Track</span><span class="sxs-lookup"><span data-stu-id="8a190-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="8a190-255">Der **dwtrack** -Member der durch *lpsetvideo* identifizierten Struktur gibt an, welcher Titel vom Befehl betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="8a190-255">The **dwTrack** member of the structure identified by *lpSetVideo* specifies which track is affected by the command.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI \_ VCR- \_ setvideo- \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="8a190-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI\_VCR\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="8a190-257">Legt die Videoquelle fest und muss mit dem **MCI \_ VCR \_ setvideo zum Markieren \_ von** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a190-257">Sets the video source, and must be used with the **MCI\_VCR\_SETVIDEO\_TO** flag.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI \_ VCR- \_ setvideo- \_ Monitor</span><span class="sxs-lookup"><span data-stu-id="8a190-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI\_VCR\_SETVIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="8a190-259">Legt den Video Quell Monitor fest und muss mit dem MCI \_ VCR \_ setvideo \_ zum Markieren von verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a190-259">Sets the video source monitor, and must be used with the MCI\_VCR\_SETVIDEO\_TO flag.</span></span>

</dd> <dt>

<span data-ttu-id="8a190-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI \_ VCR \_ setvideo \_ für</span><span class="sxs-lookup"><span data-stu-id="8a190-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI\_VCR\_SETVIDEO\_TO</span></span>
</dt> <dd>

<span data-ttu-id="8a190-261">Der **dwto** -Member der von *lpsetvideo* identifizierten Struktur enthält eine der folgenden Konstanten:</span><span class="sxs-lookup"><span data-stu-id="8a190-261">The **dwTo** member of the structure identified by *lpSetVideo* contains one of the following constants:</span></span>

<dl> <dd><span data-ttu-id="8a190-262">**MCI \_ VCR- \_ src- \_ \_ typtuner**</span><span class="sxs-lookup"><span data-stu-id="8a190-262">**MCI\_VCR\_SRC\_TYPE\_TUNER**</span></span></dd> <dd><span data-ttu-id="8a190-263">**MCI \_ VCR- \_ src- \_ \_ typzeile**</span><span class="sxs-lookup"><span data-stu-id="8a190-263">**MCI\_VCR\_SRC\_TYPE\_LINE**</span></span></dd> <dd><span data-ttu-id="8a190-264">**MCI \_ VCR \_ src \_ Type \_ aux**</span><span class="sxs-lookup"><span data-stu-id="8a190-264">**MCI\_VCR\_SRC\_TYPE\_AUX**</span></span></dd> <dd><span data-ttu-id="8a190-265">**MCI \_ VCR- \_ src- \_ Typ \_ generisch**</span><span class="sxs-lookup"><span data-stu-id="8a190-265">**MCI\_VCR\_SRC\_TYPE\_GENERIC**</span></span></dd> <dd><span data-ttu-id="8a190-266">**MCI \_ VCR- \_ src- \_ Typ \_ stumm schalten**</span><span class="sxs-lookup"><span data-stu-id="8a190-266">**MCI\_VCR\_SRC\_TYPE\_MUTE**</span></span></dd> <dd><span data-ttu-id="8a190-267">**Ausgabe des MCI- \_ VCR- \_ src- \_ Typs \_**</span><span class="sxs-lookup"><span data-stu-id="8a190-267">**MCI\_VCR\_SRC\_TYPE\_OUTPUT**</span></span></dd> <dd><span data-ttu-id="8a190-268">**MCI \_ VCR- \_ src- \_ Typ \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="8a190-268">**MCI\_VCR\_SRC\_TYPE\_RGB**</span></span></dd> <dd><span data-ttu-id="8a190-269">**MCI \_ VCR- \_ setvideo- \_ Nummer**</span><span class="sxs-lookup"><span data-stu-id="8a190-269">**MCI\_VCR\_SETVIDEO\_NUMBER**</span></span></dd> </dl>

<span data-ttu-id="8a190-270">Der **dwnumber** -Member der-Struktur, die von *lpsetvideo* identifiziert wird, enthält die Videoeingabe (vom Typ, der im **dwto** -Member angegeben ist), der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a190-270">The **dwNumber** member of the structure identified by *lpSetVideo* contains the video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

<span data-ttu-id="8a190-271">Bei VCR-Geräten verweist der *lpsetvideo* -Parameter auf eine [**MCI \_ VCR- \_ setvideo \_**](mci-vcr-setvideo-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="8a190-271">For VCR devices, the *lpSetVideo* parameter points to an [**MCI\_VCR\_SETVIDEO\_PARMS**](mci-vcr-setvideo-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a190-272">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a190-272">Requirements</span></span>



| <span data-ttu-id="8a190-273">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a190-273">Requirement</span></span> | <span data-ttu-id="8a190-274">Wert</span><span class="sxs-lookup"><span data-stu-id="8a190-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a190-275">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a190-275">Minimum supported client</span></span><br/> | <span data-ttu-id="8a190-276">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a190-276">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8a190-277">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a190-277">Minimum supported server</span></span><br/> | <span data-ttu-id="8a190-278">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a190-278">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8a190-279">Header</span><span class="sxs-lookup"><span data-stu-id="8a190-279">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a190-280"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a190-280"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a190-281">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a190-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a190-282">MCI</span><span class="sxs-lookup"><span data-stu-id="8a190-282">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8a190-283">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="8a190-283">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

