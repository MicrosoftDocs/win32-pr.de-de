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
ms.openlocfilehash: 85e31a8efb1e39d47ab3959fc5ecc175336ab7b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039248"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>ID2D1SvgElement:: GetAttributeValue-Methoden

Ruft ein Attribut dieses Elements ab.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                     | BESCHREIBUNG                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue (pcwstr, float \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | Ruft ein Attribut dieses Elements als float ab.<br/>                                                                                                    |
| [**GetAttributeValue (pcwstr, D2D1 \_ Color \_ F \* )**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | Ruft ein Attribut dieses Elements als Farbe ab.<br/>                                                                                                    |
| [**GetAttributeValue (pcwstr, refid, void \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | Ruft ein Attribut dieses Elements als Schnittstellentyp ab. <br/>                                                                                         |
| [**GetAttributeValue (pcwstr, D2D1 \_ Fill \_ Mode \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | Ruft ein Attribut dieses Elements als Füll Modus ab. Diese Methode kann verwendet werden, um den Wert der Eigenschaften Füll Regel oder Clip Regel zu erhalten.<br/>             |
| [**GetAttributeValue (pcwstr, ID2D1SvgPaint \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | Ruft ein Attribut dieses Elements als Paint ab. Diese Methode kann verwendet werden, um den Wert der Füll-oder Strich Eigenschaften zu erhalten.<br/>                         |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ length \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | Ruft ein Attribut dieses Elements als Längen Wert ab.<br/>                                                                                             |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ Display \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | Ruft ein Attribut dieses Elements als Anzeige Wert ab. Diese Methode kann verwendet werden, um den Wert der Anzeige Eigenschaft zu erhalten.<br/>                          |
| [**GetAttributeValue (pcwstr, D2D1 \_ Extended \_ Mode \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | Ruft ein Attribut dieses Elements als erweiterungsmoduswert ab. Diese Methode kann verwendet werden, um den Wert eines SpreadMethod-Attributs zu erhalten.<br/>                  |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ Overflow \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | Ruft ein Attribut dieses Elements als Überlauf Wert ab. Diese Methode kann verwendet werden, um den Wert der Overflow-Eigenschaft zu erhalten.<br/>                       |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ line \_ Cap \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | Ruft ein Attribut dieses Elements als Zeilen deckwert ab. Diese Methode kann verwendet werden, um den Wert der Stroke-LineCap-Eigenschaft zu erhalten.<br/>                  |
| [**GetAttributeValue (pcwstr, D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | Ruft ein Attribut dieses Elements als Matrix Wert ab. Diese Methode kann verwendet werden, um den Wert eines Transform-oder gradienttransform-Attributs zu erhalten.<br/>     |
| [**GetAttributeValue (pcwstr, ID2D1SvgPathData \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | Ruft ein Attribut dieses Elements als Pfaddaten ab. Diese Methode kann verwendet werden, um den Wert des Attributs d für ein Path-Element zu erhalten.<br/>                   |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ line \_ Join \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | Ruft ein Attribut dieses Elements als Zeilen Verknüpfungs Wert ab. Diese Methode kann verwendet werden, um den Wert der Stroke-LineJoin-Eigenschaft zu erhalten.<br/>                |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ Unit \_ Type \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | Ruft ein Attribut dieses Elements als Einheitentyp Wert ab. Diese Methode kann verwendet werden, um den Wert eines gradientunits-oder clippathunits-Attributs zu erhalten.<br/>  |
| [**GetAttributeValue (pcwstr, ID2D1SvgAttribute \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | Ruft ein Attribut dieses Elements ab.<br/>                                                                                                               |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ Visibility \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | Ruft ein Attribut dieses Elements als Sichtbarkeits Wert ab. Diese Methode kann verwendet werden, um den Wert der Visibility-Eigenschaft zu erhalten.<br/>                    |
| [**GetAttributeValue (pcwstr, ID2D1SvgStrokeDashArray \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | Ruft ein Attribut dieses Elements als Strich Strich-Array ab. Diese Methode kann verwendet werden, um den Wert der Stroke-dasharray-Eigenschaft zu erhalten.<br/>             |
| [**GetAttributeValue (pcwstr, ID2D1SvgPointCollection \* \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | Ruft ein Attribut dieses Elements als Punkte ab. Diese Methode kann verwendet werden, um den Wert des Points-Attributs in einem Polygon-oder polylinienelement zu erhalten.<br/>  |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ Preserve \_ Aspect \_ Ratio \* )**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | Ruft ein Attribut dieses Elements als Wert für das Seitenverhältnis beibehalten ab. Diese Methode kann verwendet werden, um den Wert eines preserveaspectratio-Attributs zu erhalten.<br/> |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG \_ Attribute \_ Pod \_ Type, void \* , UInt32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | Ruft ein Attribut dieses Elements als POD-Typ ab.<br/>                                                                                                 |
| [**GetAttributeValue (pcwstr, D2D1 \_ SVG- \_ Attribut \_ Zeichenfolgentyp \_ , pwstr, UInt32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | Ruft ein Attribut dieses Elements als Zeichenfolge ab. <br/>                                                                                                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

