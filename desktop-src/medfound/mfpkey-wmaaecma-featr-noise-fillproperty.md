---
description: Gibt an, ob der Spracherfassungs-DSP Füllgeräusche ausführt.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec3f2f6780157da97263bd6e68ac5f38c9448a5633fafe6481b082ed033331dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035118"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>MFPKEY \_ WMAAECMA \_ FEATR \_ NOISE \_ FILL-Eigenschaft

Gibt an, ob der Spracherfassungs-DSP Füllgeräusche ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

VARIANT \_ TRUE

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Durch die Füllfüllung wird eine kleine Menge an Rauschen zu Teilen des Signals hinzugefügt, bei denen die Restgeräusche durch zentriertes Clipping entfernt wurden. Dies führt zu einer besseren Erfahrung für den Benutzer, als stille Lücken im Signal zu hinterlassen.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | Beschreibung            |
|----------------|------------------------|
| VARIANT \_ TRUE  | Aktivieren Sie die Füllfüllung.  |
| VARIANT \_ FALSE | Deaktivieren Sie das Auffüllen von Rauschen. |



 

Der Standardwert dieser Eigenschaft ist VARIANT \_ TRUE (aktiviert). Bevor Sie diese Eigenschaft festlegen, müssen Sie die [MFPKEY \_ WMAAECMA \_ FEATURE \_ MODE-Eigenschaft](mfpkey-wmaaecma-feature-modeproperty.md) auf VARIANT \_ TRUE festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

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

 

 
