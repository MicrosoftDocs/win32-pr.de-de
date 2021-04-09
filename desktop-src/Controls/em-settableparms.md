---
title: EM_SETTABLEPARMS Meldung (RichEdit. h)
description: Ändert die Parameter von Zeilen in einer Tabelle.
ms.assetid: 6CE9B8D1-68C9-4692-8454-24BC81E9038F
keywords:
- Windows-Steuerelemente für EM_SETTABLEPARMS Meldung
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
ms.openlocfilehash: 86fa77774bd7fcf461fc74b479a57304a5f8ee3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949709"
---
# <a name="em_settableparms-message"></a>EM \_ settableparamems-Meldung

Ändert die Parameter von Zeilen in einer Tabelle.

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



| Rückgabecode                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_** Fehler</dt> </dl>        | Es können keine Änderungen vorgenommen werden. Dies kann vorkommen, wenn es sich bei dem Steuerelement um ein nur-Text-oder einzeilige Steuerelement handelt oder wenn sich die Einfügemarke in einem mathematischen Objekt befindet. Sie tritt auch auf, wenn Tabellen deaktiviert sind, oder, wenn die Nachricht " [**EM \_ seteditstyleex**](em-seteditstyleex.md) " den Wert " **SES \_ Ex \_** relevante Werte" festlegt. <br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>   | Der *wParam* -oder *LPARAM* -Wert ist NULL oder zeigt auf eine ungültige Struktur. Der **ccell** -Member der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur muss mindestens 1 und nicht größer als 63 sein. Der **cbrow** -Member muss gleich `sizeof(TABLEROWPARMS)` oder sein `sizeof(TABLEROWPARMS)   2*sizeof(long)` . Der letztere Wert ist die Größe der RichEdit 4,1 **tablerowparamems** -Struktur. Der **cbcell** -Member von **tablerowparamems** muss gleich sein `sizeof(TABLECELLPARMS)` . Die Einfügemarke muss sich am Anfang einer Tabelle oder innerhalb einer Tabellenzeile befinden, und die Anzahl der Zellen kann nur um eins geändert werden. |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Diese Meldung ändert die Parameter der Anzahl von Zeilen, die durch das **cRow** -Element der [**tablerowparamems**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) -Struktur angegeben werden, wenn die Tabelle viele aufeinander folgende Zeilen enthält. Wenn der Wert für " **cRow** " kleiner als 0 ist, wird die Meldung bis zum Ende der Tabelle durchlaufen. Wenn die Anzahl der neuen Zellen von der Anzahl der aktuellen Zellen um + 1 oder 1 abweicht, wird die Zelle an dem Index eingefügt oder gelöscht, der durch den **icell** -Member von **tablerowparamems** angegeben wird. Die Zeile der Anfangs Tabelle wird durch eine Zeichenposition identifiziert. Diese Position wird von **cpstartrow** -Membern mit Werten angegeben, die größer oder gleich 0 (null) sind. Die Position sollte sich in der Tabellenzeile befinden, jedoch nicht innerhalb einer geschachtelten Tabelle, es sei denn, Sie möchten die Parameter der Tabelle ändern. Wenn der **cpstartrow** -Member 1 ist, wird die Zeichenposition von der aktuellen Auswahl angegeben. Positionieren Sie hierfür die Auswahl an einer beliebigen Position innerhalb der Tabellenzeile, oder wählen Sie die Zeile mit dem aktiven Ende der Auswahl am Ende der Tabellenzeile aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ gettablesparms**](em-gettableparms.md)
</dt> </dl>

 

 





