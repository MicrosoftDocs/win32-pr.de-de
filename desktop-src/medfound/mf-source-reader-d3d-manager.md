---
description: Enthält einen Zeiger auf den Microsoft Direct3D-Device Manager für den Quell Reader.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: MF_SOURCE_READER_D3D_MANAGER-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865579"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>MF- \_ Quell \_ Leser \_ D3D Manager- \_ Attribut

Enthält einen Zeiger auf den Microsoft [Direct3D-Device Manager](direct3d-device-manager.md) für den [Quell Reader](source-reader.md).

## <a name="data-type"></a>Datentyp

**IDirect3DDeviceManager9 \* oder IMF dxgidebug Manager \*** gespeichert als **IUnknown \** _

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs kann ein Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle oder ein [**imfdxgidebug Manager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)sein.

Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Video-Decoder bereitzustellen, die vom Quell Leser geladen werden. Wenn Sie dieses Attribut festlegen und der Decoder Microsoft DirectX Video Acceleration (DXVA) unterstützt, verwendet der Quell Leser das Direct3D-Gerät zum Zuordnen von Video Puffern. Diese Puffer sind kompatibel mit dem DXVA 2-Videoprozessor. (Siehe [DXVA-Video Verarbeitung](dxva-video-processing.md).)

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**Mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

In der Regel legen Sie dieses Attribut fest, wenn Sie den Quell Reader verwenden, um decodierte Video Frames zu erhalten und die Frames mithilfe von Direct3D anzuzeigen. Durch Festlegen dieses Attributs kann der Decoder DXVA verwenden.

Sie würden dieses Attribut nicht festlegen, wenn Folgendes:

-   Sie verwenden den Quell Reader, um nur Audioinhalte und keine Videos zu verarbeiten.
-   Sie erhalten komprimierte Videos vom Quell-Reader. In diesem Fall erstellt der Quell Leser keinen Decoder.

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

[Quell Leser](source-reader.md)
</dt> <dt>

[Attribute des Quell Readers](source-reader-attributes.md)
</dt> </dl>

 

 




