---
description: Gibt den postverarbeitungs Modus für den Decoder an.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361046"
---
# <a name="mfpkey_postprocessmode-property"></a>Mfpkey- \_ postprocessmode-Eigenschaft

Gibt den postverarbeitungs Modus für den Decoder an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

**g \_ wszwmvcforcepostprocessmode**

## <a name="data-type"></a>Datentyp

**VT \_ I4**

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft auf einen der folgenden Werte fest.



| Wert | Bedeutung                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | Der Decoder legt den postverarbeitungs Modus basierend auf verfügbaren CPU-Ressourcen adaptiv fest. |
| 0     | Der Decoder führt keine nach Verarbeitung aus.                                               |
| 1     | der-Decoder führt eine schnelle Blockierung aus.                                                 |
| 2     | Der Decoder führt vollständige Blockierung aus.                                                  |
| 3     | Der Decoder führt eine schnelle Blockierung und einen deringing aus.                                    |
| 4     | Der Decoder führt vollständige Blockierung und Aufhebung aus.                                    |



 

Da der Wert dieser Eigenschaft zwischen 0 und 4 liegt, erhöht sich die Decodierungs Komplexität, die Verwendung von CPU-Ressourcen und die Bildqualität.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




