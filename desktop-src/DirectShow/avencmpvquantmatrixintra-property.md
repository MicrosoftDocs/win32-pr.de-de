---
description: Gibt die Luma-Quantisierungsmatrix für makroblockinterne Blöcke an. Diese Eigenschaft gilt für MPEG-Videoencoder.
ms.assetid: 65e6e276-1da7-47ee-b337-0ff64a9c4cff
title: AVEncMPVQuantMatrixIntra-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac326bc284603c8f841704f7aa496db9d2795e7ff1a1c3a9f60a218a854a999e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794630"
---
# <a name="avencmpvquantmatrixintra-property"></a>AVEncMPVQuantMatrixIntra-Eigenschaft

Gibt die Luma-Quantisierungsmatrix für makroblockinterne Blöcke an. Diese Eigenschaft gilt für MPEG-Videoencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPVQuantMatrixIntra**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist eine Zeichenfolge, die die 64 8-Bit-Koeffizienten enthält, die als Zeichenfolge mit Hexadezimalwerten (128 Zeichen) codiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




