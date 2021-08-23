---
description: Gibt an, ob der Aufrufer die für die Ausgabe verwendeten Texturen zuordnet.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: MF_XVP_CALLER_ALLOCATES_OUTPUT-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31da89bec9c9573d9d968077e51d413e1861bca28cb606667d402fab5a408f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599970"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>MF \_ XVP \_ CALLER \_ ALLOCATES \_ OUTPUT-Attribut

Gibt an, ob der Aufrufer die für die Ausgabe verwendeten Texturen zuordnet.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut **TRUE** ist, erwartet der Videoprozessor, dass Ausgabetexturen vom Aufrufer zugeordnet werden, auch wenn der DirectX-Videobeschleunigungsmodus (DXVA) ausgeführt wird. Wenn dieses Attribut **FALSE** ist, ordnet der Videoprozessor die Ausgabetexturen zu, wenn er im DXVA-Modus arbeitet, und schlägt fehl, wenn vom Aufrufer bereitgestellte Ausgabetexturen bereitgestellt werden.

So legen Sie dieses Attribut fest:

1.  Rufen Sie [**ÜBERTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Videoprozessor auf.
2.  Rufen Sie [**DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Legen Sie das Attribut fest, bevor das Streaming beginnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




