---
title: glAddSwapHintRectWIN-Funktion (Gl.h)
description: Die Rückruffunktion glAddSwapHintRectWIN gibt einen Satz von Rechtecke an, die von SwapBuffers kopiert werden sollen.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- glAddSwapHintRectWIN-Funktion OpenGL
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
ms.openlocfilehash: 75077ac2a93e3e952ae3c3daca3ea847f7b4b0efc340da0e980b1a4bec6efa64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618050"
---
# <a name="gladdswaphintrectwin-function"></a>glAddSwapHintRectWIN-Funktion

Die **Rückruffunktion glAddSwapHintRectWIN** gibt einen Satz von Rechtecke an, die von [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)kopiert werden sollen.

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

Die x-Koordinate (in Fensterkoordinaten) der unteren linken Ecke des Rechtecks für den Hinweisbereich.

</dd> <dt>

*y* 
</dt> <dd>

Die y-Koordinate (in Fensterkoordinaten) der unteren linken Ecke des Rechtecks für den Hinweisbereich.

</dd> <dt>

*width* 
</dt> <dd>

Die Breite des Rechtecks für den Hinweisbereich.

</dd> <dt>

*height* 
</dt> <dd>

Die Höhe des Rechtecks für den Hinweisbereich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glAddSwapHintRectWIN-Funktion** beschleunigt die Animation, indem sie die Menge der Neumalungen zwischen Frames reduziert. Mit **glAddSwapHintRectWIN** geben Sie einen Satz rechteckiger Bereiche an, die kopiert werden sollen, wenn Sie [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)aufrufen. Wenn Sie vor dem Aufrufen von **SwapBuffers** keine Rechtecke mit **glAddSwapHintRectWIN** angeben, wird der gesamte Framepuffer ausgetauscht. Die Verwendung von **glAddSwapHintRectWIN** zum Kopieren nur geänderter Teile des Puffers kann die Leistung von **SwapBuffers** erheblich steigern, insbesondere wenn **SwapBuffers** in Software implementiert ist.

Die **glAddSwapHintRectWIN-Funktion** fügt dem Hinweisbereich ein Rechteck hinzu. Wenn das PFD \_ SWAP \_ COPY-Flag der [**Pixelformatstruktur PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) festgelegt ist, verwendet **SwapBuffers** diesen Bereich, um das Kopieren des Hintergrundpuffers in den Frontpuffer abzuschneiden. Sie geben PFD SWAP COPY nicht an. Sie \_ \_ wird von der fähigen Hardware festgelegt. Der Hinweisbereich wird nach jedem Aufruf von **SwapBuffers** gelöscht. Bei einigen Hardwarekonfigurationen kann **SwapBuffers** den Hinweisbereich ignorieren und den gesamten Puffer austauschen. **SwapBuffers** wird vom System und nicht von der Anwendung implementiert.

OpenGL verwaltet für jedes Fenster einen separaten Hinweisbereich. Wenn Sie **glAddSwapHintRectWIN** für alle Einem Fenster zugeordneten Renderingkontexte aufrufen, werden die Hinweisrechtecke in einem einzelnen Bereich kombiniert.

Rufen **Sie glAddSwapHintRectWIN** mit einem umschließenden Rechteck für jedes für einen Frame gezeichnete Objekt und für jedes Rechteck auf, das gelöscht wird, um vorherige Frameobjekte zu löschen.

> [!Note]  
> Die **glAddSwapHintRectWIN-Funktion** ist eine Erweiterungsfunktion, die nicht Teil der OpenGL-Standardbibliothek ist, sondern Teil der GL \_ \_ WIN-Austauschhinweiserweiterung \_ ist. Um zu überprüfen, ob Ihre Implementierung von OpenGL **glAddSwapHintRectWIN** unterstützt, rufen Sie **glGetString**(GL \_ EXTENSIONS) auf. Wenn der GL \_ \_ WIN-Swaphinweis zurückgegeben \_ wird, wird **glAddSwapHintRectWIN** unterstützt. Rufen Sie **wglGetProcAddress** auf, um die Adresse einer Erweiterungsfunktion abzurufen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





