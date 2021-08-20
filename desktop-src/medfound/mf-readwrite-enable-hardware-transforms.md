---
description: Ermöglicht dem Quellleser oder Senkenwriter die Verwendung hardwarebasierter Media Foundation Transformationen (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS-Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f851ba188f8a2cc42140b799e23156cdc8e5c06bb474deb16debf508c173a908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059533"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>MF \_ READWRITE \_ ENABLE HARDWARE \_ \_ TRANSFORMS-Attribut

Ermöglicht dem Quellleser oder Senkenwriter die Verwendung hardwarebasierter Media Foundation Transformationen (MFTs).

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Standardmäßig verwenden der Quellleser und der Senkenwriter keine Hardwaredecoder oder Encoder. Um die Verwendung von Hardware-MFTs zu aktivieren, legen Sie dieses Attribut beim Erstellen des Quelllesers oder Senkenwriters auf **TRUE** fest.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Es gibt eine Ausnahme vom Standardverhalten. Der Quellleser und der Senkenwriter verwenden automatisch MFTs, die lokal im Prozess des Aufrufers registriert sind. Um ein MFT lokal zu registrieren, rufen Sie [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) oder [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)auf. Hardware-MFTs, die lokal registriert sind, werden auch dann verwendet, wenn das **ATTRIBUT MF \_ READWRITE \_ ENABLE HARDWARE \_ \_ TRANSFORMS** nicht festgelegt ist.

Dieses Attribut wirkt sich nicht auf die hardwarebeschleunigte Videodecodierung aus, die DirectX Video Acceleration (DXVA) verwendet. Legen Sie das ATTRIBUT MF SOURCE READER [ \_ \_ \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md) fest, um die DXVA-Decodierung im Quellleser zu aktivieren.

Wenn dieses Attribut **TRUE** ist, legen Sie das [MF \_ READWRITE \_ DISABLE \_ CONVERTERS-Attribut](mf-readwrite-disable-converters.md) nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sink Writer-Attribute](sink-writer-attributes.md)
</dt> <dt>

[Quellleseattribute](source-reader-attributes.md)
</dt> </dl>

 

 




