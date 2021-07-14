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
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a>MF \_ VIRTUALCAMERA \_ APP PACKAGE FAMILY \_ \_ \_ NAME-Attribut

Gibt den Namen der App-Paketfamilie für eine Konfigurationsanwendung für virtuelle Kamera an. Wenn angegeben, wird die Konfigurationsanwendung der virtuellen Kamera von der Pipeline zugeordnet und ein Startpunkt auf der Seite Kamera Einstellungen bereitgestellt.

## <a name="data-type"></a>Datentyp

[MF_ATTRIBUTE_STRING](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a>Hinweise

Dieses Attribut kann von der benutzerdefinierten Medienquelle der virtuellen Kamera aus dem [MedienquellenattributspeicherSGEMEDIASourceEx::GetSourceAttributes verfügbar gemacht werden.](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource)  

Wenn die Konfigurationsanwendung noch nicht auf dem Computer installiert ist, wird die Store-Anwendung gestartet und zu der Anwendungsseite navigiert, die durch den Paketfamiliennamen angegeben wird. Andernfalls wird die installierte Anwendung für den Benutzer gestartet.


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Build 22000<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Build 22000<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEs::SetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




