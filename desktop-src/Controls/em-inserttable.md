---
title: EM_INSERTTABLE Meldung (RichEdit. h)
description: Fügt eine oder mehrere identische Tabellenzeilen mit leeren Zellen ein.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- Windows-Steuerelemente für EM_INSERTTABLE Meldung
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475555"
---
# <a name="em_inserttable-message"></a>EM \_ insertfähige Nachricht

Fügt eine oder mehrere identische Tabellenzeilen mit leeren Zellen ein.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeiger auf eine [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**tablecellparamems**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Tabelle eingefügt wird, andernfalls einen Fehlercode.

## <a name="remarks"></a>Bemerkungen

Wenn der **cpstartrow** -Member von [**tablerowparms**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) 1 ist, löscht diese Meldung den markierten Text (sofern vorhanden) und fügt dann leere Tabellenzeilen mit den Zeilen-und Zell Parametern ein, die von *wParam* und *LPARAM* angegeben werden. Dadurch wird die Auswahl auf den Anfang der ersten Zelle in der ersten Zeile verwiesen. Der Client kann dann die Tabellenzellen auffüllen, indem er die Auswahl (oder ein [**itextrange**](/windows/desktop/api/Tom/nn-tom-itextrange)) auf die verschiedenen Zell Endmarkierungen zeigt und den gewünschten Text einfügt und formatiert. Dieser Text kann Zeilen in der Zeilen Tabelle einschließen. Wenn der **cpstartrow** -Member der **tablerowparamems** gleich 0 (null) oder größer ist, werden die Tabellenzeilen an der von **cpstartrow** angegebenen Zeichenposition eingefügt. Dadurch wird nur die aktuelle Auswahl geändert, wenn die Tabelle in den ausgewählten Text eingefügt wird.

Eine Microsoft Rich Edit-Tabelle besteht aus einer Sequenz von Tabellenzeilen, die wiederum aus Sequenzen von Absätzen bestehen. Eine Tabellenzeile beginnt mit dem speziellen Trennzeichen Absatz für zwei Zeichen u + FFF9 u + 000D und endet mit dem zweistelligen Trennzeichen Absatz u + fffb u + 000D. Jede Zelle wird von der Zelle u + 0007 beendet, die als eine feste Zeichenfolge gekennzeichnet wird, ebenso wie U + 000D (CR). Die Tabellenzeilen-und Zellen Parameter werden als spezielle Absatz Formatierung der Tabellenzeilen Trennzeichen behandelt. Die Formatierung enthält die Informationen in der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur. Die Zellen Parameter, die von der [**tablecellparms**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur angegeben werden, werden in einer erweiterten Version des Registerkarten Arrays gespeichert. In diesem Format können Tabellen in anderen Tabellen geschachtelt werden, bis zu 15 Ebenen tief.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ InsertImage**](em-insertimage.md)
</dt> </dl>

 

 





