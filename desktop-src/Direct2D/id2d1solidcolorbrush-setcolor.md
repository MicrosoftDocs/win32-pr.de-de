---
title: ID2D1SolidColorBrush SetColor-Methoden
description: Gibt die Farbe dieses Pinsel mit voll Tonfarbe an.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- SetColor-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362047"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>ID2D1SolidColorBrush:: SetColor-Methoden

Gibt die Farbe dieses Pinsel mit voll Tonfarbe an.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                          | BESCHREIBUNG                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**SetColor (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Gibt die Farbe dieses Pinsel mit voll Tonfarbe an. <br/> |
| [**SetColor (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Gibt die Farbe dieses Pinsel mit voll Tonfarbe an. <br/> |



## <a name="remarks"></a>Bemerkungen

Zur Unterstützung der Erstellung von Farben bietet Direct2D die [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse. Es bietet mehrere Hilfsmethoden zum Erstellen von Farben und stellt eine Menge oder vordefinierte Farben bereit.

## <a name="examples"></a>Beispiele

Der folgende Code zeigt, wie diese Methode verwendet wird.


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

