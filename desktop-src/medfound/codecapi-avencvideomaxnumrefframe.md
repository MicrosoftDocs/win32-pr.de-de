---
description: Gibt die maximalen vom Encoder unterstützten Verweis Rahmen an.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132161"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>Codecapi \_ avencvideomaxnumrefframe (Eigenschaft)

Gibt die maximalen vom Encoder unterstützten Verweis Rahmen an.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideomaxnumrefframe**

## <a name="remarks"></a>Bemerkungen

Bei H. 264 wird dies dem Sequenz Parameter Set Variable **Max \_ NUM \_ ref \_ Frames** entsprechend der Angabe in der H. 264-Spezifikation zugeordnet.

**H. 264/AVC-Encoder:**

Encoder können weniger Verweis Frames verwenden, um die im Bitstream angegebene Ebene einzuhalten.

Encoder müssen " [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützen.

Dies ist eine statische Eigenschaft, die bedeutet, dass Sie nur festgelegt werden kann, bevor die Codierungs Sitzung gestartet wird.

Der empfohlene Standardwert ist 2.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

