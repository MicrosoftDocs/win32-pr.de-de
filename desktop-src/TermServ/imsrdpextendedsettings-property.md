---
title: IMsRdpExtendedSettings Property-Eigenschaft
description: Enthält eine benannte Eigenschaft.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Eigenschaften Eigenschaften Remotedesktopdienste
- Eigenschafts Eigenschaft Remotedesktopdienste, imsrdpextendedsettings-Schnittstelle
- Imsrdpextendedsettings-Schnittstelle Remotedesktopdienste, Property-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745352"
---
# <a name="imsrdpextendedsettingsproperty-property"></a><span data-ttu-id="9b54e-106">Imsrdpextendedsettings::P roperty-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9b54e-106">IMsRdpExtendedSettings::Property property</span></span>

<span data-ttu-id="9b54e-107">Enthält eine benannte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9b54e-107">Contains a named property.</span></span>

<span data-ttu-id="9b54e-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9b54e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b54e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b54e-109">Syntax</span></span>


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a><span data-ttu-id="9b54e-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9b54e-110">Property value</span></span>

<span data-ttu-id="9b54e-111">Der benannte Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="9b54e-111">The named property value.</span></span>

| <span data-ttu-id="9b54e-112">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="9b54e-112">Property name</span></span> | <span data-ttu-id="9b54e-113">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9b54e-113">Data type</span></span> | <span data-ttu-id="9b54e-114">Access</span><span class="sxs-lookup"><span data-stu-id="9b54e-114">Access</span></span> | <span data-ttu-id="9b54e-115">Kann geändert werden, nachdem die Verbindung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9b54e-115">Can be changed after connection started</span></span> | <span data-ttu-id="9b54e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b54e-116">Description</span></span> |
|----------|-----------|--------|-----------------------------------------|-------------|
| <span data-ttu-id="9b54e-117">Connectdechildsession</span><span class="sxs-lookup"><span data-stu-id="9b54e-117">ConnectToChildSession</span></span> | <span data-ttu-id="9b54e-118">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9b54e-118">**VT\_BOOL**</span></span> | <span data-ttu-id="9b54e-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9b54e-119">Read/Write</span></span> | <span data-ttu-id="9b54e-120">Ja</span><span class="sxs-lookup"><span data-stu-id="9b54e-120">Yes</span></span> | <span data-ttu-id="9b54e-121">Das Festlegen dieser Eigenschaft auf **true** bewirkt, dass das Client Steuerelement eine Verbindung mit der untergeordneten Sitzung auf dem lokalen Computer anstelle eines Remote Servers herstellt.</span><span class="sxs-lookup"><span data-stu-id="9b54e-121">Setting this property to **True** causes the client control to connect to the child session on the local machine instead of a remote server.</span></span> <span data-ttu-id="9b54e-122">Wenn diese Eigenschaft auf **true** festgelegt ist, können Sie keine Verbindung mit einem Remote Server herstellen, da alle Verbindungen zu localhost umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9b54e-122">If this property is set to **true**, you cannot connect to a remote server because all connections are redirected to localhost.</span></span> <span data-ttu-id="9b54e-123">Weitere Informationen zu untergeordneten Sitzungen finden Sie unter untergeordnete [Sitzungen](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="9b54e-123">For more information about child sessions, see [Child Sessions](child-sessions.md).</span></span> |
| <span data-ttu-id="9b54e-124">Disablekredentialsdelegation</span><span class="sxs-lookup"><span data-stu-id="9b54e-124">DisableCredentialsDelegation</span></span> | <span data-ttu-id="9b54e-125">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9b54e-125">**VT\_BOOL**</span></span> | <span data-ttu-id="9b54e-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9b54e-126">Read/Write</span></span> | <span data-ttu-id="9b54e-127">Nein</span><span class="sxs-lookup"><span data-stu-id="9b54e-127">No</span></span> | <span data-ttu-id="9b54e-128">**True** gibt an, dass Anmelde Informationen nicht an den Remote Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b54e-128">If **True**, credentials are not sent to the remote server.</span></span> |
| <span data-ttu-id="9b54e-129">Enableframebufferredirect</span><span class="sxs-lookup"><span data-stu-id="9b54e-129">EnableFrameBufferRedirection</span></span> | <span data-ttu-id="9b54e-130">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9b54e-130">**VT\_BOOL**</span></span> | <span data-ttu-id="9b54e-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9b54e-131">Read/Write</span></span> | <span data-ttu-id="9b54e-132">Nein</span><span class="sxs-lookup"><span data-stu-id="9b54e-132">No</span></span> | <span data-ttu-id="9b54e-133">**True** gibt an, dass eine Frame Puffer Umleitung versucht wird.</span><span class="sxs-lookup"><span data-stu-id="9b54e-133">If **True**, frame buffer redirection is attempted.</span></span> <span data-ttu-id="9b54e-134">Bei einer Loopback Verbindung (auf dem Client und auf dem Server) ermöglicht die Frame Puffer Umleitung, dass der Arbeitsspeicher für den Frame Puffer zwischen den Sitzungen gemeinsam verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b54e-134">For a loopback connection (the same computer is both client and server) frame buffer redirection allows the memory for the frame buffer to be shared between the sessions.</span></span> |
| <span data-ttu-id="9b54e-135">Enablehardwaremode</span><span class="sxs-lookup"><span data-stu-id="9b54e-135">EnableHardwareMode</span></span> | <span data-ttu-id="9b54e-136">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9b54e-136">**VT\_BOOL**</span></span>  | <span data-ttu-id="9b54e-137">Nur schreiben</span><span class="sxs-lookup"><span data-stu-id="9b54e-137">Write Only</span></span> | <span data-ttu-id="9b54e-138">Nein</span><span class="sxs-lookup"><span data-stu-id="9b54e-138">No</span></span> | <span data-ttu-id="9b54e-139">**True** gibt an, dass die Hardwareunterstützung mit der Grafik Decodierung versucht wird.</span><span class="sxs-lookup"><span data-stu-id="9b54e-139">If **True**, hardware assist with graphics decoding is attempted.</span></span> |
| <span data-ttu-id="9b54e-140">Ignorecursoren</span><span class="sxs-lookup"><span data-stu-id="9b54e-140">IgnoreCursors</span></span> | <span data-ttu-id="9b54e-141">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9b54e-141">**VT\_BOOL**</span></span> | <span data-ttu-id="9b54e-142">Nur schreiben</span><span class="sxs-lookup"><span data-stu-id="9b54e-142">Write Only</span></span> | <span data-ttu-id="9b54e-143">Nein</span><span class="sxs-lookup"><span data-stu-id="9b54e-143">No</span></span> | <span data-ttu-id="9b54e-144">**True** gibt an, dass vom Remote Server gesendete Cursor ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="9b54e-144">If **True**, cursors sent by the remote server are ignored.</span></span> |
| <span data-ttu-id="9b54e-145">Manualclipboardsyncenabled</span><span class="sxs-lookup"><span data-stu-id="9b54e-145">ManualClipboardSyncEnabled</span></span> | <span data-ttu-id="9b54e-146">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9b54e-146">**VT\_BOOL**</span></span> | <span data-ttu-id="9b54e-147">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9b54e-147">Read/Write</span></span> | <span data-ttu-id="9b54e-148">Ja</span><span class="sxs-lookup"><span data-stu-id="9b54e-148">Yes</span></span> | <span data-ttu-id="9b54e-149">Wenn diese Eigenschaft auf " **true** " festgelegt wird, werden die lokalen und Remote-zwischen Ablagen nicht automatisch synchron gehalten. Stattdessen muss die [**imsrdpclipboard**](imsrdpclipboard.md) -Schnittstelle verwendet werden, um Zwischenablage Formate aus der lokalen Zwischenablage mit der Remote Zwischenablage und der Remote Zwischenablage in die lokale Zwischenablage zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="9b54e-149">Setting this property to **True** means that the local and remote clipboards will not be automatically kept in sync. Instead the [**IMsRdpClipboard**](imsrdpclipboard.md) interface must be used to sync clipboard formats from the local clipboard to the remote clipboard and the remote clipboard to the local clipboard.</span></span> |
| <span data-ttu-id="9b54e-150">ZoomLevel</span><span class="sxs-lookup"><span data-stu-id="9b54e-150">ZoomLevel</span></span> | <span data-ttu-id="9b54e-151">\**_VT \_ UI4_*</span><span class="sxs-lookup"><span data-stu-id="9b54e-151">\**_VT\_UI4_*</span></span> | <span data-ttu-id="9b54e-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9b54e-152">Read/Write</span></span> | <span data-ttu-id="9b54e-153">Ja</span><span class="sxs-lookup"><span data-stu-id="9b54e-153">Yes</span></span> | <span data-ttu-id="9b54e-154">Implementiert das Zoom Feature mithilfe des RDP-ActiveX-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="9b54e-154">Implements the Zoom feature by using the RDP ActiveX control.</span></span> <span data-ttu-id="9b54e-155">Die Zoom Funktion ist im Menü **System** von RDP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b54e-155">The Zoom feature is available from the **System** menu of RDP.</span></span> <span data-ttu-id="9b54e-156">Die **Zoomlevel** -Eigenschaft hat keine Auswirkung auf den RemoteApp-Modus und den Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="9b54e-156">The **ZoomLevel** property has no effect in RemoteApp mode and full-screen mode.</span></span> <span data-ttu-id="9b54e-157">[**Imsrdpclientadvancedsettings:: smartsizing**](imsrdpclientadvancedsettings-smartsizing.md) und **Zoomlevel** schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="9b54e-157">[**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) and **ZoomLevel** are mutually exclusive.</span></span> |

## <a name="requirements"></a><span data-ttu-id="9b54e-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b54e-158">Requirements</span></span>



| <span data-ttu-id="9b54e-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b54e-159">Requirement</span></span> | <span data-ttu-id="9b54e-160">Wert</span><span class="sxs-lookup"><span data-stu-id="9b54e-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b54e-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b54e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9b54e-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9b54e-162">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9b54e-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b54e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9b54e-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b54e-164">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9b54e-165">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9b54e-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b54e-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b54e-166"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="9b54e-167">DLL</span><span class="sxs-lookup"><span data-stu-id="9b54e-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b54e-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b54e-168"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="9b54e-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="9b54e-169">CLSID</span></span><br/>                    | <span data-ttu-id="9b54e-170">CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.</span><span class="sxs-lookup"><span data-stu-id="9b54e-170">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54d38bf7-b1ef-4479-9674-1bd6ea465258</span></span><br/> <span data-ttu-id="9b54e-171">CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.</span><span class="sxs-lookup"><span data-stu-id="9b54e-171">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="9b54e-172">CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.</span><span class="sxs-lookup"><span data-stu-id="9b54e-172">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="9b54e-173">IID</span><span class="sxs-lookup"><span data-stu-id="9b54e-173">IID</span></span><br/>                      | <span data-ttu-id="9b54e-174">IID \_ imsrdpextendedsettings ist definiert als 302d8188-0052-4807-806a-362b628fi9ac5</span><span class="sxs-lookup"><span data-stu-id="9b54e-174">IID\_IMsRdpExtendedSettings is defined as 302D8188-0052-4807-806A-362B628F9AC5</span></span><br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="9b54e-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b54e-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b54e-176">**Imsrdpextendedsettings**</span><span class="sxs-lookup"><span data-stu-id="9b54e-176">**IMsRdpExtendedSettings**</span></span>](imsrdpextendedsettings.md)
</dt> </dl>

 

 





