---
description: Gibt die Codierungsqualität für die DLNA-Mediensenke (Digital Living Network Alliance) an.
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: MF_MP2DLNA_ENCODE_QUALITY -Attribut (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a612dae32aabe4276ece76e7edff1aef431cc5d93f8aeaae0dbc9087620374c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973659"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a>MF \_ MP2DLNA \_ ENCODE \_ QUALITY-Attribut

Gibt die Codierungsqualität für die DLNA-Mediensenke (Digital Living Network Alliance) an.

## <a name="data-type"></a>Datentyp

**UINT32**

Bereich: 0–18

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Höhere Zahlen weisen auf eine bessere Codierungsqualität hin. Niedrigere Zahlen weisen auf eine schnellere Codierung, aber eine niedrigere Codierungsqualität hin. Der Standardwert ist 9.

Um dieses Attribut für die DLNA-Mediensenke festlegen zu können, fragen Sie die Mediensenke für die [**BENUTZEROBERFLÄCHEAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ab. Legen Sie das Attribut fest, bevor das Streaming beginnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




