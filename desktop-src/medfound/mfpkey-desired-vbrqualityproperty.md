---
description: Gibt die gewünschte Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (VBR) von Audiostreams an.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349152"
---
# <a name="mfpkey_desired_vbrquality-property"></a>Mfpkey \_ gewünschte \_ vbrquality-Eigenschaft

Gibt die gewünschte Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (VBR) von Audiostreams an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Dieser Wert kann zwischen 0 und 100 liegen, wobei 100 eine maximale Qualität ist. Der Wert 0 gibt an, dass die Qualitäts basierte VBR-Codierungsmethode nicht verwendet werden soll.

Legen Sie die folgenden Codierungs Eigenschaften fest, um VBR-Modi aufzulisten, die eine bestimmte Qualitätsanforderung erfüllen.

-   Legen Sie [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) auf **Variant \_ true** fest.
-   Legen Sie [**mfpkey- \_ \_ Enumeration \_ vbrquality**](mfpkey-constrain-enumerated-vbrqualityproperty.md) auf **Variant \_ true** fest.
-   Legen Sie für **mfpkey die \_ gewünschte \_ vbrquality** auf die gewünschte Qualität fest. Legen Sie für den Modus ohne Verlust die gewünschte Qualität auf 100 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
