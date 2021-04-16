---
description: Gibt an, ob der Aufrufer die für die Ausgabe verwendeten Texturen zuweist.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: MF_XVP_CALLER_ALLOCATES_OUTPUT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527395"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>MF \_ xvp \_ Caller \_ weist das \_ Ausgabe Attribut zu

Gibt an, ob der Aufrufer die für die Ausgabe verwendeten Texturen zuweist.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut den Wert **true** hat, erwartet der Videoprozessor, dass Ausgabe Texturen vom Aufrufer zugeordnet werden, auch wenn er im DXVA-Modus (DirectX Video Acceleration) ausgeführt wird. Wenn dieses Attribut den Wert **false** hat, weist der Videoprozessor die Ausgabe Texturen beim Betrieb im DXVA-Modus zu und schlägt fehl, wenn vom Aufrufer bereitgestellte Ausgabe Texturen bereitgestellt werden.

So legen Sie dieses Attribut fest:

1.  Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Videoprozessor.
2.  Rückrufe [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Legen Sie das-Attribut vor Beginn des Streamings fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>MFI. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




