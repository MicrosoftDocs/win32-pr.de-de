---
description: Ermöglicht es dem Quell Leser, Media Foundation Transformationen (MFTs) zu verwenden, die für die Transcodierung optimiert sind.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525991"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>MF- \_ Quell \_ Leser Aktivieren von \_ \_ transcode \_ only- \_ Attribut Transformationen

Ermöglicht es dem [Quell Leser](source-reader.md) , Media Foundation Transformationen (MFTs) zu verwenden, die für die Transcodierung optimiert sind.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Einige MFTs, insbesondere Decoder, sind für die Transcodierung und nicht für die Wiedergabe optimiert. Standardmäßig lädt der Quell Leser diese Transformationen nicht. Legen Sie dieses Attribut auf " **true** " fest, wenn Sie Transcodierung-MFTs mit dem Quell Leser verwenden möchten.

Eine Anwendung kann dieses Attribut festlegen, wenn Sie die Daten nicht in Echtzeit verarbeitet (für die Transcodierung oder ähnliche Szenarien). Verwenden Sie andernfalls für die Echt Zeit Wiedergabe das Standardverhalten.

Intern bewirkt dieses Attribut, dass der Quell Leser beim Aufrufen von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)das Flag **\_ \_ \_ transcode \_ only für das MFT-Enum-Flag** einschließt.

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

[Quell Leser](source-reader.md)
</dt> </dl>

 

 




