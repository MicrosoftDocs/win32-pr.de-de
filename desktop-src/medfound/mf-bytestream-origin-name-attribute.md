---
description: Gibt die ursprüngliche URL für einen Byte Datenstrom an.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: MF_BYTESTREAM_ORIGIN_NAME-Attribut (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353120"
---
# <a name="mf_bytestream_origin_name-attribute"></a>MF- \_ Bytestream- \_ Ursprungs \_ Namensattribut

Gibt die ursprüngliche URL für einen Byte Datenstrom an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Bemerkungen

Dateibasierte Byte Datenströme können dieses Attribut unterstützen. Der Attribut Wert wird festgelegt, wenn der Byte Datenstrom erstellt wird. Um den Attribut Wert zu erhalten, Fragen Sie das Byte Datenstrom Objekt für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Byte Datenstrom Attribute](byte-stream-attributes.md)
</dt> <dt>

[**Imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




