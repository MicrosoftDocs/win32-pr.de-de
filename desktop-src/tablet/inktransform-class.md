---
description: Stellt eine 3X3-Matrix dar, die wiederum eine affine-Transformation darstellt.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Inktransform-Klasse (msink AUT. h)
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
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366228"
---
# <a name="inktransform-class"></a>Inktransform-Klasse

Stellt eine 3X3-Matrix dar, die wiederum eine affine-Transformation darstellt.

**Inktransform** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **inktransform** -Klasse verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Ruft **inktransform** als 6-Gleit Komma Zahlen ab.<br/>                                                                      |
| [**Widerzuspiegeln**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Reflektiert die Transformation in horizontaler oder vertikaler Richtung.<br/>                                          |
| [**Zurücksetzen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Setzt die Transformation auf ihren ursprünglichen Zustand zurück.<br/>                                                                      |
| [**Drehen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Dreht die Transformation um einen Winkel in Grad und gibt optional einen Mittelpunkt für die Drehung an.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Skaliert die Transformation um X-und Y-Faktoren.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Ändert die **inktransform** mit 6 Gleit Komma Zahlen.<br/>                                                                    |
| [**Scherz**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Wendet eine Schere mit den angegebenen horizontalen und vertikalen Faktoren an.<br/>                                              |
| [**Übersetzen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Verschiebt die Transformation um die angegebenen horizontalen und vertikalen Komponenten.<br/>                                         |



 

### <a name="properties"></a>Eigenschaften

Die **inktransform** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                     | Zugriffstyp           | BESCHREIBUNG                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Daten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Lesen/Schreiben<br/> | Ruft die Automatisierungs Version der Win32 XForm-Struktur ab oder legt Sie fest.<br/>                            |
| [**eDx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Lesen/Schreiben<br/> | Ruft die reelle Zahl ab, die das Element in der dritten Zeile (erste Spalte) angibt, oder legt diese fest.<br/>   |
| [**Edy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Lesen/Schreiben<br/> | Ruft die reelle Zahl ab, die das Element in der dritten Zeile, zweiten Spalte angibt, oder legt diese fest.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Lesen/Schreiben<br/> | Ruft die reelle Zahl ab, die das Element in der ersten Zeile (erste Spalte) angibt, oder legt diese fest.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Lesen/Schreiben<br/> | Ruft die reelle Zahl ab, die das Element in der ersten Zeile, zweiten Spalte angibt, oder legt diese fest.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Lesen/Schreiben<br/> | Ruft die reelle Zahl ab, die das Element in der zweiten Zeile (erste Spalte) angibt, oder legt diese fest.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Lesen/Schreiben<br/> | Ruft die reelle Zahl ab, die das Element in der zweiten Zeile, zweiten Spalte angibt, oder legt diese fest.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Das-Objekt speichert nur sechs der neun Zahlen in einer 3X3-Matrix, da alle 3X3-Matrizen, die affine Transformationen darstellen, dieselbe dritte Spalte (0, 0, 1) enthalten. Dieses Objekt wird wiederum verwendet, um Transformations Vorgänge zu beschreiben, z. b. das Verschieben, das Scheren, das Skalieren oder das Drehen in einem [**inkrenderer**](inkrenderer-class.md) -Objekt, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt oder [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung.

> [!Note]  
> Das **inktransform** -Objekt korreliert mit der [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

