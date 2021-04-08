---
description: Gibt an, ob der Encoder die VBR-Codierung (Variable Bitrate) verwendet.
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: MFPKEY_VBRENABLED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864128"
---
# <a name="mfpkey_vbrenabled-property"></a>Mfpkey \_ vbrenabled (Eigenschaft)

Gibt an, ob der Encoder die VBR-Codierung (Variable Bitrate) verwendet. Lese-/Schreibzugriff.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

**g \_ wszwmvcvbrenabled**, **g \_ wszwmcpaudiovbrsupported**

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Dieser Wert muss für alle anderen VBR-Eigenschaften, die vom Codec verwendet werden sollen, auf **Variant \_ true** festgelegt werden.

Nachdem Sie diesen Wert für den Audioencoder auf **Variant \_ true** festgelegt haben, sind die mithilfe der [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) -Methode abgerufenen Ausgabetypen VBR-Typen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mfpkey \_ schränkt die \_ Enumeration von \_ vbrquality ein**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**mfpkey \_ gewünschte \_ vbrquality**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
