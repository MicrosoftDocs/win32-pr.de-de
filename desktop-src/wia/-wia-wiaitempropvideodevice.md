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
# <a name="video-wia-device-property-constants"></a>Video-WIA-Geräte Eigenschafts Konstanten

Der standardmäßige Windows-Abbild Erfassungs-(WIA)-Videotreiber (wiavusd.dll) unterstützt die folgenden Eigenschaften für Streaming-Videogeräte.

> [!Note]  
> WIA unterstützt keine Videogeräte in Windows Server 2003, Windows Vista oder höher. Verwenden Sie für diese Versionen von Windows [DirectShow](/previous-versions//ms783323(v=vs.85)) zum Abrufen von Bildern aus Videos.

 

Das Präfix "WIA \_ DPV \_ " gibt eine Geräte Eigenschaft für Video Geräte an und ist die Benennungs Konvention, die in C/C++ verwendet wird. Bei der Skripterstellung verwenden diese Konstanten das Präfix "VideoDevice" und sind Teil des enumerierten Typs [wiaitempropertyid](-wia-wiaitempropertyid.md) . Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.



| Konstante/Wert                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ \_Letzte \_ Abbildung \_ von DPV**</dt> <dt>videodevicelastpicturetaken</dt> </dl> | Diese Eigenschaft wird verwendet, um den WIA-Treiber zu benachrichtigen, dass ein neues Bild hinzugefügt wurde. Anwendungen sollten den Wert dieser Eigenschaft auf den Namen der Bilddatei festlegen, die als Ergebnis eines erfolgreichen Aufrufens der [**iwiavideo:: takepicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) -Methode erstellt wurde. <br/> Typ: VT \_ BSTR, Access: Lesen/Schreiben<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ DPV- \_ Abbild \_ Verzeichnis**</dt> <dt>videoenviceimagesdirectory</dt> </dl>         | Diese Eigenschaft wird vom Standard-WIA-Video-Benutzermodus-Treiber (wiavusd.dll) verfügbar gemacht. Der Wert dieser Eigenschaft ist der vollständige Pfad des Verzeichnisses, in dem der WIA-Videotreiber standardmäßig Bilder einfügt. Anwendungen sollten die [**iwiavideo:: imagesdirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) -Eigenschaft auf diesen Wert festlegen. <br/> Typ: VT \_ BSTR, Zugriff: schreibgeschützt<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ DPV \_ \_ ddisplay-Geräte \_ Pfad**</dt> <dt>videodebug-showdevicepath</dt> </dl>     | Der vollständige Pfad des DirectShow-Geräts. <br/> Typ: VT \_ BSTR, Zugriff: schreibgeschützt<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ DPF \_ - \_ Bereitstellungspunkt**</dt> <dt>filedevicemountpoint</dt> </dl>                              | Nicht implementiert. <br/> Type: **VT \_ I4**, Access: Read Only, gültige Werte: [WIA \_ Prop \_ None](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
