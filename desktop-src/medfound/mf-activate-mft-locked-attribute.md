---
description: Gibt an, ob das Topologielader die Medientypen auf einer Media Foundation Transform (MFT) ändert. Anwendungen verwenden dieses Attribut in der Regel nicht.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: MF_ACTIVATE_MFT_LOCKED -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445447af46e1ce1da25aaa075dd4490d1210c1d01b2e7717829d2672dc74701f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060910"
---
# <a name="mf_activate_mft_locked-attribute"></a>MF \_ ACTIVATE \_ MFT \_ LOCKED-Attribut

Gibt an, ob das Topologielader die Medientypen auf einer Media Foundation Transform (MFT) ändert. Anwendungen verwenden dieses Attribut in der Regel nicht.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Wenn der Wert dieses Attributs ungleich 0 (null) ist, ändert das Topologielader die Medientypen auf dem MFT nicht. Das Topologielader legt dieses Attribut fest, nachdem es die Topologie geladen hat.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




