---
description: Gibt an, ob der sprach Erfassungs-DSP den Quell Modus oder Filter Modus verwendet.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215050"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>Eigenschaft "mfpkey \_ wmaaecma \_ DMO \_ Source \_ Mode"

Gibt an, ob der sprach Erfassungs-DSP den Quell Modus oder Filter Modus verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ true

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Im Quell Modus muss die Anwendung keine Eingabedaten an den DSP senden, da der DSP automatisch Daten von den Audiogeräten abruft. Im Filter Modus muss die Anwendung die Eingabedaten an den DSP senden.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG  |
|----------------|--------------|
| Variant \_ false | Filter Modus. |
| Variant \_ true  | Der Quell Modus. |



 

> [!Note]  
> Wenn sich der DMO im Quell Modus befindet, sollten Sie nur [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) aufrufen, um das Ausgabedatenstrom Format festzulegen, und [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) nicht aufrufen, um Eingabedaten Strom Formate festzulegen. Andernfalls schlägt die DMO-Initialisierung fehl.

 

Wenn der Wert dieser Eigenschaft Variant true ist \_ , weist der DSP keine Eingaben auf. Wenn der Wert Variant \_ false ist, verfügt der DSP abhängig vom Wert der Eigenschaft [mfpkey \_ wmaaecma \_ System \_ Mode](mfpkey-wmaaecma-system-modeproperty.md) , wie in der folgenden Tabelle gezeigt, über eine oder zwei Eingaben.



| Wert                     | Anzahl von Eingaben |
|---------------------------|------------------|
| Optibeam \_ \_ -Array und \_ AEC | 2                |
| nur Optibeam- \_ array \_     | 1                |
| einzelner \_ Channel- \_ AEC      | 2                |
| \_ \_ nsagc eines einzelnen Kanals    | 1                |



 

> [!Note]  
> Nur Modi mit einer einzelnen Eingabe können mit dem Wrapper Filter DMO aus der DirectShow 9,0-API verwendet werden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
