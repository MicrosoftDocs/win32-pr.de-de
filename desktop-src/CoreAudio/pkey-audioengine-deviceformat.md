---
description: Die pkey \_ Audioengine \_ deviceformat-Eigenschaft gibt das Geräte Format an. Hierbei handelt es sich um das Format, das vom Benutzer für den Datenstrom zwischen der Audioengine und dem audioendpunktgerät ausgewählt wird, wenn das Gerät im freigegebenen Modus betrieben wird.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748904"
---
# <a name="pkey_audioengine_deviceformat"></a><span data-ttu-id="c53dc-103">Pkey \_ Audioengine \_ deviceformat</span><span class="sxs-lookup"><span data-stu-id="c53dc-103">PKEY\_AudioEngine\_DeviceFormat</span></span>

<span data-ttu-id="c53dc-104">Die **pkey \_ Audioengine \_ deviceformat** -Eigenschaft gibt das Geräte Format an. Hierbei handelt es sich um das Format, das vom Benutzer für den Datenstrom zwischen der Audioengine und dem audioendpunktgerät ausgewählt wird, wenn das Gerät im freigegebenen Modus betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c53dc-104">The **PKEY\_AudioEngine\_DeviceFormat** property specifies the device format, which is the format that the user has selected for the stream that flows between the audio engine and the audio endpoint device when the device operates in shared mode.</span></span> <span data-ttu-id="c53dc-105">Dieses Format ist möglicherweise nicht das beste Standardformat, das von einer Anwendung im exklusiven Modus verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c53dc-105">This format might not be the best default format for an exclusive-mode application to use.</span></span> <span data-ttu-id="c53dc-106">In der Regel sucht eine Anwendung im exklusiven Modus nach einem passenden Geräte Format, indem eine Reihe von Aufrufen der [**iaudioclient:: isformatsupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) -Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c53dc-106">Typically, an exclusive-mode application finds a suitable device format by making some number of calls to the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method.</span></span> <span data-ttu-id="c53dc-107">Weitere Informationen finden Sie unter [Geräte Formate](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="c53dc-107">For more information, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="c53dc-108">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf einen VT- \_ BLOB festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c53dc-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="c53dc-109">Der **BLOB** -Member der **PROPVARIANT** -Struktur ist eine Struktur vom Typ " **BLOB** ", die zwei Member enthält.</span><span class="sxs-lookup"><span data-stu-id="c53dc-109">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="c53dc-110">Member **BLOB. cbSize** ist ein **DWORD** -Wert, der die Anzahl der Bytes in der Formatbeschreibung angibt.</span><span class="sxs-lookup"><span data-stu-id="c53dc-110">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="c53dc-111">Member **BLOB. pblobdata** verweist auf eine **WaveFormatEx** -Struktur, die die Formatbeschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="c53dc-111">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="c53dc-112">Weitere Informationen zum **BLOB** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c53dc-112">For more information about **BLOB**, see the Windows SDK documentation.</span></span> <span data-ttu-id="c53dc-113">Weitere Informationen zu **WaveFormatEx** finden Sie in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c53dc-113">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c53dc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c53dc-114">Requirements</span></span>



| <span data-ttu-id="c53dc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c53dc-115">Requirement</span></span> | <span data-ttu-id="c53dc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c53dc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c53dc-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c53dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c53dc-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c53dc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c53dc-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c53dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c53dc-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c53dc-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c53dc-121">Header</span><span class="sxs-lookup"><span data-stu-id="c53dc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c53dc-122"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c53dc-122"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c53dc-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c53dc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c53dc-124">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="c53dc-124">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="c53dc-125">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="c53dc-125">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




