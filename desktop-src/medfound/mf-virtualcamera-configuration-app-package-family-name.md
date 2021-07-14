---
description: Gibt den Namen der App-Paketfamilie für eine Konfigurationsanwendung für virtuelle Kamera an.
title: MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691857"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a><span data-ttu-id="c1c6d-103">MF \_ VIRTUALCAMERA \_ APP PACKAGE FAMILY \_ \_ \_ NAME-Attribut</span><span class="sxs-lookup"><span data-stu-id="c1c6d-103">MF\_VIRTUALCAMERA\_APP\_PACKAGE\_FAMILY\_NAME attribute</span></span>

<span data-ttu-id="c1c6d-104">Gibt den Namen der App-Paketfamilie für eine Konfigurationsanwendung für virtuelle Kamera an.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-104">Specifies the app package family name for a virtual camera configuration application.</span></span> <span data-ttu-id="c1c6d-105">Wenn angegeben, wird die Konfigurationsanwendung der virtuellen Kamera von der Pipeline zugeordnet und ein Startpunkt auf der Seite Kamera Einstellungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-105">When provided, the pipeline will associate the configuration application with the virtual camera and provide a launch point within the Camera Settings page.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1c6d-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c1c6d-106">Data type</span></span>

[<span data-ttu-id="c1c6d-107">MF_ATTRIBUTE_STRING</span><span class="sxs-lookup"><span data-stu-id="c1c6d-107">MF_ATTRIBUTE_STRING</span></span>](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a><span data-ttu-id="c1c6d-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1c6d-108">Remarks</span></span>

<span data-ttu-id="c1c6d-109">Dieses Attribut kann von der benutzerdefinierten Medienquelle der virtuellen Kamera aus dem [MedienquellenattributspeicherSGEMEDIASourceEx::GetSourceAttributes verfügbar gemacht werden.](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource)</span><span class="sxs-lookup"><span data-stu-id="c1c6d-109">This attribute may be exposed by the virtual camera custom media source from the media source attribute store [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span></span>  

<span data-ttu-id="c1c6d-110">Wenn die Konfigurationsanwendung noch nicht auf dem Computer installiert ist, wird die Store-Anwendung gestartet und zu der Anwendungsseite navigiert, die durch den Paketfamiliennamen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-110">If the configuration application is not yet installed on the machine, the Store application will be launched and navigated to the application page specified by the package family name.</span></span> <span data-ttu-id="c1c6d-111">Andernfalls wird die installierte Anwendung für den Benutzer gestartet.</span><span class="sxs-lookup"><span data-stu-id="c1c6d-111">Otherwise, the installed application will be launched for the user.</span></span>


## <a name="requirements"></a><span data-ttu-id="c1c6d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1c6d-112">Requirements</span></span>



| <span data-ttu-id="c1c6d-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1c6d-113">Requirement</span></span> | <span data-ttu-id="c1c6d-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c1c6d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c6d-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1c6d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c6d-116">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="c1c6d-116">Windows Build 22000</span></span><br/>                          |
| <span data-ttu-id="c1c6d-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1c6d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c6d-118">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="c1c6d-118">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="c1c6d-119">Header</span><span class="sxs-lookup"><span data-stu-id="c1c6d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c6d-120"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c6d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c6d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1c6d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c6d-122">Alphabetische Liste Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c1c6d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1c6d-123">**ATTRIBUTEs::GetString**</span><span class="sxs-lookup"><span data-stu-id="c1c6d-123">**IMFAttributes::GetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="c1c6d-124">**ATTRIBUTEs::SetString**</span><span class="sxs-lookup"><span data-stu-id="c1c6d-124">**IMFAttributes::SetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




