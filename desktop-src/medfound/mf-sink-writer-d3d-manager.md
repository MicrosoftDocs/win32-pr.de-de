---
description: Enthält einen Zeiger auf die DXGI-Geräte-Manager sink Writer.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: MF_SINK_WRITER_D3D_MANAGER -Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706287b6001ba52c8bf5ba8a19326948afcf4f7f7569c606507115f484c46f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714310"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>MF \_ SINK \_ WRITER \_ D3D \_ MANAGER-Attribut

Enthält einen Zeiger auf die DXGI-Geräte-Manager sink [Writer.](sink-writer.md)

## <a name="data-type"></a>Datentyp

**DURCHDXGIDeviceManager \* *_ gespeichert als _* IUnknown\***

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Zeiger auf die [**BENUTZERDEFINIERTEGIDeviceManager-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Videoencoder oder Mediensenken zur Verfügung zu stellen, die vom Sink Writer geladen werden.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sink Writer](sink-writer.md)
</dt> </dl>

 

 




