---
title: ID2D1HwndRenderTarget Resize-Methoden (D2d1. h)
description: Ändert die Größe des Renderziels in die angegebene Pixelgröße.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Größenänderung von Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370209"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>ID2D1HwndRenderTarget:: Resize-Methoden

Ändert die Größe des Renderziels in die angegebene Pixelgröße.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                         | BESCHREIBUNG                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Resize (D2D1 \_ size \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Ändert die Größe des Renderziels in die angegebene Pixelgröße. <br/> |
| [**Größe ändern (D2D1 \_ size \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Ändert die Größe des Renderziels in die angegebene Pixelgröße.<br/>  |



## <a name="remarks"></a>Bemerkungen

Nachdem diese Methode aufgerufen wurde, wird der Inhalt des Back Puffers des Renderziels nicht definiert, auch wenn beim Erstellen des Renderziels die [**D2D1 Present options-Option " \_ \_ \_ \_ Inhalt beibehalten**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) " angegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
