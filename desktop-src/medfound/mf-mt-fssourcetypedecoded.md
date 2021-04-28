---
description: 'MF_MT_FSSourceTypeDecoded Attribut: Gibt an, ob ein Decoder Beim Festlegen von Zeitstempeln Decodierungszeitstempel (DTS) verwenden kann.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093088"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a>MF \_ MT \_ FSSourceTypeDecoded-Attribut

Gibt an, dass ein Medientyp automatisch decodiert wird.

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**


## <a name="remarks"></a>Bemerkungen
Ein Medientyp wird als Attribut markiert, um anzugeben, dass dies in der physischen Quelle nicht vorhanden ist und von der Pipeline synthetisiert wird. Der Wert 1 (TRUE) gibt an, dass der Medientyp synthetisiert wird. Der Wert 0 (FALSE) oder der wert, der nicht vorhanden ist, gibt an, dass dies nicht der Fall ist.

In der aktuellen Version sollte dieses Attribut mithilfe des folgenden GUID-Werts anstelle der MD_MT_FSSourceTypeDecoded angegeben werden:

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | UWP-Apps für Windows Server \[ 2012-Desktop-Apps \|\]<br/>                        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




