---
title: ICM_GETSTATE Nachricht (Vfw.h)
description: Die ICM \_ GETSTATE-Nachricht fragt einen Videokomprimierungstreiber ab, um seine aktuelle Konfiguration in einem Speicherblock zurückzugeben oder die Menge des Arbeitsspeichers zu bestimmen, der zum Abrufen der Konfigurationsinformationen erforderlich ist.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bf21d808752b8a3ac3ba71a8593cd6dc577b3af4f34f421682d126c73b3578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784950"
---
# <a name="icm_getstate-message"></a>\_ICM GETSTATE-Nachricht

Die **ICM \_ GETSTATE-Nachricht** fragt einen Videokomprimierungstreiber ab, um seine aktuelle Konfiguration in einem Speicherblock zurückzugeben oder die Menge des Arbeitsspeichers zu bestimmen, der zum Abrufen der Konfigurationsinformationen erforderlich ist. Sie können diese Nachricht explizit oder mithilfe des [**ICGetState-Makros**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) senden.


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*Pv*
</dt> <dd>

Zeiger auf einen Speicherblock, der die aktuellen Konfigurationsinformationen enthalten soll. Sie können **NULL** für diesen Parameter angeben, um die Menge an Arbeitsspeicher zu bestimmen, die für die Konfigurationsinformationen erforderlich ist, wie in [**ICGetStateSize.**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize)

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Größe des Speicherblocks in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn *pv* **NULL** ist, wird die Arbeitsspeichermenge in Bytes zurückgegeben, die für Konfigurationsinformationen erforderlich ist.

Wenn *pv* nicht **NULL** ist, gibt ICERR \_ OK zurück, wenn erfolgreich, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die Struktur, die zur Darstellung von Konfigurationsinformationen verwendet wird, ist treiberspezifisch und wird vom Treiber definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





