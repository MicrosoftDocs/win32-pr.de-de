---
description: Beendet den aktuellen Codierungs Durchlauf oder fragt ab, ob der aktuelle Codierungs Durchlauf der letzte ist.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Avenccommonpassend-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482515"
---
# <a name="avenccommonpassend-property"></a>Avenccommonpassend (Eigenschaft)

Beendet den aktuellen Codierungs Durchlauf oder fragt ab, ob der aktuelle Codierungs Durchlauf der letzte ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonpassend**

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft auf **Variant \_ true** festgelegt wird, wird der aktuelle Codierungs Durchlauf beendet. Wenn Sie diese Eigenschaft auf **Variant \_ false** festlegen, wird die Multipass-Codierung beendet

Beim Lesen dieser Eigenschaft wird abgefragt, ob der aktuelle Codierungs Durchlauf der letzte ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




