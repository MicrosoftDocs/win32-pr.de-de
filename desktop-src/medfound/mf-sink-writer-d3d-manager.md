---
description: Enthält einen Zeiger auf den DXGI-Device Manager für den Senke-Writer.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: MF_SINK_WRITER_D3D_MANAGER-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352542"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>MF \_ Sink \_ Writer \_ D3D \_ Manager-Attribut

Enthält einen Zeiger auf den DXGI-Device Manager für den [Senke-Writer](sink-writer.md).

## <a name="data-type"></a>Datentyp

**IMF dxgidebug Manager \** _ als " _*IUnknown \** " gespeichert_

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfdxgidebug Manager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle.

Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Video Encoder oder Medien senken bereitzustellen, die vom senkenwriter geladen werden.

Verwenden Sie dieses Attribut mit den folgenden Funktionen:

-   [**Mfkreatesinkschreiterfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MF | atesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Senke-Writer](sink-writer.md)
</dt> </dl>

 

 




