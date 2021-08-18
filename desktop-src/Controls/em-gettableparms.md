---
title: EM_GETTABLEPARMS (Richedit.h)
description: Ruft die Tabellenparameter für eine Tabellenzeile und die Zellenparameter für die angegebene Anzahl von Zellen ab.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- EM_GETTABLEPARMS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ddca96ce29a0f7b7076580b48cfeceecf1f638830b7c77bc9406a39e97de57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545030"
---
# <a name="em_gettableparms-message"></a>EM \_ GETTABLEPARMS-Nachricht

Ruft die Tabellenparameter für eine Tabellenzeile und die Zellenparameter für die angegebene Anzahl von Zellen ab.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
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

Gibt S \_ OK zurück, wenn erfolgreich, oder einer der folgenden Fehlercodes.



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Änderungen können nicht vorgenommen werden. Dies kann auftreten, wenn das Steuerelement ein Nur-Text- oder einzeigen-Steuerelement ist oder wenn sich die Einfügemarke in einem mathematischen Objekt befindet. Sie tritt auch auf, wenn Tabellen deaktiviert sind, wenn die [**EM \_ SETEDITSTYLEEX-Meldung**](em-seteditstyleex.md) den **SES \_ EX \_ NOTABLE-Wert** fest legt. <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *wParam* oder *lParam* ist NULL oder verweist auf eine ungültige Struktur. Das **cbRow-Member** der [**TABLEROWPARMS-Struktur**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) muss gleich oder `sizeof(TABLEROWPARMS)` sizeof(TABLEROWPARMS) 2 \* sizeof(long) sein. Der zweite Wert ist die Größe der RichEdit 4.1 **TABLEROWPARMS-Struktur.** Der **cbCell-Member** der **TABLEROWPARMS-Struktur** muss gleich `sizeof(TABLECELLPARMS)` sein. Die Position des Abfragezeichens muss an einem Tabellenzeilentrennzeichen liegen. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Diese Meldung ruft die Tabellenparameter für die Zeile an der Zeichenposition ab, die vom **cpStartRow-Member** der [**TABLEROWPARMS-Struktur**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) angegeben wird, und die Anzahl der Zellen, die vom **cCells-Member** der [**TABLECELLPARMS-Struktur angegeben**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) werden.

Die vom **cpStartRow-Member** der [**TABLEROWPARMS-Struktur**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) angegebene Zeichenposition sollte am Anfang der Tabellenzeile oder am Endtrennzeichen der Tabellenzeile liegen. Wenn **cpStartRow** auf 1 festgelegt ist, wird die Zeichenposition durch die aktuelle Auswahl angegeben. Positionieren Sie in diesem Fall die Auswahl am Ende der Zeile (zwischen der Zellenmarkung und dem Endtrennzeichen der Tabellenzeile), oder wählen Sie die Zeile aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ SETTABLEPARMS**](em-settableparms.md)
</dt> </dl>

 

 





