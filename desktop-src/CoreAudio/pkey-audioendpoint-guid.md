---
description: Die pkey \_ audioendpoint \_ GUID-Eigenschaft stellt den DirectSound-Geräte Bezeichner bereit, der dem audioendpunktgerät entspricht.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346247"
---
# <a name="pkey_audioendpoint_guid"></a><span data-ttu-id="93114-103">Pkey- \_ audioendpunkt- \_ GUID</span><span class="sxs-lookup"><span data-stu-id="93114-103">PKEY\_AudioEndpoint\_GUID</span></span>

<span data-ttu-id="93114-104">Die **pkey \_ audioendpoint \_ GUID** -Eigenschaft stellt den DirectSound-Geräte Bezeichner bereit, der dem audioendpunktgerät entspricht.</span><span class="sxs-lookup"><span data-stu-id="93114-104">The **PKEY\_AudioEndpoint\_GUID** property supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span> <span data-ttu-id="93114-105">Der Eigenschafts Wert ist eine GUID, die der Client als Geräte Bezeichner für die **directsoundcreate** -oder **directsoundcaptuneu** -Funktion in der DirectSound-API bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="93114-105">The property value is a GUID that the client can supply as the device identifier to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function in the DirectSound API.</span></span> <span data-ttu-id="93114-106">Durch diesen Wert wird das audioendpunktgerät für alle audioendpunktgeräte im System eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="93114-106">This value uniquely identifies the audio endpoint device across all audio endpoint devices in the system.</span></span> <span data-ttu-id="93114-107">Weitere Informationen zu DirectSound finden Sie in der DirectX SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="93114-107">For more information about DirectSound, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="93114-108">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ LPWSTR festgelegt.</span><span class="sxs-lookup"><span data-stu-id="93114-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="93114-109">Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine GUID enthält, die das audioendpunktgerät in DirectSound identifiziert.</span><span class="sxs-lookup"><span data-stu-id="93114-109">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the audio endpoint device in DirectSound.</span></span>

<span data-ttu-id="93114-110">Wie bereits erläutert, unterstützt die [mmdevice-API](mmdevice-api.md) [Geräte Rollen](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="93114-110">As explained previously, the [MMDevice API](mmdevice-api.md) supports [device roles](device-roles.md).</span></span> <span data-ttu-id="93114-111">Obwohl DirectSound Geräte Rollen nicht direkt unterstützt, kann ein DirectSound-Client die pkey \_ audioendpoint- \_ GUID-Eigenschaft verwenden, um auf der Grundlage seiner Geräte Rolle ein DirectSound-Rendering oder-Erfassungsgerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="93114-111">Although DirectSound does not directly support device roles, a DirectSound client can use the PKEY\_AudioEndpoint\_GUID property to select a DirectSound rendering or capture device based on its device role.</span></span>

<span data-ttu-id="93114-112">Beispielsweise führt eine DirectSound-Anwendung die folgenden Schritte aus, um ein DirectSound-Gerät zu erstellen, das dem renderingendpunktgerät entspricht, dem der Benutzer die emultimedia-Rolle zugewiesen hat:</span><span class="sxs-lookup"><span data-stu-id="93114-112">For example, a DirectSound application performs the following steps to create a DirectSound device that corresponds to the rendering endpoint device that the user has assigned the eMultimedia role to:</span></span>

1.  <span data-ttu-id="93114-113">Aufrufen der [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode zum Abrufen der [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle des renderingendpunktgeräts, das über die emultimedia-Rolle verfügt.</span><span class="sxs-lookup"><span data-stu-id="93114-113">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the rendering endpoint device that has the eMultimedia role.</span></span>
2.  <span data-ttu-id="93114-114">Rufen Sie die [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) -Methode auf, um die **IPropertyStore** -Schnittstelle des emultimedia-Geräts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93114-114">Call the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to obtain the **IPropertyStore** interface of the eMultimedia device.</span></span> <span data-ttu-id="93114-115">Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="93114-115">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>
3.  <span data-ttu-id="93114-116">Rufen Sie die **IPropertyStore:: GetValue** -Methode auf, um den pkey \_ audioendpoint- \_ GUID-Eigenschafts Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93114-116">Call the **IPropertyStore::GetValue** method to obtain the PKEY\_AudioEndpoint\_GUID property value.</span></span>
4.  <span data-ttu-id="93114-117">Konvertieren Sie den Eigenschafts Wert von einer GUID im Zeichen folgen Format in eine 16-Byte-GUID-Struktur.</span><span class="sxs-lookup"><span data-stu-id="93114-117">Convert the property value from a GUID in string format to a 16-byte GUID structure.</span></span>
5.  <span data-ttu-id="93114-118">Rufen Sie die **DirectSound Create** -Funktion mit der GUID auf, um das Gerät mit der emultimedia-Rolle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93114-118">Call the **DirectSoundCreate** function with the GUID to create the device with the eMultimedia role.</span></span>

> [!Note]  
> <span data-ttu-id="93114-119">**Pkey \_ Audioendpoint \_ GUID** ist eine schreibgeschützte Eigenschaft, unabhängig vom Speicherzugriffs Modus, der von der Anwendung in [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore)angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="93114-119">**PKEY\_AudioEndpoint\_GUID** is a read-only property regardless of the storage-access mode requested by the application in [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span></span> <span data-ttu-id="93114-120">Wenn eine Anwendung versucht, mithilfe von **IPropertyStore:: SetValue** einen Wert festzulegen, schlägt dieser-Befehl mit dem \_ Fehlercode "E AccessDenied" fehl.</span><span class="sxs-lookup"><span data-stu-id="93114-120">If an application attempts to set a value by using **IPropertyStore::SetValue**, this call fails with the E\_ACCESSDENIED error code.</span></span>

 

<span data-ttu-id="93114-121">Beachten Sie, dass die in Schritt 4 generierte 16-Byte-GUID mit der Geräte-GUID übereinstimmt, die das Gerät während der DirectSound-Geräte Enumeration identifiziert.</span><span class="sxs-lookup"><span data-stu-id="93114-121">Note that the 16-byte GUID generated in step 4 matches the device GUID that identifies the device during DirectSound device enumeration.</span></span> <span data-ttu-id="93114-122">Die Funktion " **directsoundenumerate** " listet renderingendpunktgeräte auf, und die Funktion " **directsoundcaptureenumerate** " listet Erfassungs Endpunkt Geräte auf.</span><span class="sxs-lookup"><span data-stu-id="93114-122">The **DirectSoundEnumerate** function enumerates rendering endpoint devices, and the **DirectSoundCaptureEnumerate** function enumerates capture endpoint devices.</span></span> <span data-ttu-id="93114-123">In beiden Fällen ist die Geräte-GUID der erste Parameter, der an die enumerationsrückruf-Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="93114-123">In either case, the device GUID is the first parameter passed to the enumeration callback function.</span></span> <span data-ttu-id="93114-124">Weitere Informationen zur DirectSound-Enumeration finden Sie in der DirectX SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="93114-124">For more information about DirectSound enumeration, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="93114-125">Ein Codebeispiel, in dem die pkey \_ audioendpoint- \_ GUID-Eigenschaft verwendet wird, finden Sie unter [Geräte Rollen für DirectSound-Anwendungen](device-roles-for-directsound-applications.md).</span><span class="sxs-lookup"><span data-stu-id="93114-125">For a code example that uses the PKEY\_AudioEndpoint\_GUID property, see [Device Roles for DirectSound Applications](device-roles-for-directsound-applications.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93114-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93114-126">Requirements</span></span>



| <span data-ttu-id="93114-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93114-127">Requirement</span></span> | <span data-ttu-id="93114-128">Wert</span><span class="sxs-lookup"><span data-stu-id="93114-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93114-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93114-129">Minimum supported client</span></span><br/> | <span data-ttu-id="93114-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93114-130">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="93114-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93114-131">Minimum supported server</span></span><br/> | <span data-ttu-id="93114-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93114-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="93114-133">Header</span><span class="sxs-lookup"><span data-stu-id="93114-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="93114-134"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="93114-134"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93114-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93114-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93114-136">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="93114-136">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="93114-137">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="93114-137">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




