---
description: Ermöglicht es dem Quell-oder senkenwriter, hardwarebasierte Media Foundation Transformationen (MFTs) zu verwenden.
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347508"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>MF- \_ Lesevorgang \_ enable \_ Hardware Transformationen- \_ Attribut

Ermöglicht es dem Quell-oder senkenwriter, hardwarebasierte Media Foundation Transformationen (MFTs) zu verwenden.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Standardmäßig verwenden der Quell-und der sendende Writer keine Hardware-Decoder oder-Encoder. Um die Verwendung von Hardware-MFTs zu aktivieren, legen Sie dieses Attribut auf " **true** " fest, wenn Sie den Quell-oder sendenden Writer erstellen.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**Mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**Mfkreatesinkschreiterfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MF | atesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Es gibt eine Ausnahme zum Standardverhalten. Der Quell-und sendende Writer verwendet automatisch MFTs, die lokal im Prozess des Aufrufers registriert sind. Um eine MFT lokal zu registrieren, müssen Sie [**mftregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) oder [**mftregisterlocalbyclsid**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)aufrufen. Lokal registrierte Hardware-MFTs werden auch dann verwendet, wenn das Paket "read- **\_ \_ \_ Hardware \_ Transformationen aktivieren** " nicht festgelegt ist.

Dieses Attribut wirkt sich nicht auf die hardwarebeschleunigte Video Decodierung aus, die DirectX Video Acceleration (DXVA) verwendet. Legen Sie zum Aktivieren der DXVA-Decodierung im Quell Leser das [ \_ \_ \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -Attribut des MF-Quell Readers fest.

Wenn dieses Attribut auf **true** festgelegt ist, legen Sie das-Attribut für das [MF- \_ Lese schreiben \_ deaktiviert \_](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Senkenwriter-Attribute](sink-writer-attributes.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




