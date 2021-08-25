---
description: Gibt LTR-Frameinformationen (Long Term Reference) an und wird im Ausgabebeispiel zurückgegeben.
ms.assetid: 0632D780-C56B-4FDB-8A76-B7A7DE414242
title: MFSampleExtension_LongTermReferenceFrameInfo-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642c246adf0e5e1c10249085201fba3dc430b6547516b79fe4929e9de4b998a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848120"
---
# <a name="mfsampleextension_longtermreferenceframeinfo-attribute"></a>MFSampleExtension \_ LongTermReferenceFrameInfo-Attribut

Gibt LTR-Frameinformationen (Long Term Reference) an und wird im Ausgabebeispiel zurückgegeben.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

**H.264/AVC-Encoder:**

Encoder müssen dieses Attribut im Ausgabebeispiel zurückgeben, wenn die Anwendung LTR-Frames steuert, die von [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)angegeben werden.

MFSampleExtension \_ LongTermReferenceFrameInfo gibt bis zu zwei Felder zurück.

Das erste Feld, bits \[ 0..15, \] ist *LongTermFrameIdx,* das dem Ausgabeframe zugeordnet ist, wenn es als LTR-Frame markiert ist. Der erste Wert ist 0xffff, wenn es sich bei diesem Ausgabeframe um einen kurzzeitigen Verweisrahmen oder einen Nicht-Verweisrahmen handelt.

Das zweite Feld, bits \[ 16..31, ist eine Bitmap, die \] aus *MaxNumLTRFrames* viele Bits besteht, die angeben, welche LTR-Frame(s) ab Bit 16 zum Codieren dieses Ausgabeframes verwendet wurden. Die restlichen Bits müssen auf 0 festgelegt werden. Der zweite Wert ist 0, wenn dieser Ausgaberahmen nicht mit LTR-Frames codiert ist. *MaxNumLTRFrames* ist die maximale Anzahl von LTR-Frames, die über [CODECAPI \_ AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




