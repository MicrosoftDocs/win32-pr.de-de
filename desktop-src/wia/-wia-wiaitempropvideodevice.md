---
description: Der standardmäßige Windows-Abbild Erfassungs-(WIA)-Videotreiber (wiavusd.dll) unterstützt die folgenden Eigenschaften für Streaming-Videogeräte.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Video-WIA-Geräte Eigenschafts Konstanten (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129376"
---
# <a name="video-wia-device-property-constants"></a><span data-ttu-id="98aac-103">Video-WIA-Geräte Eigenschafts Konstanten</span><span class="sxs-lookup"><span data-stu-id="98aac-103">Video WIA Device Property Constants</span></span>

<span data-ttu-id="98aac-104">Der standardmäßige Windows-Abbild Erfassungs-(WIA)-Videotreiber (wiavusd.dll) unterstützt die folgenden Eigenschaften für Streaming-Videogeräte.</span><span class="sxs-lookup"><span data-stu-id="98aac-104">The standard Windows Image Acquisition (WIA) video driver (wiavusd.dll) supports the following properties for streaming video devices.</span></span>

> [!Note]  
> <span data-ttu-id="98aac-105">WIA unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="98aac-105">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="98aac-106">Verwenden Sie für diese Versionen von Windows [DirectShow](/previous-versions//ms783323(v=vs.85)) zum Abrufen von Bildern aus Videos.</span><span class="sxs-lookup"><span data-stu-id="98aac-106">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

<span data-ttu-id="98aac-107">Das Präfix "WIA \_ DPV \_ " gibt eine Geräte Eigenschaft für Video Geräte an und ist die Benennungs Konvention, die in C/C++ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98aac-107">The prefix "WIA\_DPV\_" indicates a Device Property for Video devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="98aac-108">Bei der Skripterstellung verwenden diese Konstanten das Präfix "VideoDevice" und sind Teil des enumerierten Typs [wiaitempropertyid](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="98aac-108">For scripting purposes these constants use the prefix "VideoDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="98aac-109">Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="98aac-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



| <span data-ttu-id="98aac-110">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="98aac-110">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="98aac-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98aac-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <span data-ttu-id="98aac-112"><dt>**WIA \_ \_Letzte \_ Abbildung \_ von DPV**</dt> <dt>videodevicelastpicturetaken</dt></span><span class="sxs-lookup"><span data-stu-id="98aac-112"><dt>**WIA\_DPV\_LAST\_PICTURE\_TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt></span></span> </dl> | <span data-ttu-id="98aac-113">Diese Eigenschaft wird verwendet, um den WIA-Treiber zu benachrichtigen, dass ein neues Bild hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="98aac-113">This property is used to notify the WIA driver that a new image has been added.</span></span> <span data-ttu-id="98aac-114">Anwendungen sollten den Wert dieser Eigenschaft auf den Namen der Bilddatei festlegen, die als Ergebnis eines erfolgreichen Aufrufens der [**iwiavideo:: takepicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) -Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="98aac-114">Applications should set the value of this property to the name of the image file created as the result of a successful call to the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method.</span></span> <br/> <span data-ttu-id="98aac-115">Typ: VT \_ BSTR, Access: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="98aac-115">Type: VT\_BSTR, Access: Read/Write</span></span><br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <span data-ttu-id="98aac-116"><dt>**WIA \_ DPV- \_ Abbild \_ Verzeichnis**</dt> <dt>videoenviceimagesdirectory</dt></span><span class="sxs-lookup"><span data-stu-id="98aac-116"><dt>**WIA\_DPV\_IMAGES\_DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt></span></span> </dl>         | <span data-ttu-id="98aac-117">Diese Eigenschaft wird vom Standard-WIA-Video-Benutzermodus-Treiber (wiavusd.dll) verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="98aac-117">This property is exposed by the standard WIA video user-mode driver (wiavusd.dll).</span></span> <span data-ttu-id="98aac-118">Der Wert dieser Eigenschaft ist der vollständige Pfad des Verzeichnisses, in dem der WIA-Videotreiber standardmäßig Bilder einfügt.</span><span class="sxs-lookup"><span data-stu-id="98aac-118">The value of this property is the full path of the directory where the WIA video driver puts images by default.</span></span> <span data-ttu-id="98aac-119">Anwendungen sollten die [**iwiavideo:: imagesdirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) -Eigenschaft auf diesen Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="98aac-119">Applications should set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property to this value.</span></span> <br/> <span data-ttu-id="98aac-120">Typ: VT \_ BSTR, Zugriff: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98aac-120">Type: VT\_BSTR, Access: Read Only</span></span><br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <span data-ttu-id="98aac-121"><dt>**WIA \_ DPV \_ \_ ddisplay-Geräte \_ Pfad**</dt> <dt>videodebug-showdevicepath</dt></span><span class="sxs-lookup"><span data-stu-id="98aac-121"><dt>**WIA\_DPV\_DSHOW\_DEVICE\_PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt></span></span> </dl>     | <span data-ttu-id="98aac-122">Der vollständige Pfad des DirectShow-Geräts.</span><span class="sxs-lookup"><span data-stu-id="98aac-122">The full path of the DirectShow device.</span></span> <br/> <span data-ttu-id="98aac-123">Typ: VT \_ BSTR, Zugriff: schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98aac-123">Type: VT\_BSTR, Access: Read Only</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <span data-ttu-id="98aac-124"><dt>**WIA \_ DPF \_ - \_ Bereitstellungspunkt**</dt> <dt>filedevicemountpoint</dt></span><span class="sxs-lookup"><span data-stu-id="98aac-124"><dt>**WIA\_DPF\_MOUNT\_POINT**</dt> <dt>FileDeviceMountPoint</dt></span></span> </dl>                              | <span data-ttu-id="98aac-125">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="98aac-125">Not implemented.</span></span> <br/> <span data-ttu-id="98aac-126">Type: **VT \_ I4**, Access: Read Only, gültige Werte: [WIA \_ Prop \_ None](-wia-property-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="98aac-126">Type: **VT\_I4**, Access: Read Only, Valid values: [WIA\_PROP\_NONE](-wia-property-attributes.md)</span></span><br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="98aac-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98aac-127">Requirements</span></span>



| <span data-ttu-id="98aac-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98aac-128">Requirement</span></span> | <span data-ttu-id="98aac-129">Wert</span><span class="sxs-lookup"><span data-stu-id="98aac-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="98aac-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98aac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="98aac-131">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98aac-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="98aac-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98aac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="98aac-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98aac-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="98aac-134">Header</span><span class="sxs-lookup"><span data-stu-id="98aac-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="98aac-135"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="98aac-135"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
