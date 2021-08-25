---
title: EM_INSERTTABLE Nachricht (Richedit.h)
description: Fügt eine oder mehrere identische Tabellenzeilen mit leeren Zellen ein.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 5a015ae2b9a886ddfa24591944f3f70eca8cb192af771c821df9e4a403c837d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413058"
---
# <a name="em_inserttable-message"></a>EM \_ INSERTTABLE-Meldung

Fügt eine oder mehrere identische Tabellenzeilen mit leeren Zellen ein.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeiger auf eine [**TABLEROWPARMS-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms)

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**TABLECELLPARMS-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Tabelle eingefügt wird, oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Hinweise

Wenn das **cpStartRow-Element** von [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) 1 ist, löscht diese Meldung den ausgewählten Text (falls vorhanden) und fügt dann leere Tabellenzeilen mit den Zeilen- und Zellenparametern ein, die von *wParam* und *lParam* angegeben werden. Die Auswahl bleibt so, dass sie auf den Anfang der ersten Zelle in der ersten Zeile verweist. Der Client kann dann die Tabellenzellen auffüllen, indem er die Auswahl (oder einen [**ITextRange)**](/windows/desktop/api/Tom/nn-tom-itextrange)auf die verschiedenen Zellenendemarkierungen zeigt und den gewünschten Text einfügt und formatiert. Dieser Text kann geschachtelte Tabellenzeilen enthalten. Wenn der **cpStartRow-Member** von **TABLEROWPARMS** 0 oder höher ist, werden alternativ Tabellenzeilen an der von **cpStartRow** angegebenen Zeichenposition eingefügt. Dadurch wird die aktuelle Auswahl nur geändert, wenn die Tabelle in den ausgewählten Text eingefügt wird.

Eine Microsoft Rich Edit-Tabelle besteht aus einer Sequenz von Tabellenzeilen, die wiederum aus Sequenzen von Absätzen bestehen. Eine Tabellenzeile beginnt mit dem speziellen Absatz U+FFF9 U+000D mit zwei Zeichen und endet mit dem Absatz U+FFFB U+000D mit zwei Zeichen. Jede Zelle wird durch die Zellenmarkierung U+0007 beendet, die als harte Absatzendemarkierung behandelt wird, genauso wie U+000D (CR). Die Tabellenzeilen- und Zellenparameter werden als spezielle Absatzformatierung der Tabellenzeilentrennzeichen behandelt. Die Formatierung enthält die Informationen in der [**TABLEROWPARMS-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) Die von der [**TABLECELLPARMS-Struktur**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) angegebenen Zellenparameter werden in einer erweiterten Version des Tabstopparrays gespeichert. Mit diesem Format können Tabellen in anderen Tabellen geschachtelt werden, bis zu 15 Ebenen tief.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ INSERTIMAGE**](em-insertimage.md)
</dt> </dl>

 

 





