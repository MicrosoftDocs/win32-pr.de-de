---
title: ID2D1SvgElement SetAttributeValue-Methoden (D2d1svg.h)
description: Legt ein Attribut dieses Elements fest.
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
keywords:
- SetAttributeValue-Methoden Direct2D
topic_type:
- apiref
api_location:
- d2d1svg.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 95ac3021abdf641b268e2278e92dfd86227244cde1d1d51f992953e68584fa69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527140"
---
# <a name="id2d1svgelementsetattributevalue-methods"></a>ID2D1SvgElement::SetAttributeValue-Methoden

Legt ein Attribut dieses Elements fest.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                      | Beschreibung                                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAttributeValue(PCWSTR, FLOAT)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_float))                                             | Legt ein Attribut dieses Elements mithilfe eines float-Elements fest.<br/>                                                                                                 |
| [**SetAttributeValue(PCWSTR, D2D1 \_ COLOR \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_color_f_))                                  | Legt ein Attribut dieses Elements als Farbe fest.<br/>                                                                                                    |
| [**SetAttributeValue(PCWSTR, D2D1 \_ FILL \_ MODE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_fill_mode))                                  | Legt ein Attribut dieses Elements als Füllmodus fest. Mit dieser Methode kann der Wert der Eigenschaften "fill-rule" oder "clip-rule" festgelegt werden.<br/>         |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ DISPLAY)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_display))                                | Ruft ein Attribut dieses Elements als Anzeigewert ab. Diese Methode kann verwendet werden, um den Wert der Display-Eigenschaft zu erhalten.<br/>                          |
| [**SetAttributeValue(PCWSTR, D2D1 \_ EXTEND \_ MODE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_extend_mode))                               | Legt ein Attribut dieses Elements als Wert für den Erweiterungsmodus fest. Mit dieser Methode kann der Wert eines spreadMethod-Attributs festgelegt werden.<br/>                 |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ OVERFLOW)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_overflow))                               | Legt ein Attribut dieses Elements als Überlaufwert fest. Mit dieser Methode kann der Wert der Overflow-Eigenschaft festgelegt werden.<br/>                       |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ CAP)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_cap))                             | Legt ein Attribut dieses Elements als Zeilenoberwert fest. Mit dieser Methode kann der Wert der Stroke-Linecap-Eigenschaft festgelegt werden.<br/>                  |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LENGTH &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_length_))                              | Legt ein Attribut dieses Elements als Längenwert fest.<br/>                                                                                             |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE \_ JOIN)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_join))                             | Legt ein Attribut dieses Elements als Zeilenumknungswert fest. Mit dieser Methode kann der Wert der Strichlinienjoin-Eigenschaft festgelegt werden.<br/>                |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ UNIT \_ TYPE)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_unit_type))                            | Legt ein Attribut dieses Elements als Einheitentypwert fest. Mit dieser Methode kann der Wert eines gradientUnits- oder clipPathUnits-Attributs festgelegt werden.<br/>  |
| [**SetAttributeValue(PCWSTR, ID2D1SvgAttribute \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_id2d1svgattribute))                              | Legt ein Attribut dieses Elements mithilfe einer Schnittstelle fest.<br/>                                                                                            |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ VISIBILITY)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_visibility))                            | Legt ein Attribut dieses Elements als Sichtbarkeitswert fest. Mit dieser Methode kann der Wert der Sichtbarkeitseigenschaft festgelegt werden.<br/>                    |
| [**SetAttributeValue(PCWSTR, D2D1 \_ MATRIX \_ 3X2 \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_matrix_3x2_f_))                           | Legt ein Attribut dieses Elements als Matrixwert fest. Mit dieser Methode kann der Wert eines transform- oder gradientTransform-Attributs festgelegt werden.<br/>     |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ PRESERVE ASPECT \_ RATIO \_ &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_preserve_aspect_ratio_))             | Legt ein Attribut dieses Elements als Wert für das beibehaltene Seitenverhältnis fest. Mit dieser Methode kann der Wert eines preserveAspectRatio-Attributs festgelegt werden.<br/> |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ STRING \_ TYPE, PCWSTR)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_string_type_pcwstr))          | Legt ein Attribut dieses Elements mithilfe einer Zeichenfolge fest. <br/>                                                                                               |
| [**SetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE , void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_pod_type_constvoid_uint32)) | Legt ein Attribut dieses Elements mithilfe eines POD-Typs fest.<br/>                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D2d1svg.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

�

�
