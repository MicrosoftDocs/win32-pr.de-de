---
description: Gibt das Zielformat für einen Encoder an.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Avenccommonformateinschränkungs-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e79536959aaaa0c50403bdd79d005bd48c729e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340093"
---
# <a name="avenccommonformatconstraint-property"></a>Avenccommonformateinschränkung (Eigenschaft)

Gibt das Zielformat für einen Encoder an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi- \_ avenccommonformateinschränkung**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein **BSTR** -Wert, der die Zeichen folgen Darstellung einer GUID enthält. Die folgenden GUIDs sind definiert.



| GUID                                         | Beschreibung                     |
|----------------------------------------------|---------------------------------|
| Codecapi \_ GUID \_ avenccommonformatatsc        | ATSC-Kabelfernsehen.          |
| Codecapi \_ GUID \_ avenccommonformatdvb         | DVB-Kabelfernsehen.           |
| Codecapi \_ GUID \_ avenccommonformatdvd \_ dashvr | DVD-VR                          |
| Codecapi \_ GUID \_ avenccommonformatdvd \_ plusvr | DVD + VR                          |
| Codecapi \_ GUID \_ avenccommonformatdvd \_ V      | DVD-Video                       |
| Codecapi- \_ GUID \_ avenccommonformathighmat     | HighMAT                         |
| Codecapi \_ GUID \_ avenccommonformathighmpv     | In dieser Version nicht dokumentiert. |
| Codecapi- \_ GUID \_ AVEncCommonFormatMP3         | MPEG-Audioschicht-3 (MP3)        |
| Codecapi \_ GUID \_ avenccommonformatsvcd        | Super Video-CD (SVCD)           |
| Codecapi \_ GUID \_ avenccommonformatunspezifiziert | Nicht angegebenes Format.             |
| Codecapi \_ GUID \_ avenccommonformatvcd         | Video-CD (VCD)                  |



 

## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft festlegen, um das Zielformat anzugeben. Encoder können diese Eigenschaft auch als Funktion zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




