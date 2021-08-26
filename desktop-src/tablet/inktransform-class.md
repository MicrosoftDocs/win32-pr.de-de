---
description: Stellt eine 3x3-Matrix dar, die wiederum eine affine Transformation darstellt.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: InkTransform-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 4bdc93e2c80f1a7ef4a8eacf1a58288c008e1354cda702e492deb2990e8938d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938660"
---
# <a name="inktransform-class"></a>InkTransform-Klasse

Stellt eine 3x3-Matrix dar, die wiederum eine affine Transformation darstellt.

**InkTransform verfügt** über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **InkTransform-Klasse** verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Ruft **InkTransform als** 6 Gleitkommadaten ab.<br/>                                                                      |
| [**Spiegeln**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Spiegelt die Transformation entweder in horizontaler oder vertikaler Richtung wider.<br/>                                          |
| [**Zurücksetzen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Setzt die Transformation auf ihren ursprünglichen Zustand zurück.<br/>                                                                      |
| [**Drehen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Dreht die Transformation um einen in Grad gemessenen Winkel und gibt optional einen Mittelpunkt für die Drehung an.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Skaliert die Transformation um X- und Y-Faktoren.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Ändert die **InkTransform mithilfe** von 6 Gleitkommaen.<br/>                                                                    |
| [**Scheren**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Wendet einen Shear mit den angegebenen horizontalen und vertikalen Faktoren an.<br/>                                              |
| [**Übersetzen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Verschiebt die Transformation um die angegebenen horizontalen und vertikalen Komponenten.<br/>                                         |



 

### <a name="properties"></a>Eigenschaften

Die **InkTransform-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                     | Zugriffstyp           | BESCHREIBUNG                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Daten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Lesen/Schreiben<br/> | Ruft die Automation-Version der WIN32 XFORM-Struktur ab oder legt diese fest.<br/>                            |
| [**Edx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Lesen/Schreiben<br/> | Ruft die tatsächliche Zahl ab, die das Element in der dritten Zeile, der ersten Spalte, angibt, oder legt diese fest.<br/>   |
| [**Edy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Lesen/Schreiben<br/> | Ruft die tatsächliche Zahl ab, die das Element in der dritten Zeile der zweiten Spalte angibt, oder legt diese fest.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Lesen/Schreiben<br/> | Ruft die tatsächliche Zahl ab, die das Element in der ersten Zeile, der ersten Spalte angibt, oder legt diese fest.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Lesen/Schreiben<br/> | Ruft die tatsächliche Zahl ab, die das Element in der ersten Zeile, zweiten Spalte angibt, oder legt diese fest.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Lesen/Schreiben<br/> | Ruft die tatsächliche Zahl ab, die das Element in der zweiten Zeile, der ersten Spalte, angibt, oder legt diese fest.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Lesen/Schreiben<br/> | Ruft die tatsächliche Zahl ab, die das Element in der zweiten Zeile der zweiten Spalte angibt, oder legt diese fest.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

Das -Objekt speichert nur sechs der neun Zahlen in einer 3x3-Matrix, da alle 3x3-Matrizen, die affine Transformationen darstellen, dieselbe dritte Spalte (0, 0, 1) haben. Dieses Objekt wird wiederum verwendet, um Transformationsvorgänge wie Das Verschieben, Skalieren, Skalieren oder Drehen in einem [**InkRenderer-Objekt,**](inkrenderer-class.md) [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) oder [einer InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) zu beschreiben.

> [!Note]  
> Das **InkTransform-Objekt** korreliert mit der [**XFORM-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-xform)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

