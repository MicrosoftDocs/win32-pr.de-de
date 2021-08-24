---
title: EM_SETTABLEPARMS (Richedit.h)
description: Ändert die Parameter von Zeilen in einer Tabelle.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- EM_SETTABLEPARMS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_SETTABLEPARMS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccb6258f03d76391bf2288331efb3d9ebde4fb903fe907eaa5e9d37e7497a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576350"
---
# <a name="em_settableparms-message"></a>EM \_ SETTABLEPARMS-Meldung

Ändert die Parameter von Zeilen in einer Tabelle.

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



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Änderungen können nicht vorgenommen werden. Dies kann auftreten, wenn das Steuerelement ein Nur-Text- oder einzeigen-Steuerelement ist oder wenn sich die Einfügemarke in einem mathematischen Objekt befindet. Sie tritt auch auf, wenn Tabellen deaktiviert sind oder wenn die [**EM \_ SETEDITSTYLEEX-Meldung**](em-seteditstyleex.md) den **SES \_ EX \_ NOTABLE-Wert fest** legt. <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *wParam* oder *lParam* ist NULL oder verweist auf eine ungültige Struktur. Der **cCell-Member** der [**TABLEROWPARMS-Struktur**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) muss mindestens 1 und nicht mehr als 63 sein. Der **cbRow-Member** muss gleich oder `sizeof(TABLEROWPARMS)` `sizeof(TABLEROWPARMS)   2*sizeof(long)` sein. Der zweite Wert ist die Größe der RichEdit 4.1 **TABLEROWPARMS-Struktur.** Das **cbCell-Member** von **TABLEROWPARMS muss** gleich `sizeof(TABLECELLPARMS)` sein. Die Einfügemarke muss am Anfang einer Tabelle oder innerhalb einer Tabellenzeile stehen, und die Anzahl der Zellen kann sich nur um eins ändern. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Diese Meldung ändert die Parameter der Anzahl der Zeilen, die vom **cRow-Member** der [**TABLEROWPARMS-Struktur**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) angegeben werden, wenn die Tabelle über so viele aufeinander folgende Zeilen verfügt. Wenn **cRow** kleiner als 0 ist, wird die Nachricht bis zum Ende der Tabelle durch iteriert. Wenn sich die neue Zellenanzahl von der aktuellen Zellenanzahl um +1 oder 1 unterscheidet, wird die Zelle an dem vom **iCell-Member** von **TABLEROWPARMS** angegebenen Index eingefügt oder gelöscht. Die Anfangstabellenzeile wird durch eine Zeichenposition identifiziert. Diese Position wird von **cpStartRow-Membern** mit Werten angegeben, die größer oder gleich 0 (null) sind. Die Position sollte innerhalb der Tabellenzeile, aber nicht innerhalb einer geschachtelten Tabelle liegen, es sei denn, Sie möchten die Parameter dieser Tabelle ändern. Wenn das **cpStartRow-Member** 1 ist, wird die Zeichenposition durch die aktuelle Auswahl angegeben. Positionieren Sie hierzu die Auswahl an einer beliebigen Stelle innerhalb der Tabellenzeile, oder wählen Sie die Zeile mit dem aktiven Ende der Auswahl am Ende der Tabellenzeile aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ GETTABLEPARMS**](em-gettableparms.md)
</dt> </dl>

 

 





