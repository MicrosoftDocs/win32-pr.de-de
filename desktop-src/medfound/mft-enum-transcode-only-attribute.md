---
description: Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0951d4f370849678eb88ecbd9751c417a7e50d2bd709ad1f2c5b6cf96f5f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973079"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>Attribut MFT \_ ENUM \_ TRANSCODE \_ ONLY \_ ATTRIBUTE

Gibt an, ob ein Decoder für die Transcodierung und nicht für die Wiedergabe optimiert ist.

Dieses Attribut gilt derzeit nur für hardwarebasierte Decoder, die den AVStream-Minitreiber verwenden. Das Attribut wird in der Registrierung unter den Funktioneninformationen des Decoders gespeichert. Weitere Informationen finden Sie in der Dokumentation zu [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).

Anwendungen verwenden dieses Attribut in der Regel nicht.

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Hinweise

Wenn dieser Registrierungseintrag vorhanden ist und gleich 1 ist, überspringt die [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) den Decoder, es sei denn, der Aufrufer hat das **\_ MFT-ENUM-FLAG \_ \_ TRANSCODE \_ ONLY-Flag** in **MFTEnumEx** angegeben.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
