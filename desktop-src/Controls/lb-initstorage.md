---
title: LB_INITSTORAGE Meldung (Winuser. h)
description: Ordnet Arbeitsspeicher zum Speichern von Listenfeld Elementen zu. Diese Meldung wird verwendet, bevor eine Anwendung eine große Anzahl von Elementen zu einem Listenfeld hinzufügt.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- Windows-Steuerelemente für LB_INITSTORAGE Meldung
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476815"
---
# <a name="lb_initstorage-message"></a>LB- \_ InitStorage-Nachricht

Ordnet Arbeitsspeicher zum Speichern von Listenfeld Elementen zu. Diese Meldung wird verwendet, bevor eine Anwendung eine große Anzahl von Elementen zu einem Listenfeld hinzufügt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der hinzu zufügenden Elemente.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Größe des Arbeitsspeichers in Bytes, der für Element Zeichenfolgen belegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Gesamtzahl der Elemente, für die Speicher reserviert wurde, d. h. die Gesamtanzahl der Elemente, die von allen erfolgreichen **lb- \_ InitStorage** -Nachrichten hinzugefügt wurden.

Wenn die Meldung fehlschlägt, ist der Rückgabewert "lb \_ errspace".

Microsoft Windows NT 4,0: Diese Nachricht weist nicht die angegebene Arbeitsspeicher Menge zu. Allerdings wird immer der im *wParam* -Parameter angegebene Wert zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die " **lb- \_ InitStorage** "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen. Sie reserviert die angegebene Arbeitsspeicher Menge, sodass nachfolgende [**lb- \_ AddString**](lb-addstring.md)-, [**lb- \_ InsertString**](lb-insertstring.md)-, [**lb \_**](lb-dir.md)-und [**lb- \_ AddFile**](lb-addfile.md) -Nachrichten die kürzeste Zeit in Anspruch nehmen. Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden. Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

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

[**LB- \_ AddFile**](lb-addfile.md)
</dt> <dt>

[**LB- \_ AddString**](lb-addstring.md)
</dt> <dt>

[**LB- \_ dir**](lb-dir.md)
</dt> <dt>

[**LB- \_ InsertString**](lb-insertstring.md)
</dt> </dl>

 

 





