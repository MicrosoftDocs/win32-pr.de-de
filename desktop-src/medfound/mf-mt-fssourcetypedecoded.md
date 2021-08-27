---
description: 'MF_MT_FSSourceTypeDecoded-Attribut: Gibt an, ob ein Decoder beim Festlegen von Zeitstempeln ZEITStempel (DTS) decodieren kann.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae25fce343d0c24f7b0a79e2623e7c3e2d0f9272b2f95a825860860ff6f88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113760"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>MF \_ MT \_ FSSourceTypeDecoded-Attribut

Gibt an, dass ein Medientyp automatisch decodiert wird.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert


## <a name="remarks"></a>Hinweise
Ein Medientyp wird als Attribut markiert, um anzugeben, dass dies in der physischen Quelle nicht vorhanden ist und von der Pipeline synthetisiert wird. Der Wert 1 (TRUE) gibt an, dass der Medientyp synthetisiert wird. Der Wert 0 (FALSE) oder der Wert, der nicht vorhanden ist, gibt an, dass er nicht vorhanden ist.

In der aktuellen Version sollte dieses Attribut mit dem folgenden GUID-Wert anstelle der MD_MT_FSSourceTypeDecoded Konstante angegeben werden:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




