---
title: MCI_LIST Befehl (MMSYSTEM. h)
description: Der MCI \_ -Listen Befehl ruft Informationen über die Anzahl und die Typen der Eingaben ab, die für das Gerät verfügbar sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519037"
---
# <a name="mci_list-command"></a><span data-ttu-id="6b156-105">MCI- \_ Listen Befehl</span><span class="sxs-lookup"><span data-stu-id="6b156-105">MCI\_LIST command</span></span>

<span data-ttu-id="6b156-106">Der MCI \_ -Listen Befehl ruft Informationen über die Anzahl und die Typen der Eingaben ab, die für das Gerät verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6b156-106">The MCI\_LIST command obtains information about the number and types of inputs available to the device.</span></span> <span data-ttu-id="6b156-107">Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.</span><span class="sxs-lookup"><span data-stu-id="6b156-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="6b156-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="6b156-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a><span data-ttu-id="6b156-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b156-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b156-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="6b156-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6b156-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="6b156-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6b156-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6b156-113">MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test.</span><span class="sxs-lookup"><span data-stu-id="6b156-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="6b156-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6b156-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b156-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lplist*</span><span class="sxs-lookup"><span data-stu-id="6b156-115"><span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*</span></span>
</dt> <dd>

<span data-ttu-id="6b156-116">Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="6b156-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="6b156-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="6b156-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b156-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b156-118">Return Value</span></span>

<span data-ttu-id="6b156-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="6b156-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b156-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b156-120">Remarks</span></span>

<span data-ttu-id="6b156-121">Die folgenden zusätzlichen Flags gelten für den **Digitalvideo** -Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="6b156-121">The following additional flags apply to the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6b156-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ List \_ alg</span><span class="sxs-lookup"><span data-stu-id="6b156-122"><span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI\_DGV\_LIST\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="6b156-123">Der **lpstrinalgorithmus** -Member der durch *lplist* identifizierten Struktur enthält eine Adresse eines Puffers, der den Namen eines Algorithmus enthält.</span><span class="sxs-lookup"><span data-stu-id="6b156-123">The **lpstrAlgorithm** member of the structure identified by *lpList* contains an address of a buffer containing the name of an algorithm.</span></span> <span data-ttu-id="6b156-124">Der Name wird verwendet, um die einem Algorithmus zugeordneten Typen von Qualitäts Deskriptoren abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-124">The name is used to retrieve the types of quality descriptors associated with an algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI- \_ DGV- \_ Listen \_ Anzahl</span><span class="sxs-lookup"><span data-stu-id="6b156-125"><span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI\_DGV\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="6b156-126">Gibt die Anzahl der Optionen des angegebenen Typs zurück.</span><span class="sxs-lookup"><span data-stu-id="6b156-126">Returns the number of options of the specified type.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI- \_ DGV- \_ Listen \_ Element</span><span class="sxs-lookup"><span data-stu-id="6b156-127"><span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI\_DGV\_LIST\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="6b156-128">Eine-Konstante, die angibt, dass der Listentyp im **dwitem** -Member der durch *lplist* identifizierten-Struktur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6b156-128">A constant indicating the list type is included in the **dwItem** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="6b156-129">Dieses Flag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6b156-129">This flag is required.</span></span> <span data-ttu-id="6b156-130">Verwenden Sie eine der folgenden Konstanten, um den Auflistungstyp anzugeben:</span><span class="sxs-lookup"><span data-stu-id="6b156-130">Use one of the following constants to indicate the list type:</span></span>

</dd> <dt>

<span data-ttu-id="6b156-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ \_ -Liste Audio- \_ alg</span><span class="sxs-lookup"><span data-stu-id="6b156-131"><span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI\_DGV\_LIST\_AUDIO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="6b156-132">Der Befehl sollte Namen von audioalgorithmen abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-132">The command should retrieve names of audio algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ \_ -Liste \_ Audioqualität</span><span class="sxs-lookup"><span data-stu-id="6b156-133"><span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI\_DGV\_LIST\_AUDIO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="6b156-134">Der Befehl sollte audioqualitätsgrade abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-134">The command should retrieve audio quality levels.</span></span> <span data-ttu-id="6b156-135">Die zurückgegebenen Ebenen werden dem Algorithmus zugeordnet, auf den der **lpstrinalgorithmus** -Member der durch *lplist* bezeichneten Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="6b156-135">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="6b156-136">Wenn dieser Member mithilfe der Zeichenfolge "Current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b156-136">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI \_ \_ -DGV \_ -Listen-Audiodatenstrom \_</span><span class="sxs-lookup"><span data-stu-id="6b156-137"><span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI\_DGV\_LIST\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="6b156-138">Der Befehl sollte Namen von Audiodatenströmen abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-138">The command should retrieve names of audio streams.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI- \_ DGV- \_ Liste \_ immer noch \_ Al</span><span class="sxs-lookup"><span data-stu-id="6b156-139"><span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI\_DGV\_LIST\_STILL\_AL</span></span>
</dt> <dd>

<span data-ttu-id="6b156-140">Der Befehl sollte Namen von immer noch Algorithmen abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-140">The command should retrieve names of still algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI- \_ DGV- \_ Liste \_ immer noch \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="6b156-141"><span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI\_DGV\_LIST\_STILL\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="6b156-142">Der Befehl sollte Qualitätsstufen abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-142">The command should retrieve quality levels.</span></span> <span data-ttu-id="6b156-143">Die zurückgegebenen Ebenen werden dem Algorithmus zugeordnet, auf den der **lpstrinalgorithmus** -Member der durch *lplist* bezeichneten Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="6b156-143">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="6b156-144">Wenn dieser Member mithilfe der Zeichenfolge "Current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b156-144">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI- \_ DGV- \_ Liste \_ Video- \_ alg</span><span class="sxs-lookup"><span data-stu-id="6b156-145"><span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI\_DGV\_LIST\_VIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="6b156-146">Der Befehl sollte Namen von Video Algorithmen abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-146">The command should retrieve names of video algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI- \_ DGV- \_ Listen \_ Video \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="6b156-147"><span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI\_DGV\_LIST\_VIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="6b156-148">Der Befehl sollte Video Qualitäts Ebenen abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-148">The command should retrieve video quality levels.</span></span> <span data-ttu-id="6b156-149">Die zurückgegebenen Ebenen werden dem Algorithmus zugeordnet, auf den der **lpstrinalgorithmus** -Member der durch *lplist* bezeichneten Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="6b156-149">The levels returned are associated with the algorithm referenced by the **lpstrAlgorithm** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="6b156-150">Wenn dieser Member mithilfe der Zeichenfolge "Current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b156-150">If that member is specified using the string "current", then the qualities associated with the current algorithm are returned.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI- \_ DGV- \_ Liste ( \_ Video \_ Quelle)</span><span class="sxs-lookup"><span data-stu-id="6b156-151"><span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI\_DGV\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="6b156-152">Der Befehl sollte Informationen zu den Videoquellen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6b156-152">The command should return information about the video sources.</span></span> <span data-ttu-id="6b156-153">Bei Verwendung mit der MCI- \_ DGV- \_ Listen Anzahl \_ gibt der Befehl die Anzahl der Videoquellen zurück.</span><span class="sxs-lookup"><span data-stu-id="6b156-153">When used with MCI\_DGV\_LIST\_COUNT, the command returns the number of video sources.</span></span> <span data-ttu-id="6b156-154">Bei Verwendung mit der MCI- \_ DGV- \_ Listen \_ Nummer gibt der Befehl den Typ einer Videoquelle zurück.</span><span class="sxs-lookup"><span data-stu-id="6b156-154">When used with MCI\_DGV\_LIST\_NUMBER, the command returns the type of a video source.</span></span> <span data-ttu-id="6b156-155">MCI definiert die folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="6b156-155">MCI defines the following types:</span></span>

-   <span data-ttu-id="6b156-156">MCI \_ DGV \_ setvideo \_ src \_ generic</span><span class="sxs-lookup"><span data-stu-id="6b156-156">MCI\_DGV\_SETVIDEO\_SRC\_GENERIC</span></span>
-   <span data-ttu-id="6b156-157">MCI \_ DGV \_ setvideo \_ src \_ NTSC</span><span class="sxs-lookup"><span data-stu-id="6b156-157">MCI\_DGV\_SETVIDEO\_SRC\_NTSC</span></span>
-   <span data-ttu-id="6b156-158">MCI \_ DGV \_ setvideo \_ src \_ PAL</span><span class="sxs-lookup"><span data-stu-id="6b156-158">MCI\_DGV\_SETVIDEO\_SRC\_PAL</span></span>
-   <span data-ttu-id="6b156-159">MCI \_ DGV \_ setvideo \_ src \_ RGB</span><span class="sxs-lookup"><span data-stu-id="6b156-159">MCI\_DGV\_SETVIDEO\_SRC\_RGB</span></span>
-   <span data-ttu-id="6b156-160">MCI \_ DGV \_ setvideo \_ src \_ SECAM</span><span class="sxs-lookup"><span data-stu-id="6b156-160">MCI\_DGV\_SETVIDEO\_SRC\_SECAM</span></span>
-   <span data-ttu-id="6b156-161">MCI \_ DGV \_ setvideo \_ src \_ SVideo</span><span class="sxs-lookup"><span data-stu-id="6b156-161">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO</span></span>

<span data-ttu-id="6b156-162">Möglicherweise gibt es mehrere Quellen für jeden Typ, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6b156-162">There might be more than one source of each type returned.</span></span> <span data-ttu-id="6b156-163">Der generische Quelltyp wird verwendet, wenn mehr als ein Typ von Signal für diesen Connector zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6b156-163">The generic source type is used when more then one type of signal is allowed for that connector.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI- \_ DGV- \_ Listen \_ \_ Videostream</span><span class="sxs-lookup"><span data-stu-id="6b156-164"><span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI\_DGV\_LIST\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="6b156-165">Der Befehl sollte Namen von Videostreams abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b156-165">The command should retrieve names of video streams.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI- \_ DGV- \_ Listen \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="6b156-166"><span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI\_DGV\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="6b156-167">Ein Index wird im **dwnumber** -Member der durch *lplist* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="6b156-167">An index is specified in the **dwNumber** member of the structure identified by *lpList*.</span></span> <span data-ttu-id="6b156-168">Der Index muss eine ganze Zahl zwischen 1 und dem Wert sein, der für das MCI- \_ DGV- \_ Listen Anzahl-Flag zurückgegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="6b156-168">The index must be an integer between 1 and the value returned for the MCI\_DGV\_LIST\_COUNT flag.</span></span>

</dd> </dl>

<span data-ttu-id="6b156-169">Für Digital Video-Geräte verweist die *lplist* auf eine [**MCI- \_ DGV- \_ Listen \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) -Elementstruktur.</span><span class="sxs-lookup"><span data-stu-id="6b156-169">For digital-video devices, *lpList* points to an [**MCI\_DGV\_LIST\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) structure.</span></span>

<span data-ttu-id="6b156-170">Die folgenden zusätzlichen Flags gelten für den **VCR** -Gerätetyp:</span><span class="sxs-lookup"><span data-stu-id="6b156-170">The following additional flags apply to the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="6b156-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>Audioquelle für MCI \_ VCR \_ \_ -Liste \_</span><span class="sxs-lookup"><span data-stu-id="6b156-171"><span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI\_VCR\_LIST\_AUDIO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="6b156-172">Listet Audioeingaben oder-Typen auf.</span><span class="sxs-lookup"><span data-stu-id="6b156-172">List audio inputs or types.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>Anzahl der MCI- \_ VCR- \_ Listen \_</span><span class="sxs-lookup"><span data-stu-id="6b156-173"><span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>MCI\_VCR\_LIST\_COUNT</span></span>
</dt> <dd>

<span data-ttu-id="6b156-174">Legt den **dwreturn** -Member der von *lplist* identifizierten-Struktur auf die Gesamtzahl von Video-oder Audioeingaben fest.</span><span class="sxs-lookup"><span data-stu-id="6b156-174">Sets the **dwReturn** member of the structure identified by *lpList* to the total number of video or audio inputs.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI- \_ VCR- \_ Listen \_ Nummer</span><span class="sxs-lookup"><span data-stu-id="6b156-175"><span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI\_VCR\_LIST\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="6b156-176">Legt den **dwreturn** -Member der durch *lplist* identifizierten Struktur auf den Typ der Video-oder Audioeingabe fest, die vom **dwnumber** -Member angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b156-176">Sets the **dwReturn** member of the structure identified by *lpList* to the type of the video or audio input specified by the **dwNumber** member.</span></span>

</dd> <dt>

<span data-ttu-id="6b156-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>Video Quelle für MCI \_ VCR- \_ Liste \_ \_</span><span class="sxs-lookup"><span data-stu-id="6b156-177"><span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>MCI\_VCR\_LIST\_VIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="6b156-178">Listet Videoeingaben oder-Typen auf.</span><span class="sxs-lookup"><span data-stu-id="6b156-178">List video inputs or types.</span></span>

</dd> </dl>

<span data-ttu-id="6b156-179">Bei VCR-Geräten verweist *lplist* auf eine [**MCI- \_ VCR- \_ Listen \_**](mci-vcr-list-parms.md) -Element-Struktur.</span><span class="sxs-lookup"><span data-stu-id="6b156-179">For VCR devices, *lpList* points to an [**MCI\_VCR\_LIST\_PARMS**](mci-vcr-list-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b156-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b156-180">Requirements</span></span>



| <span data-ttu-id="6b156-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b156-181">Requirement</span></span> | <span data-ttu-id="6b156-182">Wert</span><span class="sxs-lookup"><span data-stu-id="6b156-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b156-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b156-183">Minimum supported client</span></span><br/> | <span data-ttu-id="6b156-184">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b156-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6b156-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b156-185">Minimum supported server</span></span><br/> | <span data-ttu-id="6b156-186">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b156-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6b156-187">Header</span><span class="sxs-lookup"><span data-stu-id="6b156-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b156-188"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b156-188"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b156-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b156-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b156-190">MCI</span><span class="sxs-lookup"><span data-stu-id="6b156-190">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6b156-191">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="6b156-191">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

