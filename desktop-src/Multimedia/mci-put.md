---
title: MCI_PUT Befehl (MMSYSTEM. h)
description: Mit dem Befehl MCI \_ Put werden die Quell-, Ziel-und Frame Rechtecke festgelegt. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- MCI_PUT Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106538"
---
# <a name="mci_put-command"></a><span data-ttu-id="949ce-105">Befehl "MCI \_ Put"</span><span class="sxs-lookup"><span data-stu-id="949ce-105">MCI\_PUT command</span></span>

<span data-ttu-id="949ce-106">Mit dem Befehl MCI \_ Put werden die Quell-, Ziel-und Frame Rechtecke festgelegt.</span><span class="sxs-lookup"><span data-stu-id="949ce-106">The MCI\_PUT command sets the source, destination, and frame rectangles.</span></span> <span data-ttu-id="949ce-107">Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="949ce-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="949ce-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="949ce-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="949ce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="949ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="949ce-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="949ce-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="949ce-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="949ce-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="949ce-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="949ce-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="949ce-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="949ce-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="949ce-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="949ce-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpdest*</span><span class="sxs-lookup"><span data-stu-id="949ce-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="949ce-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="949ce-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="949ce-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="949ce-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="949ce-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="949ce-118">Return Value</span></span>

<span data-ttu-id="949ce-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="949ce-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="949ce-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="949ce-120">Remarks</span></span>

<span data-ttu-id="949ce-121">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="949ce-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="949ce-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI- \_ DGV- \_ Put- \_ Client</span><span class="sxs-lookup"><span data-stu-id="949ce-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI\_DGV\_PUT\_CLIENT</span></span>
</dt> <dd>

<span data-ttu-id="949ce-123">Das für MCI \_ DGV- \_ Rect definierte Rechteck gilt für die Position des Client Fensters.</span><span class="sxs-lookup"><span data-stu-id="949ce-123">The rectangle defined for MCI\_DGV\_RECT applies to the position of the client window.</span></span> <span data-ttu-id="949ce-124">Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Anzeige Fensters.</span><span class="sxs-lookup"><span data-stu-id="949ce-124">The rectangle specified is relative to the parent window of the display window.</span></span> <span data-ttu-id="949ce-125">Das MCI- \_ DGV- \_ Put- \_ Fenster muss gleichzeitig mit diesem Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="949ce-125">MCI\_DGV\_PUT\_WINDOW must be set concurrently with this flag.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI- \_ DGV- \_ Put- \_ Ziel</span><span class="sxs-lookup"><span data-stu-id="949ce-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI\_DGV\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="949ce-127">Das Rechteck, das für MCI \_ DGV-Rect definiert ist, \_ gibt ein Ziel Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="949ce-127">The rectangle defined for MCI\_DGV\_RECT specifies a destination rectangle.</span></span> <span data-ttu-id="949ce-128">Das Ziel Rechteck gibt den Teil des Client Fensters an, der dieser Gerätetreiber Instanz zugeordnet ist, in der das Bild oder das Video angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="949ce-128">The destination rectangle specifies the portion of the client window associated with this device driver instance that shows the image or video.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI- \_ DGV- \_ Put- \_ Frame</span><span class="sxs-lookup"><span data-stu-id="949ce-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI\_DGV\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="949ce-130">Das für MCI \_ DGV- \_ Rect definierte Rechteck gilt für das Frame Rechteck.</span><span class="sxs-lookup"><span data-stu-id="949ce-130">The rectangle defined for MCI\_DGV\_RECT applies to the frame rectangle.</span></span> <span data-ttu-id="949ce-131">Das Rahmen Rechteck gibt den Teil des Frame Puffers an, der als Ziel der Videobilder aus dem Video Rechteck verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="949ce-131">The frame rectangle specifies the portion of the frame buffer used as the destination of the video images obtained from the video rectangle.</span></span> <span data-ttu-id="949ce-132">Das Video sollte so skaliert werden, dass es in das Frame Puffer Rechteck passt.</span><span class="sxs-lookup"><span data-stu-id="949ce-132">The video should be scaled to fit within the frame buffer rectangle.</span></span>

<span data-ttu-id="949ce-133">Das Rechteck wird in den Rahmen Puffer Koordinaten angegeben.</span><span class="sxs-lookup"><span data-stu-id="949ce-133">The rectangle is specified in frame buffer coordinates.</span></span> <span data-ttu-id="949ce-134">Das Standard Rechteck ist der vollständige Frame Puffer.</span><span class="sxs-lookup"><span data-stu-id="949ce-134">The default rectangle is the full frame buffer.</span></span> <span data-ttu-id="949ce-135">Das Angeben dieses Rechtecks ermöglicht dem Gerät das Skalieren des Bilds beim digitsieren der Daten.</span><span class="sxs-lookup"><span data-stu-id="949ce-135">Specifying this rectangle lets the device scale the image as it digitizes the data.</span></span> <span data-ttu-id="949ce-136">Geräte, die das Abbild nicht skalieren können, lehnen diesen Befehl mit nicht unterstützter mcierr- \_ \_ Funktion ab</span><span class="sxs-lookup"><span data-stu-id="949ce-136">Devices that cannot scale the image reject this command with MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="949ce-137">Sie können das Flag MCI \_ getdevcaps \_ - \_ streckungs Flag mit dem [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl verwenden, um zu bestimmen, ob ein Gerät das Image skaliert.</span><span class="sxs-lookup"><span data-stu-id="949ce-137">You can use the MCI\_GETDEVCAPS\_CAN\_STRETCH flag with the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command to determine if a device scales the image.</span></span> <span data-ttu-id="949ce-138">Ein Gerät gibt **false** zurück, wenn das Abbild nicht skaliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="949ce-138">A device returns **FALSE** if it cannot scale the image.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI \_ DGV \_ Put- \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="949ce-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI\_DGV\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="949ce-140">Das für MCI \_ DGV- \_ Rect definierte Rechteck gibt ein Quell Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="949ce-140">The rectangle defined for MCI\_DGV\_RECT specifies a source rectangle.</span></span> <span data-ttu-id="949ce-141">Das Quell Rechteck gibt an, welcher Teil des Frame Puffers skaliert werden soll, um in das Ziel Rechteck zu passen.</span><span class="sxs-lookup"><span data-stu-id="949ce-141">The source rectangle specifies which portion of the frame buffer is to be scaled to fit into the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI \_ DGV \_ Put- \_ Video</span><span class="sxs-lookup"><span data-stu-id="949ce-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI\_DGV\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="949ce-143">Das für MCI \_ DGV \_ Rect definierte Rechteck gilt für das Video Rechteck.</span><span class="sxs-lookup"><span data-stu-id="949ce-143">The rectangle defined for MCI\_DGV\_RECT applies to the video rectangle.</span></span> <span data-ttu-id="949ce-144">Das Video Rechteck gibt an, welcher Teil der aktuellen Präsentations Quelle im Frame Puffer gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="949ce-144">The video rectangle specifies which portion of the current presentation source is stored in the frame buffer.</span></span> <span data-ttu-id="949ce-145">Das Rechteck wird mithilfe der natürlichen Koordinaten der Präsentations Quelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="949ce-145">The rectangle is specified using the natural coordinates of the presentation source.</span></span> <span data-ttu-id="949ce-146">Sie ermöglicht das anschneiden, das vor dem Speichern von Bildern und Videos im Frame Puffer auftritt.</span><span class="sxs-lookup"><span data-stu-id="949ce-146">It allows the specification of cropping that occurs prior to storing images and video in the frame buffer.</span></span> <span data-ttu-id="949ce-147">Das Standard Rechteck ist der vollständige aktive Scanbereich oder die vollständigen entkomprimierten Bilder und das Video.</span><span class="sxs-lookup"><span data-stu-id="949ce-147">The default rectangle is the full active scan area or the full decompressed images and video.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI- \_ DGV- \_ Put- \_ Fenster</span><span class="sxs-lookup"><span data-stu-id="949ce-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI\_DGV\_PUT\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="949ce-149">Das für MCI \_ DGV- \_ Rect definierte Rechteck gilt für das Anzeige Fenster.</span><span class="sxs-lookup"><span data-stu-id="949ce-149">The rectangle defined for MCI\_DGV\_RECT applies to the display window.</span></span> <span data-ttu-id="949ce-150">Dieses Rechteck ist relativ zum übergeordneten Fenster des Anzeige Fensters (in der Regel der Desktop).</span><span class="sxs-lookup"><span data-stu-id="949ce-150">This rectangle is relative to the parent window of the display window (usually the desktop).</span></span> <span data-ttu-id="949ce-151">Wenn das Fenster nicht angegeben wird, wird standardmäßig die anfängliche Fenstergröße und-Position verwendet.</span><span class="sxs-lookup"><span data-stu-id="949ce-151">If the window is not specified, it defaults to the initial window size and position.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect</span><span class="sxs-lookup"><span data-stu-id="949ce-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="949ce-153">Der **RC** -Member der durch *lpdest* identifizierten Struktur enthält ein gültiges Rechteck.</span><span class="sxs-lookup"><span data-stu-id="949ce-153">The **rc** member of the structure identified by *lpDest* contains a valid rectangle.</span></span>

</dd> </dl>

<span data-ttu-id="949ce-154">Für Digital Video-Geräte verweist *lpdest* auf eine [**MCI \_ DGV \_ Put \_**](/previous-versions//dd743397(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="949ce-154">For digital-video devices, *lpDest* points to an [**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85)) structure.</span></span>

<span data-ttu-id="949ce-155">Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="949ce-155">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="949ce-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI \_ OVLY \_ - \_ Ziel</span><span class="sxs-lookup"><span data-stu-id="949ce-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI\_OVLY\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="949ce-157">Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich des Client Fensters an, in dem ein Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="949ce-157">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the client window used to display an image.</span></span> <span data-ttu-id="949ce-158">Das Rechteck enthält den Offset und den sichtbaren Block des Bilds relativ zum Fenster Ursprung.</span><span class="sxs-lookup"><span data-stu-id="949ce-158">The rectangle contains the offset and visible extent of the image relative to the window origin.</span></span> <span data-ttu-id="949ce-159">Wenn der Frame gestreckt wird, wird die Quelle auf das Ziel Rechteck gestreckt.</span><span class="sxs-lookup"><span data-stu-id="949ce-159">If the frame is being stretched, the source is stretched to the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI \_ OVLY \_ - \_ Frame</span><span class="sxs-lookup"><span data-stu-id="949ce-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI\_OVLY\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="949ce-161">Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich des Video Puffers an, der zum Empfangen des Video Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="949ce-161">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used to receive the video image.</span></span> <span data-ttu-id="949ce-162">Das Rechteck enthält den Offset und den Umfang des Puffer Bereichs relativ zum Video Puffer Ursprung.</span><span class="sxs-lookup"><span data-stu-id="949ce-162">The rectangle contains the offset and extent of the buffer area relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI \_ OVLY \_ - \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="949ce-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI\_OVLY\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="949ce-164">Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich des Video Puffers an, der als Quelle des digitalen Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="949ce-164">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used as the source of the digital image.</span></span> <span data-ttu-id="949ce-165">Das Rechteck enthält den Offset und den Umfang des clippingrechtecks für den Video Puffer relativ zum Ursprung.</span><span class="sxs-lookup"><span data-stu-id="949ce-165">The rectangle contains the offset and extent of the clipping rectangle for the video buffer relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI \_ OVLY \_ - \_ Video</span><span class="sxs-lookup"><span data-stu-id="949ce-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI\_OVLY\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="949ce-167">Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich der Videoquellen Erfassung durch den Video Puffer an.</span><span class="sxs-lookup"><span data-stu-id="949ce-167">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video source capture by the video buffer.</span></span> <span data-ttu-id="949ce-168">Das Rechteck enthält den Offset und den Umfang des clippingrechtecks für die Videoquelle relativ zum Ursprung.</span><span class="sxs-lookup"><span data-stu-id="949ce-168">The rectangle contains the offset and extent of the clipping rectangle for the video source relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="949ce-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect</span><span class="sxs-lookup"><span data-stu-id="949ce-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="949ce-170">Der **RC** -Member der durch *lpdest* identifizierten Struktur enthält ein gültiges Anzeige Rechteck.</span><span class="sxs-lookup"><span data-stu-id="949ce-170">The **rc** member of the structure identified by *lpDest* contains a valid display rectangle.</span></span> <span data-ttu-id="949ce-171">Wenn dieses Flag nicht angegeben wird, entspricht das Standard Rechteck den Koordinaten des Video Puffers oder Fensters, das abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="949ce-171">If this flag is not specified, the default rectangle matches the coordinates of the video buffer or window being clipped.</span></span>

</dd> </dl>

<span data-ttu-id="949ce-172">Bei Video Überlagerungs Geräten verweist *lpdest* auf eine [**MCI \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="949ce-172">For video-overlay devices, *lpDest* points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="949ce-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="949ce-173">Requirements</span></span>



| <span data-ttu-id="949ce-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="949ce-174">Requirement</span></span> | <span data-ttu-id="949ce-175">Wert</span><span class="sxs-lookup"><span data-stu-id="949ce-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="949ce-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="949ce-176">Minimum supported client</span></span><br/> | <span data-ttu-id="949ce-177">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="949ce-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="949ce-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="949ce-178">Minimum supported server</span></span><br/> | <span data-ttu-id="949ce-179">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="949ce-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="949ce-180">Header</span><span class="sxs-lookup"><span data-stu-id="949ce-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="949ce-181"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="949ce-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="949ce-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="949ce-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="949ce-183">MCI</span><span class="sxs-lookup"><span data-stu-id="949ce-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="949ce-184">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="949ce-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

