---
title: CB_INITSTORAGE Meldung (Winuser.h)
description: Eine Anwendung sendet die CB \_ INITSTORAGE-Nachricht, bevor dem Listenfeldteil eines Kombinationsfelds eine große Anzahl von Elementen hinzugefügt wird. Diese Meldung belegt Arbeitsspeicher zum Speichern von Listenfeldelementen.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be1aeccdde2c81c87956a42e72440732ff9eb2732cbd066f51308816c01f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089090"
---
# <a name="cb_initstorage-message"></a>CB \_ INITSTORAGE-Meldung

Eine Anwendung sendet die **CB \_ INITSTORAGE-Nachricht,** bevor dem Listenfeldteil eines Kombinationsfelds eine große Anzahl von Elementen hinzugefügt wird. Diese Meldung belegt Arbeitsspeicher zum Speichern von Listenfeldelementen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der hinzuzufügende Elemente.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Menge an Arbeitsspeicher, die für Elementzeichenfolgen in Bytes zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Elemente, für die Speicher vorab zugeordnet wurde, d. h. die Gesamtzahl der Elemente, die von allen erfolgreichen **CB \_ INITSTORAGE-Nachrichten** hinzugefügt wurden.

Wenn die Nachricht fehlschlägt, lautet der Rückgabewert CB \_ ERRSPACE.

Die Meldung belegt Arbeitsspeicher und gibt die oben beschriebenen Erfolgs- und Fehlerwerte zurück.

## <a name="remarks"></a>Hinweise

Die **CB \_ INITSTORAGE-Nachricht** beschleunigt die Initialisierung von Kombinationsfeldern mit einer großen Anzahl von Elementen (über 100). Sie reserviert die angegebene Arbeitsspeichermenge, sodass nachfolgende [**CB \_ ADDSTRING-,**](cb-addstring.md) [**CB \_ INSERTSTRING-**](cb-insertstring.md)und [**CB \_ DIR-Nachrichten**](cb-dir.md) so kurz wie möglich dauern. Sie können Schätzungen für die *Parameter wParam* und *lParam* verwenden. Wenn Sie dies überschätzen, wird der zusätzliche Arbeitsspeicher belegt. Wenn Sie dies dezimieren, wird die normale Zuordnung für Elemente verwendet, die die angeforderte Menge überschreiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





