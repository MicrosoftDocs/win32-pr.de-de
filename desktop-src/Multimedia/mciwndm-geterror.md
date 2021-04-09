---
title: MCIWNDM_GETERROR Meldung (VFW. h)
description: Die mciwndm \_ getError-Nachricht Ruft den letzten gefundenen MCI-Fehler ab. Sie können diese Nachricht explizit oder mit dem mciwndgeterror-Makro senden.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- MCIWNDM_GETERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858705"
---
# <a name="mciwndm_geterror-message"></a>Mciwndm \_ getError-Meldung

Die **mciwndm \_ getError** -Nachricht Ruft den letzten gefundenen MCI-Fehler ab. Sie können diese Nachricht explizit oder mit dem [**mciwndgeterror**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) -Makro senden.


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Nest*
</dt> <dd>

Größe (in Bytes) des Fehler Puffers.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Zeiger auf einen Anwendungs definierten Puffer, der zum Zurückgeben der Fehler Zeichenfolge verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den ganzzahligen Fehlerwert zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Wenn die *LP* ein gültiger Zeiger ist, wird eine mit NULL beendete Zeichenfolge, die dem Fehler entspricht, im Puffer zurückgegeben. Wenn die Fehler Zeichenfolge länger als der Puffer ist, wird Sie von mciwnd abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mciwndgeterror**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





