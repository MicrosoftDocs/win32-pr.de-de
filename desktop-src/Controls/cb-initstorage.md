---
title: CB_INITSTORAGE Meldung (Winuser. h)
description: Eine Anwendung sendet die CB \_ InitStorage-Nachricht, bevor eine große Anzahl von Elementen zum Listenfeld Teil eines Kombinations Felds hinzugefügt wird. Diese Meldung weist Speicher zum Speichern von Listenfeld Elementen zu.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- Windows-Steuerelemente für CB_INITSTORAGE Meldung
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
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103627"
---
# <a name="cb_initstorage-message"></a>CB- \_ InitStorage-Nachricht

Eine Anwendung sendet die **CB \_ InitStorage** -Nachricht, bevor eine große Anzahl von Elementen zum Listenfeld Teil eines Kombinations Felds hinzugefügt wird. Diese Meldung weist Speicher zum Speichern von Listenfeld Elementen zu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der hinzu zufügenden Elemente.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Menge an Arbeitsspeicher, die für Element Zeichenfolgen in Bytes belegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Elemente, für die Speicher reserviert wurde, d. h. die Gesamtanzahl der Elemente, die von allen erfolgreichen **CB- \_ InitStorage** -Nachrichten hinzugefügt wurden.

Wenn die Meldung fehlschlägt, ist der Rückgabewert CB \_ errspace.

Die Meldung weist Arbeitsspeicher zu und gibt die oben beschriebenen Erfolgs-und Fehler Werte zurück.

## <a name="remarks"></a>Bemerkungen

Die **CB \_ InitStorage** -Nachricht beschleunigt die Initialisierung von Kombinations Feldern, die über eine große Anzahl von Elementen (über 100) verfügen. Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende [**CB \_ AddString**](cb-addstring.md)-, [**CB \_ InsertString**](cb-insertstring.md)-und [**CB- \_ dir**](cb-dir.md) -Nachrichten die kürzeste Zeit in Anspruch nehmen. Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden. Wenn Sie die Schätzung überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie dies unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB \_ AddString**](cb-addstring.md)
</dt> <dt>

[**CB- \_ dir**](cb-dir.md)
</dt> <dt>

[**CB \_ InsertString**](cb-insertstring.md)
</dt> </dl>

 

 





