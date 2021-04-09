---
title: MCI_WHERE Befehl (MMSYSTEM. h)
description: Der Befehl "MCI where" ruft \_ das Clippingrechteck für das Videogerät ab.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- MCI_WHERE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956526"
---
# <a name="mci_where-command"></a><span data-ttu-id="15dfa-104">Befehl "MCI \_ where"</span><span class="sxs-lookup"><span data-stu-id="15dfa-104">MCI\_WHERE command</span></span>

<span data-ttu-id="15dfa-105">Der Befehl "MCI where" ruft \_ das Clippingrechteck für das Videogerät ab.</span><span class="sxs-lookup"><span data-stu-id="15dfa-105">The MCI\_WHERE command obtains the clipping rectangle for the video device.</span></span> <span data-ttu-id="15dfa-106">Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="15dfa-106">Digital-video, and video-overlay devices recognize this command.</span></span> <span data-ttu-id="15dfa-107">Die **oberen** und **linken** Elemente der zurückgegebenen [Rect](/previous-versions//ms536136(v=vs.85)) enthalten den Ursprung des clippingrechtecks, und die **Rechte** und **unteren** Elemente enthalten die Breite und Höhe des clippingrechtecks.</span><span class="sxs-lookup"><span data-stu-id="15dfa-107">The **top** and **left** members of the returned [RECT](/previous-versions//ms536136(v=vs.85)) contain the origin of the clipping rectangle, and the **right** and **bottom** members contain the width and height of the clipping rectangle.</span></span> <span data-ttu-id="15dfa-108">(Dies ist nicht die Standardverwendung des **rechten** und **unteren** Members.)</span><span class="sxs-lookup"><span data-stu-id="15dfa-108">(This is not the standard use of the **right** and **bottom** members.)</span></span>

<span data-ttu-id="15dfa-109">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="15dfa-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
);
```



## <a name="parameters"></a><span data-ttu-id="15dfa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="15dfa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15dfa-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="15dfa-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-112">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="15dfa-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="15dfa-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-114">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="15dfa-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="15dfa-115">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="15dfa-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpquery*</span><span class="sxs-lookup"><span data-stu-id="15dfa-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-117">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="15dfa-117">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="15dfa-118">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="15dfa-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15dfa-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15dfa-119">Return Value</span></span>

<span data-ttu-id="15dfa-120">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="15dfa-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="15dfa-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15dfa-121">Remarks</span></span>

<span data-ttu-id="15dfa-122">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="15dfa-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="15dfa-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ DGV \_ ( \_ Ziel)</span><span class="sxs-lookup"><span data-stu-id="15dfa-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI\_DGV\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-124">Ruft eine Beschreibung des rechteckigen Bereichs ab, der zum Anzeigen von Videos und Bildern im Client Bereich des aktuellen Fensters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="15dfa-124">Obtains a description of the rectangular region used to display video and images in the client area of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ DGV, \_ wobei \_ Frame</span><span class="sxs-lookup"><span data-stu-id="15dfa-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI\_DGV\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-126">Ruft eine Beschreibung des rechteckigen Bereichs des Frame Puffers ab, in den Bilder aus dem Video Rechteck skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="15dfa-126">Obtains a description of the rectangular region of the frame buffer into which images from the video rectangle are scaled.</span></span> <span data-ttu-id="15dfa-127">Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.</span><span class="sxs-lookup"><span data-stu-id="15dfa-127">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ ( \_ Max.)</span><span class="sxs-lookup"><span data-stu-id="15dfa-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI\_DGV\_WHERE\_MAX</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-129">Bei Verwendung mit MCI \_ DGV \_ Where \_ Destination oder MCI \_ DGV \_ Where \_ Source gibt das zurückgegebene Rechteck die maximale Breite und Höhe des angegebenen Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="15dfa-129">When used with MCI\_DGV\_WHERE\_DESTINATION or MCI\_DGV\_WHERE\_SOURCE, the rectangle returned indicates the maximum width and height of the specified region.</span></span> <span data-ttu-id="15dfa-130">Bei Verwendung mit MCI \_ DGV \_ Where \_ Window gibt das zurückgegebene Rechteck die Größe der gesamten Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="15dfa-130">When used with MCI\_DGV\_WHERE\_WINDOW, the rectangle returned indicates the size of the entire display.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV, \_ wobei \_ Quelle</span><span class="sxs-lookup"><span data-stu-id="15dfa-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI\_DGV\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-132">Ruft eine Beschreibung des rechteckigen Bereichs ab (aus dem Frame Puffer abgeleitet), der gestreckt wird, um das Ziel Rechteck auf der Anzeige zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="15dfa-132">Obtains a description of the rectangular region (cropped from the frame buffer) that is stretched to fit the destination rectangle on the display.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI- \_ DGV- \_ \_ Video</span><span class="sxs-lookup"><span data-stu-id="15dfa-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI\_DGV\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-134">Ruft eine Beschreibung des rechteckigen Bereichs ab, der von der Präsentations Quelle zum Ausfüllen des Frame Rechtecks im Frame Puffer abgeschnitten wurde.</span><span class="sxs-lookup"><span data-stu-id="15dfa-134">Obtains a description of the rectangular region cropped from the presentation source to fill the frame rectangle in the frame buffer.</span></span> <span data-ttu-id="15dfa-135">Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.</span><span class="sxs-lookup"><span data-stu-id="15dfa-135">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI \_ DGV \_ Where- \_ Fenster</span><span class="sxs-lookup"><span data-stu-id="15dfa-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI\_DGV\_WHERE\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-137">Ruft eine Beschreibung des Anzeige Fensterrahmens ab.</span><span class="sxs-lookup"><span data-stu-id="15dfa-137">Obtains a description of the display-window frame.</span></span>

</dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="15dfa-138">Für Digital Video-Geräte zeigt der *lpquery* -Parameter auf eine **MCI- \_ DGV \_ \_** -Struktur, in der die Parameter Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="15dfa-138">For digital-video devices, the *lpQuery* parameter points to an **MCI\_DGV\_WHERE\_PARMS** structure.</span></span> <span data-ttu-id="15dfa-139">Die MCI-DGV-Struktur, bei der die Struktur von **\_ \_ \_ Parametern** mit der Struktur des [**MCI- \_ DGV- \_ \_ para**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) Metern identisch ist.</span><span class="sxs-lookup"><span data-stu-id="15dfa-139">The **MCI\_DGV\_WHERE\_PARMS** structure is identical to the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="15dfa-140">Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="15dfa-140">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="15dfa-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ OVLY \_ Where- \_ Ziel</span><span class="sxs-lookup"><span data-stu-id="15dfa-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI\_OVLY\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-142">Ruft das Zielanzeige Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="15dfa-142">Obtains the destination display rectangle.</span></span> <span data-ttu-id="15dfa-143">Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.</span><span class="sxs-lookup"><span data-stu-id="15dfa-143">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ OVLY, \_ wobei \_ Frame</span><span class="sxs-lookup"><span data-stu-id="15dfa-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI\_OVLY\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-145">Ruft das Überlagerungs Rahmen Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="15dfa-145">Obtains the overlay frame rectangle.</span></span> <span data-ttu-id="15dfa-146">Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.</span><span class="sxs-lookup"><span data-stu-id="15dfa-146">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ Where \_ Source</span><span class="sxs-lookup"><span data-stu-id="15dfa-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI\_OVLY\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-148">Ruft das Quell Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="15dfa-148">Obtains the source rectangle.</span></span> <span data-ttu-id="15dfa-149">Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.</span><span class="sxs-lookup"><span data-stu-id="15dfa-149">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="15dfa-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ OVLY \_ Where- \_ Video</span><span class="sxs-lookup"><span data-stu-id="15dfa-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI\_OVLY\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="15dfa-151">Ruft das Video Rechteck ab.</span><span class="sxs-lookup"><span data-stu-id="15dfa-151">Obtains the video rectangle.</span></span> <span data-ttu-id="15dfa-152">Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.</span><span class="sxs-lookup"><span data-stu-id="15dfa-152">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> </dl>

<span data-ttu-id="15dfa-153">Bei Video Überlagerungs Geräten zeigt der *lpquery* -Parameter auf eine [**MCI \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="15dfa-153">For video-overlay devices, the *lpQuery* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="15dfa-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15dfa-154">Requirements</span></span>



| <span data-ttu-id="15dfa-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15dfa-155">Requirement</span></span> | <span data-ttu-id="15dfa-156">Wert</span><span class="sxs-lookup"><span data-stu-id="15dfa-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15dfa-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15dfa-157">Minimum supported client</span></span><br/> | <span data-ttu-id="15dfa-158">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15dfa-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15dfa-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15dfa-159">Minimum supported server</span></span><br/> | <span data-ttu-id="15dfa-160">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15dfa-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15dfa-161">Header</span><span class="sxs-lookup"><span data-stu-id="15dfa-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="15dfa-162"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15dfa-162"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15dfa-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15dfa-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15dfa-164">MCI</span><span class="sxs-lookup"><span data-stu-id="15dfa-164">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="15dfa-165">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="15dfa-165">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

