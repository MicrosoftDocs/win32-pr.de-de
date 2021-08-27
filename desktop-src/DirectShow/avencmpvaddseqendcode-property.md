---
description: Gibt an, ob der Encoder am Ende des Streams einen Sequenzendcode hinzufügt. Diese Eigenschaft gilt für MPEG-Videoencoder.
ms.assetid: ef606207-2ee3-420b-afae-67c764e05e54
title: AVEncMPVAddSeqEndCode-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba3d757bd3023ca9539172c96f6f276bc1833eb7c4e24c8b2bb3adc6038d77c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087590"
---
# <a name="avencmpvaddseqendcode-property"></a>AVEncMPVAddSeqEndCode (Eigenschaft)

Gibt an, ob der Encoder am Ende des Streams einen Sequenzendcode hinzufügt. Diese Eigenschaft gilt für MPEG-Videoencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPVAddSeqEndCode**

## <a name="remarks"></a>Hinweise

Wenn der Wert **VARIANT \_ TRUE ist,** fügt der Encoder einen Sequenzendcode am Ende des Streams hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




