---
title: MCI_OPEN Befehl (MMSYSTEM. h)
description: Der Befehl MCI \_ Open Initialisiert ein Gerät oder eine Datei. Alle Geräte erkennen diesen Befehl.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858630"
---
# <a name="mci_open-command"></a><span data-ttu-id="3ce50-105">MCI- \_ Befehl "Öffnen"</span><span class="sxs-lookup"><span data-stu-id="3ce50-105">MCI\_OPEN command</span></span>

<span data-ttu-id="3ce50-106">Der Befehl MCI \_ Open Initialisiert ein Gerät oder eine Datei.</span><span class="sxs-lookup"><span data-stu-id="3ce50-106">The MCI\_OPEN command initializes a device or file.</span></span> <span data-ttu-id="3ce50-107">Alle Geräte erkennen diesen Befehl.</span><span class="sxs-lookup"><span data-stu-id="3ce50-107">All devices recognize this command.</span></span>

<span data-ttu-id="3ce50-108">Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="3ce50-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
);
```



## <a name="parameters"></a><span data-ttu-id="3ce50-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ce50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ce50-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*</span><span class="sxs-lookup"><span data-stu-id="3ce50-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-111">Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="3ce50-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3ce50-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-113">MCI- \_ Benachrichtigung oder MCI- \_ Wartezeit.</span><span class="sxs-lookup"><span data-stu-id="3ce50-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="3ce50-114">Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3ce50-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpopen*</span><span class="sxs-lookup"><span data-stu-id="3ce50-115"><span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-116">Zeiger auf eine [**MCI- \_ Open- \_ Parser**](mci-open-parms.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3ce50-116">Pointer to an [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span> <span data-ttu-id="3ce50-117">(Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)</span><span class="sxs-lookup"><span data-stu-id="3ce50-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ce50-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ce50-118">Return Value</span></span>

<span data-ttu-id="3ce50-119">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="3ce50-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce50-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ce50-120">Remarks</span></span>

<span data-ttu-id="3ce50-121">Das MCI \_ - \_ Flag für Open Type muss immer verwendet werden, wenn ein Gerät in der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ce50-121">The MCI\_OPEN\_TYPE flag must be used whenever a device is specified in the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="3ce50-122">Wenn Sie ein Gerät öffnen, indem Sie eine gerätertyp Konstante angeben, müssen Sie \_ \_ \_ zusätzlich zum geöffneten MCI-Typ das MCI-Flag für das Open Type-ID-Flag angeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3ce50-122">If you open a device by specifying a device-type constant, you must specify the MCI\_OPEN\_TYPE\_ID flag in addition to MCI\_OPEN\_TYPE.</span></span> <span data-ttu-id="3ce50-123">Eine Liste der Gerätetyp Konstanten finden Sie unter [MCI-Gerätetypen](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="3ce50-123">For a list of device-type constants, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="3ce50-124">Wenn das MCI \_ - \_ Flag zum Öffnen von freistellbar beim ersten Öffnen eines Geräts oder einer Datei nicht angegeben wird, schlagen alle nachfolgenden MCI- \_ Befehle zum Öffnen des Geräts oder der Datei fehl.</span><span class="sxs-lookup"><span data-stu-id="3ce50-124">If the MCI\_OPEN\_SHAREABLE flag is not specified when a device or file is initially opened, all subsequent MCI\_OPEN commands to the device or file will fail.</span></span> <span data-ttu-id="3ce50-125">Wenn das Gerät oder die Datei bereits geöffnet ist und dieses Flag nicht angegeben ist, schlägt der Aufruf fehl, auch wenn der erste geöffnete Befehl, den MCI angegeben hat, \_ \_ share able geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="3ce50-125">If the device or file is already open and this flag is not specified, the call will fail even if the first open command specified MCI\_OPEN\_SHAREABLE.</span></span> <span data-ttu-id="3ce50-126">Dateien, die für mciseq geöffnet wurden. DRV und MCIWave. DRV-Geräte sind nicht Sharable.</span><span class="sxs-lookup"><span data-stu-id="3ce50-126">Files opened for the MCISEQ.DRV and MCIWAVE.DRV devices are nonsharable.</span></span>

<span data-ttu-id="3ce50-127">Der Fall wird im Gerätenamen ignoriert, es dürfen jedoch keine führenden oder nachfolgenden Leerzeichen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3ce50-127">Case is ignored in the device name, but there cannot be leading or trailing blanks.</span></span>

<span data-ttu-id="3ce50-128">Wenn Sie die automatische Typauswahl (über die Einträge in der Registrierung) verwenden möchten, weisen Sie dem **lpstrelementname** -Member der von *lpopen* identifizierten Struktur den Dateinamen und die Dateierweiterung zu, legen Sie den **lpstrdevicetype** -Member auf **null** fest, und legen Sie das Flag für das MCI- \_ Open-Element fest \_ .</span><span class="sxs-lookup"><span data-stu-id="3ce50-128">To use automatic type selection (via the entries in the registry), assign the filename and file extension to the **lpstrElementName** member of the structure identified by *lpOpen*, set the **lpstrDeviceType** member to **NULL**, and set the MCI\_OPEN\_ELEMENT flag.</span></span>

<span data-ttu-id="3ce50-129">Die folgenden zusätzlichen Flags gelten für alle Geräte, die MCI geöffnet unterstützen \_ :</span><span class="sxs-lookup"><span data-stu-id="3ce50-129">The following additional flags apply to all devices supporting MCI\_OPEN:</span></span>

<dl> <dt>

<span data-ttu-id="3ce50-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI- \_ Open- \_ Alias</span><span class="sxs-lookup"><span data-stu-id="3ce50-130"><span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI\_OPEN\_ALIAS</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-131">Ein Alias ist im **lpstralias** -Member der durch *lpopen* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="3ce50-131">An alias is included in the **lpstrAlias** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ Open \_ share able</span><span class="sxs-lookup"><span data-stu-id="3ce50-132"><span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI\_OPEN\_SHAREABLE</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-133">Das Gerät oder die Datei muss als Sharable geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3ce50-133">The device or file should be opened as sharable.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI- \_ Open- \_ Typ</span><span class="sxs-lookup"><span data-stu-id="3ce50-134"><span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI\_OPEN\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-135">Ein Gerätetyp Name oder eine Konstante ist im **lpstrdevicetype** -Member der durch *lpopen* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="3ce50-135">A device type name or constant is included in the **lpstrDeviceType** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI- \_ öffnende \_ Typ- \_ ID</span><span class="sxs-lookup"><span data-stu-id="3ce50-136"><span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>MCI\_OPEN\_TYPE\_ID</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-137">Das nieder wertige Wort des **lpstrdevicetype** -Members der von *lpopen* identifizierten Struktur enthält einen Standard-MCI-Gerätetyp Bezeichner, und das höchst wertige Wort enthält optional den Ordinalindex für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="3ce50-137">The low-order word of the **lpstrDeviceType** member of the structure identified by *lpOpen* contains a standard MCI device type identifier and the high-order word optionally contains the ordinal index for the device.</span></span> <span data-ttu-id="3ce50-138">Verwenden Sie dieses Flag mit dem MCI- \_ \_ Flag Open Type.</span><span class="sxs-lookup"><span data-stu-id="3ce50-138">Use this flag with the MCI\_OPEN\_TYPE flag.</span></span>

</dd> </dl>

<span data-ttu-id="3ce50-139">Die folgenden zusätzlichen Flags gelten für Verbund Geräte:</span><span class="sxs-lookup"><span data-stu-id="3ce50-139">The following additional flags apply to compound devices:</span></span>

<dl> <dt>

<span data-ttu-id="3ce50-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>geöffnetes MCI- \_ \_ Element</span><span class="sxs-lookup"><span data-stu-id="3ce50-140"><span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI\_OPEN\_ELEMENT</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-141">Ein Dateiname ist im **lpstrelementname** -Member der durch *lpopen* identifizierten Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="3ce50-141">A filename is included in the **lpstrElementName** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI- \_ Open- \_ Element- \_ ID</span><span class="sxs-lookup"><span data-stu-id="3ce50-142"><span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>MCI\_OPEN\_ELEMENT\_ID</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-143">Der **lpstrelementname** -Member der Struktur, die von *lpopen* identifiziert wird, wird als **DWORD** -Wert interpretiert und hat eine interne Bedeutung für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="3ce50-143">The **lpstrElementName** member of the structure identified by *lpOpen* is interpreted as a **DWORD** value and has meaning internal to the device.</span></span> <span data-ttu-id="3ce50-144">Verwenden Sie dieses Flag mit dem MCI- \_ Flag "Open \_ Element".</span><span class="sxs-lookup"><span data-stu-id="3ce50-144">Use this flag with the MCI\_OPEN\_ELEMENT flag.</span></span>

</dd> </dl>

<span data-ttu-id="3ce50-145">Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="3ce50-145">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="3ce50-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ Open \_ nostatic</span><span class="sxs-lookup"><span data-stu-id="3ce50-146"><span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI\_DGV\_OPEN\_NOSTATIC</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-147">Das Gerät sollte die Anzahl der statischen (System) Farben in der Palette reduzieren.</span><span class="sxs-lookup"><span data-stu-id="3ce50-147">The device should reduce the number of static (system) colors in the palette.</span></span> <span data-ttu-id="3ce50-148">Dadurch erhöht sich die Anzahl der zum Rendern des Videodaten Stroms verfügbaren Farben.</span><span class="sxs-lookup"><span data-stu-id="3ce50-148">This increases the number of colors available for rendering the video stream.</span></span> <span data-ttu-id="3ce50-149">Dieses Flag gilt nur für Geräte, die eine Palette mit Windows gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ce50-149">This flag applies only to devices that share a palette with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>übergeordnetes MCI- \_ DGV-Element \_ Öffnen \_</span><span class="sxs-lookup"><span data-stu-id="3ce50-150"><span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI\_DGV\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-151">Das übergeordnete Fenster Handle wird im **hwndParent** -Member der durch *lpopen* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="3ce50-151">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ Open \_ WS</span><span class="sxs-lookup"><span data-stu-id="3ce50-152"><span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI\_DGV\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-153">Im **dwstyle** -Member der-Struktur, die von *lpopen* identifiziert wird, wird ein Fenster Stil angegeben.</span><span class="sxs-lookup"><span data-stu-id="3ce50-153">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV, \_ geöffnet, \_ 16 Bit</span><span class="sxs-lookup"><span data-stu-id="3ce50-154"><span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI\_DGV\_OPEN\_16BIT</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-155">Gibt eine Einstellung für die Unterstützung von 16-Bit-MCI-Geräten an.</span><span class="sxs-lookup"><span data-stu-id="3ce50-155">Indicates a preference for 16-bit MCI device support.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV, \_ geöffnet, \_ 32-Bit</span><span class="sxs-lookup"><span data-stu-id="3ce50-156"><span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI\_DGV\_OPEN\_32BIT</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-157">Gibt eine Einstellung für die 32-Bit-MCI-Geräte Unterstützung an.</span><span class="sxs-lookup"><span data-stu-id="3ce50-157">Indicates a preference for 32-bit MCI device support.</span></span>

</dd> </dl>

<span data-ttu-id="3ce50-158">Für Digital Video-Geräte verweist der *lpopen* -Parameter auf eine [**MCI-DGV-Struktur mit \_ \_ geöffneten \_ para**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) Metern.</span><span class="sxs-lookup"><span data-stu-id="3ce50-158">For digital-video devices, the *lpOpen* parameter points to an [**MCI\_DGV\_OPEN\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) structure.</span></span>

<span data-ttu-id="3ce50-159">Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:</span><span class="sxs-lookup"><span data-stu-id="3ce50-159">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="3ce50-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ über \_ geordnetes Element öffnen</span><span class="sxs-lookup"><span data-stu-id="3ce50-160"><span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI\_OVLY\_OPEN\_PARENT</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-161">Das übergeordnete Fenster Handle wird im **hwndParent** -Member der durch *lpopen* identifizierten Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="3ce50-161">The parent window handle is specified in the **hWndParent** member of the structure identified by *lpOpen*.</span></span>

</dd> <dt>

<span data-ttu-id="3ce50-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY- \_ Open- \_ WS</span><span class="sxs-lookup"><span data-stu-id="3ce50-162"><span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI\_OVLY\_OPEN\_WS</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-163">Im **dwstyle** -Member der-Struktur, die von *lpopen* identifiziert wird, wird ein Fenster Stil angegeben.</span><span class="sxs-lookup"><span data-stu-id="3ce50-163">A window style is specified in the **dwStyle** member of the structure identified by *lpOpen*.</span></span> <span data-ttu-id="3ce50-164">Der **dwstyle** -Wert gibt den Stil des Fensters an, den der Treiber erstellt und anzeigt, wenn die Anwendung keinen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3ce50-164">The **dwStyle** value specifies the style of the window that the driver will create and display if the application does not provide one.</span></span> <span data-ttu-id="3ce50-165">Der style-Parameter nimmt eine ganze Zahl an, die den Fenster Stil definiert.</span><span class="sxs-lookup"><span data-stu-id="3ce50-165">The style parameter takes an integer that defines the window style.</span></span> <span data-ttu-id="3ce50-166">Diese Konstanten sind identisch mit den Standardfenster Stilen (z. b. WS \_ Child, WS \_ overlappedwindow oder WS \_ Popup).</span><span class="sxs-lookup"><span data-stu-id="3ce50-166">These constants are the same as the standard window styles (such as WS\_CHILD, WS\_OVERLAPPEDWINDOW, or WS\_POPUP).</span></span>

</dd> </dl>

<span data-ttu-id="3ce50-167">Bei Video Überlagerungs Geräten zeigt der *lpopen* -Parameter auf eine [**MCI \_ OVLY- \_ Open \_**](mci-ovly-open-parms.md) -Parameterstruktur.</span><span class="sxs-lookup"><span data-stu-id="3ce50-167">For video-overlay devices, the *lpOpen* parameter points to an [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md) structure.</span></span>

<span data-ttu-id="3ce50-168">Das folgende zusätzliche Flag wird mit dem **waveaudiogerätetyp** verwendet:</span><span class="sxs-lookup"><span data-stu-id="3ce50-168">The following additional flag is used with the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="3ce50-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI- \_ Wellen \_ Öffnungs \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="3ce50-169"><span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>MCI\_WAVE\_OPEN\_BUFFER</span></span>
</dt> <dd>

<span data-ttu-id="3ce50-170">Im **dwbufferseconds** -Member der Struktur, die von *lpopen* identifiziert wird, wird eine Pufferlänge angegeben.</span><span class="sxs-lookup"><span data-stu-id="3ce50-170">A buffer length is specified in the **dwBufferSeconds** member of the structure identified by *lpOpen*.</span></span>

</dd> </dl>

<span data-ttu-id="3ce50-171">Bei Waveform-Audiogeräten zeigt der *lpopen* -Parameter auf eine [**MCI \_ Wave \_ Open \_**](mci-wave-open-parms.md) -Parameter Struktur.</span><span class="sxs-lookup"><span data-stu-id="3ce50-171">For waveform-audio devices, the *lpOpen* parameter points to an [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) structure.</span></span> <span data-ttu-id="3ce50-172">Der MCIWave-Treiber erfordert ein asynchrones Waveform-Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="3ce50-172">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce50-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ce50-173">Requirements</span></span>



| <span data-ttu-id="3ce50-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ce50-174">Requirement</span></span> | <span data-ttu-id="3ce50-175">Wert</span><span class="sxs-lookup"><span data-stu-id="3ce50-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce50-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ce50-176">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce50-177">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ce50-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3ce50-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ce50-178">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce50-179">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ce50-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3ce50-180">Header</span><span class="sxs-lookup"><span data-stu-id="3ce50-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce50-181"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ce50-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ce50-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ce50-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce50-183">MCI</span><span class="sxs-lookup"><span data-stu-id="3ce50-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3ce50-184">MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="3ce50-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

