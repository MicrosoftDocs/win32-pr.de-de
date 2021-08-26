---
title: ID2D1HwndRenderTarget Resize-Methoden (D2d1.h)
description: Ändert die Größe des Renderziels in die angegebene Pixelgröße.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Ändern der Größe von Direct2D-Methoden
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 31ffcae6473924e12ca428fd48927fd1507840dce4fdbce3a18e8f82ffe9fcaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917610"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>ID2D1HwndRenderTarget::Resize-Methoden

Ändert die Größe des Renderziels in die angegebene Pixelgröße.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                         | Beschreibung                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Resize(D2D1 \_ SIZE \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | Ändert die Größe des Renderziels in die angegebene Pixelgröße. <br/> |
| [**Resize(D2D1 \_ SIZE \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | Ändert die Größe des Renderziels in die angegebene Pixelgröße.<br/>  |



## <a name="remarks"></a>Hinweise

Nach dem Aufruf dieser Methode wird der Inhalt des Backpuffers des Renderziels nicht definiert, auch wenn die Option [**D2D1 \_ PRESENT OPTIONS RETAIN \_ \_ \_ CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) beim Erstellen des Renderziels angegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
