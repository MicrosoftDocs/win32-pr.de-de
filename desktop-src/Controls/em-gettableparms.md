---
title: EM_GETTABLEPARMS Meldung (RichEdit. h)
description: Ruft die Tabellen Parameter für eine Tabellenzeile und die Zellen Parameter für die angegebene Anzahl von Zellen ab.
ms.assetid: 36ADA41B-735B-4D6E-92B1-33260C71DF73
keywords:
- Windows-Steuerelemente für EM_GETTABLEPARMS Meldung
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
ms.openlocfilehash: b7eb244b64258b1cf83559e21affea51b1d0c5d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858849"
---
# <a name="em_gettableparms-message"></a>EM \_ gettableparamems-Meldung

Ruft die Tabellen Parameter für eine Tabellenzeile und die Zellen Parameter für die angegebene Anzahl von Zellen ab.


```C++
#define EM_GETTABLEPARMS       (WM_USER + 265)
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

Gibt \_ bei Erfolg S OK oder einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_** Fehler</dt> </dl>        | Es können keine Änderungen vorgenommen werden. Dies kann vorkommen, wenn es sich bei dem Steuerelement um ein nur-Text-oder einzeilige Steuerelement handelt oder wenn sich die Einfügemarke in einem mathematischen Objekt befindet. Es tritt auch auf, wenn Tabellen deaktiviert werden, wenn die " [**EM \_ seteditstyleex**](em-seteditstyleex.md) "-Meldung den Wert " **SES \_ Ex \_** relevante" festlegt. <br/>                                                                                                                                                                     |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>   | Der *wParam* -oder *LPARAM* -Wert ist NULL oder zeigt auf eine ungültige Struktur. Der **cbrow** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur muss gleich `sizeof(TABLEROWPARMS)` oder sizeof (tablerowparamems) 2 \* sizeof (Long) sein. Der letztere Wert ist die Größe der RichEdit 4,1 **tablerowparamems** -Struktur. Der **cbcell** -Member der **tablerowparamems** -Struktur muss gleich sein `sizeof(TABLECELLPARMS)` . Die Position des abfragezeichens muss ein Tabellenzeilen Trennzeichen sein. |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Diese Nachricht Ruft die Tabellen Parameter für die Zeile an der Zeichenposition ab, die vom **cpstartrow** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur angegeben wird, sowie die Anzahl der Zellen, die durch den **ccells** -Member der [**tablecellparamems**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) -Struktur angegeben wird.

Die Zeichenposition, die vom **cpstartrow** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur angegeben wird, muss sich am Anfang der Tabellenzeile oder am endtrennzeichen der Tabellenzeile befinden. Wenn **cpstartrow** auf 1 festgelegt ist, wird die Zeichenposition von der aktuellen Auswahl angegeben. Positionieren Sie in diesem Fall die Auswahl am Ende der Zeile (zwischen der Zelle und dem endtrennzeichen der Tabellenzeile), oder wählen Sie die Zeile aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ settableparamems**](em-settableparms.md)
</dt> </dl>

 

 





