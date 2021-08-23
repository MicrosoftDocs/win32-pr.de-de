---
description: Ermöglicht dem Quellleser die Verwendung Media Foundation Transformationen (MFTs), die für die Transcodierung optimiert sind.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS -Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc5362c93138ef301ac65ace799ad64d59ac9110af349822e0efa98d410686e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605017"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>\_ \_ MF-QUELLLESER: \_ ENABLE \_ TRANSCODE ONLY \_ \_ TRANSFORMS-Attribut

Ermöglicht dem [Quellleser](source-reader.md) die Verwendung Media Foundation Transformationen (MFTs), die für die Transcodierung optimiert sind.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Einige MFTs, insbesondere Decoder, sind für die Transcodierung und nicht für die Wiedergabe optimiert. Standardmäßig werden solche Transformationen vom Quellleser nicht geladen. Legen Sie dieses Attribut auf **TRUE** fest, wenn Sie MFTs mit dem Quellleser transcodieren möchten.

Eine Anwendung kann dieses Attribut festlegen, wenn sie die Daten nicht in Echtzeit (für Transcodierung oder ähnliche Szenarien) verarbeiten kann. Verwenden Sie andernfalls für die Echtzeitwiedergabe das Standardverhalten.

Intern bewirkt dieses Attribut, dass der Quellleser das **Flag MFT \_ ENUM \_ FLAG \_ TRANSCODE \_ ONLY** enthält, wenn [**es MFTEnumEx aufruft.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quellleser](source-reader.md)
</dt> </dl>

 

 




