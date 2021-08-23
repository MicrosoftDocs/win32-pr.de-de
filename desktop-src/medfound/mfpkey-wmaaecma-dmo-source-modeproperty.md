---
description: Gibt an, ob der Spracherfassungs-DSP den Quell- oder Filtermodus verwendet.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec9dd01be5a020047410362b2fdfc27fd8d703a393e3ae2f557b1dd3a42bf80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555300"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE-Eigenschaft

Gibt an, ob der Spracherfassungs-DSP den Quell- oder Filtermodus verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

VARIANT \_ TRUE

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Im Quellmodus muss die Anwendung keine Eingabedaten an den DSP senden, da der DSP Daten automatisch von den Audiogeräten abruft. Im Filtermodus muss die Anwendung die Eingabedaten an den DSP senden.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | Beschreibung  |
|----------------|--------------|
| VARIANT \_ FALSE | Filtermodus. |
| VARIANT \_ TRUE  | Quellmodus. |



 

> [!Note]  
> Wenn sich die DMO im Quellmodus befindet, sollten Sie nur [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) aufrufen, um das Ausgabestreamformat festzulegen, und nicht [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) aufrufen, um Eingabestreamformate festzulegen. Andernfalls schlägt DMO Initialisierung fehl.

 

Wenn der Wert dieser Eigenschaft VARIANT \_ TRUE ist, verfügt der DSP über keine Eingaben. Wenn der Wert VARIANT \_ FALSE ist, verfügt der DSP abhängig vom Wert der [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE-Eigenschaft](mfpkey-wmaaecma-system-modeproperty.md) über eine oder zwei Eingaben, wie in der folgenden Tabelle dargestellt.



| Wert                     | Anzahl von Eingaben |
|---------------------------|------------------|
| MATRIBEAM \_ ARRAY \_ UND \_ AEC | 2                |
| NUR DAS PALETTENARRAY "ONLY" \_ \_     | 1                |
| SINGLE \_ CHANNEL \_ AEC      | 2                |
| SINGLE \_ CHANNEL \_ NSAGC    | 1                |



 

> [!Note]  
> Nur Modi mit einer einzelnen Eingabe funktionieren mit dem Wrapperfilter DMO der DirectShow 9.0-API.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Spracherfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
