---
title: ID2D1CommandSink1 SetPrimitiveBlend1-Methode
description: Legt einen neuen primitiven Blend-Modus fest.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- SetPrimitiveBlend1-Methode Direct2D
- SetPrimitiveBlend1-Methode Direct2D, ID2D1CommandSink1-Schnittstelle
- ID2D1CommandSink1 Interface Direct2D, SetPrimitiveBlend1-Methode
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103546"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a>ID2D1CommandSink1:: SetPrimitiveBlend1-Methode

Legt einen neuen primitiven Blend-Modus fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*primitiveblend* 
</dt> <dd>

Type: **[ **D2D1 \_ primitive \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**

Die primitive Mischung, die auf nachfolgende primitive angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

### <a name="blend-modes"></a>Füllmethoden

Für das Rendern von Aliasing (mit Ausnahme des Min-Modus) wird der Ausgabewert O durch die lineare Interpolation der Werte *Blend (S, D)* mit dem Ziel Pixel Wert berechnet. Dies basiert auf dem Betrag, um den der primitive das Zielpixel abdeckt.

In der hier aufgeführten Tabelle werden die primitiven Blend-Modi für die Mischung aus Alias und Antialiasing angezeigt. Die in der Tabelle aufgeführten Gleichungen verwenden die folgenden Elemente:

-   O = Ausgabe
-   S = Quelle
-   Sa = quellalpha
-   D = Ziel
-   Da = zielalpha
-   C = Pixel Abdeckung



| Primitiver Blend-Modus                 | Vermischung mit Alias                            | Vermischung mit Antialiasing            | BESCHREIBUNG                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ primitive \_ Blend- \_ Quelle \_ über | O = (S + (1 SA) \* D) \* C + D \* (1 C) | O = S \* c + D \* (1 SA \* c)   | Der standardmäßige Quellen-über-Ziel-Blend-Modus.                                                                         |
| D2D1 \_ primitive \_ Blend- \_ Kopie kopieren         | O = S \* c + D \* (1 c)                   | O = S \* c + D \* (1 c)       | Die Quelle wird in das Ziel kopiert. die Ziel Pixel werden ignoriert.                                             |
| D2D1 \_ primitive \_ Blend \_ Min.          | O = min (S + 1-SA, D)                        | O = min (S \* c + 1 SA \* , D) | Die resultierenden Pixelwerte verwenden den minimalen Wert der Quell-und Ziel Pixelwerte. Verfügbar in Windows 8 und höher. |
| D2D1 \_ primitive \_ Blend- \_ Hinzufügen          | O = (S + d) \* C + d \* (1 c)             | O = S \* C + D                  | Die resultierenden Pixelwerte sind die Summe der Quell-und Ziel Pixelwerte. Verfügbar in Windows 8 und höher.     |



 

![eine Abbildung der primitiven Direct2D-Blend-Modi mit variierender Deckkraft und Hintergründen.](images/primblenddemo.png)

Eine Abbildung der primitiven Blend-Modi mit variierender Deckkraft und Hintergründen.

Die primitive Mischung gilt für alle primitiven, die auf dem Kontext gezeichnet werden, es sei denn, dies wird mit dem *compositemode* -Parameter in der [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) -API überschrieben.

Die primitive Mischung bezieht sich auf das innere aller primitiven, die auf dem Kontext gezeichnet werden. Im Fall von [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))wird dies durch das Bild Rechteck, den Offset und die globale Transformation impliziert.

Wenn die primitive Mischung nichts anderes als **D2D1 \_ primitiver \_ Blend \_** ist, wird das ClearType-Rendering deaktiviert. Wenn die Anwendung das ClearType-Rendering in diesen Modi explizit erzwingt, wird der Zeichnungs Kontext in einen Fehlerzustand versetzt. D2DERR \_ falscher \_ Zustand wird von " [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) " oder " [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)" zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1CommandSink1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

