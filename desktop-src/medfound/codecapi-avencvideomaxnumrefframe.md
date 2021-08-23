---
description: Gibt die maximale Anzahl von Referenzframes an, die vom Encoder unterstützt werden.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame -Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e11e7325628f0e7c1e6560d3fc734b34e8a032a3fbf3630aa1fb5959cec33a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606420"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>CODECAPI \_ AVEncVideoMaxNumRefFrame (Eigenschaft)

Gibt die maximale Anzahl von Referenzframes an, die vom Encoder unterstützt werden.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Hinweise

Für H.264 wird dies der Sequence Parameter Set-Variablen **max \_ num ref \_ \_ frames** gemäß definition in H.264 specification (H.264-Spezifikation) zugewiesen.

**H.264/AVC-Encoder:**

Encoder verwenden möglicherweise weniger Referenzframes, um der im Bitstream angegebenen Ebene zu folgen.

Encoder müssen [**GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)und [**GetParameterRangee unterstützen.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Dies ist eine statische Eigenschaft, die bedeutet, dass sie nur vor beginn der Codierungssitzung festgelegt werden kann.

Der empfohlene Standardwert ist 2.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

