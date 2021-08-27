---
title: ID2D1SvgElement GetAttributeValue-Methoden
description: Ruft ein Attribut dieses Elements ab.
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- GetAttributeValue-Methoden Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cfc85f2af132c52a95f196aa6e0722b4d75ccc9bc8a4b7a1abb992cc581a6f32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076850"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>ID2D1SvgElement::GetAttributeValue-Methoden

Ruft ein Attribut dieses Elements ab.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                     | BESCHREIBUNG                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue(PCWSTR, FLOAT \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Ruft ein Attribut dieses Elements als float ab.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, D2D1 \_ COLOR \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Ruft ein Attribut dieses Elements als Farbe ab.<br/>                                                                                                    |
| [**GetAttributeValue(PCWSTR, REFIID, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Ruft ein Attribut dieses Elements als Schnittstellentyp ab. <br/>                                                                                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ FILL \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Ruft ein Attribut dieses Elements als Füllmodus ab. Diese Methode kann verwendet werden, um den Wert der Füllregel- oder Clipregeleigenschaften abzurufen.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Ruft ein Attribut dieses Elements als Farbe ab. Diese Methode kann verwendet werden, um den Wert der Füll- oder Stricheigenschaften abzurufen.<br/>                         |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LENGTH \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Ruft ein Attribut dieses Elements als Längenwert ab.<br/>                                                                                             |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ DISPLAY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Ruft ein Attribut dieses Elements als Anzeigewert ab. Diese Methode kann verwendet werden, um den Wert der Anzeigeeigenschaft abzurufen.<br/>                          |
| [**GetAttributeValue(PCWSTR, D2D1 \_ EXTEND \_ MODE \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Ruft ein Attribut dieses Elements als Wert für den Erweiterungsmodus ab. Diese Methode kann verwendet werden, um den Wert eines spreadMethod-Attributs abzurufen.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ OVERFLOW \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Ruft ein Attribut dieses Elements als Überlaufwert ab. Diese Methode kann verwendet werden, um den Wert der Überlaufeigenschaft abzurufen.<br/>                       |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE CAP \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Ruft ein Attribut dieses Elements als Zeilenbegrenzungswert ab. Diese Methode kann verwendet werden, um den Wert der Stroke-Linecap-Eigenschaft abzurufen.<br/>                  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Ruft ein Attribut dieses Elements als Matrixwert ab. Diese Methode kann verwendet werden, um den Wert eines Transformations- oder gradientTransform-Attributs abzurufen.<br/>     |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Ruft ein Attribut dieses Elements als Pfaddaten ab. Diese Methode kann verwendet werden, um den Wert des d-Attributs für ein Pfadelement abzurufen.<br/>                   |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ LINE JOIN \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Ruft ein Attribut dieses Elements als Zeilenbeitrittswert ab. Diese Methode kann verwendet werden, um den Wert der stroke-linejoin-Eigenschaft abzurufen.<br/>                |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ UNIT TYPE \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Ruft ein Attribut dieses Elements als Einheitentypwert ab. Diese Methode kann verwendet werden, um den Wert eines gradientUnits- oder clipPathUnits-Attributs abzurufen.<br/>  |
| [**GetAttributeValue(PCWSTR, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Ruft ein Attribut dieses Elements ab.<br/>                                                                                                               |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ VISIBILITY \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Ruft ein Attribut dieses Elements als Sichtbarkeitswert ab. Diese Methode kann verwendet werden, um den Wert der Visibility-Eigenschaft abzurufen.<br/>                    |
| [**GetAttributeValue(PCWSTR, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Ruft ein Attribut dieses Elements als Strichstricharray ab. Diese Methode kann verwendet werden, um den Wert der Stroke-Dasharray-Eigenschaft abzurufen.<br/>             |
| [**GetAttributeValue(PCWSTR, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Ruft ein Attribut dieses Elements als Punkte ab. Diese Methode kann verwendet werden, um den Wert des Points-Attributs für ein Polygon- oder Polylinienelement abzurufen.<br/>  |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ PRESERVE ASPECT RATIO \_ \_ \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Ruft ein Attribut dieses Elements als Wert für das Beibehalten des Seitenverhältnisses ab. Diese Methode kann verwendet werden, um den Wert eines preserveAspectRatio-Attributs abzurufen.<br/> |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE, void \* , UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Ruft ein Attribut dieses Elements als POD-Typ ab.<br/>                                                                                                 |
| [**GetAttributeValue(PCWSTR, D2D1 \_ SVG \_ ATTRIBUTE \_ STRING \_ TYPE, PWSTR, UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Ruft ein Attribut dieses Elements als Zeichenfolge ab. <br/>                                                                                                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

