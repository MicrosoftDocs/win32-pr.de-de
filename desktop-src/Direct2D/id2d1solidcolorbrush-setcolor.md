---
title: ID2D1SolidColorBrush SetColor-Methoden
description: Gibt die Farbe dieses Volltonfarbpinsels an.
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
ms.openlocfilehash: eb281265a9567db5da6252944fa1da1a6beb1bd4a0fb2a6a4d80ef1177455fc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873950"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>ID2D1SolidColorBrush::SetColor-Methoden

Gibt die Farbe dieses Volltonfarbpinsels an.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                          | Beschreibung                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**SetColor(D2D1 \_ COLOR \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Gibt die Farbe dieses Volltonfarbpinsels an. <br/> |
| [**SetColor(D2D1 \_ COLOR \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Gibt die Farbe dieses Volltonfarbpinsels an. <br/> |



## <a name="remarks"></a>Hinweise

Um Farben zu erstellen, stellt Direct2D die [**ColorF-Klasse**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) zurVerf. Es bietet mehrere Hilfsmethoden zum Erstellen von Farben und stellt einen Satz oder vordefinierte Farben zurEntiert.

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
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

