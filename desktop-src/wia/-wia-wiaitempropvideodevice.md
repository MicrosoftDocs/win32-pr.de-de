---
description: Der standardmäßige WIA-Videotreiber (Windows Image Acquisition) (wiavusd.dll) unterstützt die folgenden Eigenschaften für Streamingvideogeräte.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: WIA-Geräteeigenschaftskonstanten für Video (Wiadef.h)
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
ms.openlocfilehash: 9652ac72d6e73a9c44d2f4b299823dad9cc566bb1c7c0129af497ea213a6e5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207368"
---
# <a name="video-wia-device-property-constants"></a>WIA-Geräteeigenschaftskonstanten für Video

Der standardmäßige WIA-Videotreiber (Windows Image Acquisition) (wiavusd.dll) unterstützt die folgenden Eigenschaften für Streamingvideogeräte.

> [!Note]  
> WIA unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher. Verwenden Sie für diese Versionen der Windows [DirectShow,](/previous-versions//ms783323(v=vs.85)) um Bilder aus Videos zu erhalten.

 

Das Präfix "WIA \_ \_ DPV" gibt eine Geräteeigenschaft für Videogeräte an und ist die benennungskonvention, die in C/C++ verwendet wird. Zu Skriptzwecken verwenden diese Konstanten das Präfix "VideoDevice" und sind Teil des Aufzählungstyps [WiaItemPropertyId.](-wia-wiaitempropertyid.md) Der entsprechende Membername aus dieser Skriptenumeration wird in Klammern neben dem C/C++-Konstantennamen in der folgenden Liste angezeigt.



| Konstante/Wert                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ DPV \_ LAST \_ PICTURE \_ TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt> </dl> | Diese Eigenschaft wird verwendet, um den WIA-Treiber zu benachrichtigen, dass ein neues Image hinzugefügt wurde. Anwendungen sollten den Wert dieser Eigenschaft auf den Namen der Imagedatei festlegen, die als Ergebnis eines erfolgreichen Aufrufs der [**IWiaVideo::TakePicture-Methode**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) erstellt wurde. <br/> Typ: VT \_ BSTR, Zugriff: Lesen/Schreiben<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ DPV \_ IMAGES \_ DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Diese Eigenschaft wird vom standardmäßigen WIA-Videobenutzermodustreiber (wiavusd.dll) verfügbar gemacht. Der Wert dieser Eigenschaft ist der vollständige Pfad des Verzeichnisses, in dem der WIA-Videotreiber standardmäßig Bilder ablegt. Anwendungen sollten die [**IWiaVideo::ImagesDirectory-Eigenschaft**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) auf diesen Wert festlegen. <br/> Typ: VT \_ BSTR, Zugriff: Schreibgeschützte<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ DPV \_ DSHOW \_ DEVICE \_ PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | Der vollständige Pfad des DirectShow-Geräts. <br/> Typ: VT \_ BSTR, Zugriff: Schreibgeschützte<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ DPF \_ MOUNT \_ POINT**</dt> <dt>FileDeviceMountPoint</dt> </dl>                              | Nicht implementiert. <br/> Typ: **VT \_ I4**, Zugriff: Schreibzugriff, Gültige Werte: [WIA \_ PROP \_ NONE](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
