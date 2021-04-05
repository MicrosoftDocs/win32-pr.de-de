---
description: Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755496"
---
# <a name="mfpkey_colorconv_mode-property"></a>Mfpkey \_ Color-v- \_ Modus (Eigenschaft)

Gibt an, ob der Eingabedaten Strom mit Zeilen Sprung verknüpft ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Wird vom DSP aus dem Quellvideo berechnet.

## <a name="applies-to"></a>Gilt für

-   [Farb Konverter-DSP](colorconverter.md)

## <a name="remarks"></a>Bemerkungen

Verwenden Sie einen der folgenden Werte.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 0     | progressiv |
| 2     | Interlaced  |



 

Wenn diese Eigenschaft nicht festgelegt ist, verwendet der DSP den Eingabe Medientyp, um zu bestimmen, ob das Video mit Zeilen Sprung verknüpft ist. Sie können diese Eigenschaft festlegen, um die Medientyp Einstellung außer Kraft zu setzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
