---
title: gladdtauaphintrectwin-Funktion (GL. h)
description: Die Funktion "gladdswap aphintrectwin" gibt einen Satz von Rechtecke an, die von "Swap" kopiert werden sollen.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- gladdtauaphintrectwin-Funktion OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391999"
---
# <a name="gladdswaphintrectwin-function"></a>gladdtauaphintrectwin-Funktion

Die Funktion " **gladdswap aphintrectwin** " gibt einen Satz von Rechtecke an, die von " [**Swap**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)" kopiert werden sollen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* 
</dt> <dd>

Die *x*-Koordinate (in Fenster Koordinaten) der unteren linken Ecke des Hint-Bereichs Rechtecks.

</dd> <dt>

*y* 
</dt> <dd>

Die *y*-Koordinate (in Fenster Koordinaten) der unteren linken Ecke des Hint-Bereichs Rechtecks.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Hint-Bereichs Rechtecks.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Hint-Bereichs Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **gladdtauaphintrectwin** " beschleunigt die Animation, indem die Menge an Umzeichnung zwischen Frames reduziert wird. Mit " **gladdtauaphintrectwin**" geben Sie einen Satz von rechteckigen Bereichen an, die beim Abrufen von " [**Austausch Puffern**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)" kopiert werden sollen. Wenn Sie vor dem Aufrufen von " **Austausch Puffer**" keine Rechtecke mit " **gladdtauaphintrectwin** " angeben, wird der gesamte Frame Puffer ausgetauscht. Die Verwendung von " **gladdtauaphintrectwin** ", um nur geänderte Teile des Puffers zu kopieren, kann die Leistung von "Swap"- **Puffer** erheblich erhöhen, insbesondere dann, wenn " **Swap Buffers** " in Software implementiert ist.

Die Funktion " **gladdtauaphintrectwin** " fügt dem Hinweis Bereich ein Rechteck hinzu. Wenn das PFD \_ - \_ auslagerungskopierflag der [**pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) -Pixel Format Struktur festgelegt ist, verwendet **swapbuffers** diesen Bereich, um das Kopieren des Hintergrund Puffers auf den Frontpuffer abzuschneiden. Sie geben die PFD \_ - \_ swapkopie nicht an. Sie wird durch die leistungsfähige Hardware festgelegt. Der Hinweis Bereich wird nach jedem Rückruf von " **Austausch Puffer**" gelöscht. Bei manchen Hardware Konfigurationen können **Austausch Puffer** den Hinweis Bereich ignorieren und den gesamten Puffer austauschen. **Swap-Puffer** werden vom System implementiert, nicht von der Anwendung.

OpenGL verwaltet für jedes Fenster einen separaten Hinweis Bereich. Wenn Sie " **gladdtauaphintrectwin** " für alle einem Fenster zugeordneten renderingkontexte aufzurufen, werden die Hinweis Rechtecke in einer einzelnen Region kombiniert.

Wenden Sie " **gladdtauaphintrectwin** " mit einem umschließenden Rechteck für jedes für einen Frame gezeichnete Objekt an, und für jedes Rechteck, das zum Löschen Vorheriger Frame Objekte gelöscht wurde.

> [!Note]  
> Die Funktion " **gladdswaphintrectwin** " ist eine Erweiterungs Funktion, die nicht Teil der OpenGL-Standardbibliothek ist, aber Teil der GL- \_ Win-Swap- \_ \_ Hinweis Erweiterung ist. Um zu überprüfen, ob die Implementierung von OpenGL " **gladdtauaphintrectwin**" unterstützt, nennen Sie " **glgetstring**(GL \_ Extensions)". Wenn der GL. Win-Swap-Hinweis zurückgegeben wird \_ \_ \_ , wird " **gladdswaphintrectwin** " unterstützt. Rufen Sie zum Abrufen der Adresse einer Erweiterungs Funktion **wglgetprocaddress** auf.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glgetstring**](glgetstring.md)
</dt> <dt>

[**Pixelformatdescriptor**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[**Austausch Puffer**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[**wglgetprocaddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





