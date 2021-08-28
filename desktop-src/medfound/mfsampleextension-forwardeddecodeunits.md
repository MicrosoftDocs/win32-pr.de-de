---
description: Ruft ein Objekt vom Typ "ABSTRACTIONCollection" ab, das DIESAMPLE-Objekte enthält, die NALUs (Network Abstraction Layer Units) und SEI-Einheiten (Supplemental Enhancement Information) enthalten, die von einem Decoder weitergeleitet werden.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: MFSampleExtension_ForwardedDecodeUnits -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2298a29d722c118fb79d5f0b49aa9d3d94fd735150a65772eb15e6da7638445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713730"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>MFSampleExtension \_ ForwardedDecodeUnits-Attribut

Ruft ein Objekt vom Typ [**"ABSTRACTIONCollection"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) ab, das [**DIESAMPLE-Objekte**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) enthält, die NALUs (Network Abstraction Layer Units) und SEI-Einheiten (Supplemental Enhancement Information) enthalten, die von einem Decoder weitergeleitet werden.

## <a name="data-type"></a>Datentyp

**IUnknown**

## <a name="remarks"></a>Hinweise

Die Auflistung enthält alle benutzerdefinierten NULATION/SEI-Einheiten seit dem vorherigen Frame mit entfernten Bytes zur Emulationsschutz.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




