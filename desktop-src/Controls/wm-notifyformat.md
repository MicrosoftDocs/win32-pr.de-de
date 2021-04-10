---
title: WM_NOTIFYFORMAT Meldung (Winuser. h)
description: Bestimmt, ob ein Fenster ANSI-oder Unicode-Strukturen in der WM- \_ Benachrichtigungs Meldung akzeptiert. WM \_ notifyformat-Meldungen werden von einem allgemeinen Steuerelement an das übergeordnete Fenster und vom übergeordneten Fenster an das allgemeine Steuerelement gesendet.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- Windows-Steuerelemente für WM_NOTIFYFORMAT Meldung
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956710"
---
# <a name="wm_notifyformat-message"></a>WM \_ notifyformat-Meldung

Bestimmt, ob ein Fenster ANSI-oder Unicode-Strukturen in der [**WM- \_**](wm-notify.md) Benachrichtigungs Meldung akzeptiert. **WM \_ Notifyformat** -Meldungen werden von einem allgemeinen Steuerelement an das übergeordnete Fenster und vom übergeordneten Fenster an das allgemeine Steuerelement gesendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, das die **WM \_ notifyformat** -Meldung sendet. Wenn *LPARAM* eine NF- \_ Abfrage ist, ist dieser Parameter das Handle für ein Steuerelement. Wenn *LPARAM* eine "NF \_ Requery" ist, ist dieser Parameter das Handle für das übergeordnete Fenster eines Steuer Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Der-Befehls Wert, der die Art der " **WM \_ notifyformat** "-Meldung angibt. Dies ist einer der folgenden Werte:



| Wert                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <dt>**NF- \_ Abfrage**</dt> </dl>       | Die Meldung ist eine Abfrage, mit der bestimmt wird, ob ANSI-oder Unicode-Strukturen in [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten verwendet werden sollen. Dieser Befehl wird von einem-Steuerelement an das übergeordnete Fenster während der Erstellung eines-Steuer Elements und als Reaktion auf einen NF- \_ requenbefehl gesendet.<br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <dt>**NF- \_ Requery**</dt> </dl> | Die Meldung ist eine Anforderung für ein Steuerelement, ein NF- \_ Abfrageformular dieser Nachricht an das übergeordnete Fenster zu senden. Dieser Befehl wird vom übergeordneten Fenster gesendet. Das übergeordnete Fenster fordert das Steuerelement auf, ihn über den in der [**WM- \_ Benachrichtigungs Meldung**](wm-notify.md) zu verwendenden Typ von Strukturen aufzufordern. Wenn *LPARAM* eine "NF \_ Requery" ist, ist der Rückgabewert das Ergebnis des anfragevorgangs.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                                 | Beschreibung                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NFR- \_ ANSI**</dt> </dl>    | ANSI-Strukturen sollten in [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen verwendet werden, die vom Steuerelement gesendet werden.<br/>     |
| <dl> <dt>**NFR- \_ Unicode**</dt> </dl> | Unicode-Strukturen sollten in vom Steuerelement gesendeten [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen verwendet werden. <br/> |
| <dl> <dt>**0**</dt> </dl>            | Ein Fehler ist aufgetreten.<br/>                                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein gemeinsames Steuerelement erstellt wird, sendet das Steuerelement eine **WM \_ notifyformat** -Meldung an das übergeordnete Fenster, um den Typ der Strukturen zu ermitteln, die in [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten verwendet werden sollen. Wenn das übergeordnete Fenster diese Nachricht nicht verarbeitet, antwortet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion entsprechend dem Typ des übergeordneten Fensters. Das heißt, wenn das übergeordnete Fenster ein Unicode-Fenster ist, gibt **defwindowproc** NFR \_ Unicode zurück, und wenn das übergeordnete Fenster ein ANSI-Fenster ist, gibt **defwindowproc** NFR \_ ANSI zurück. Wenn das übergeordnete Fenster ein Dialogfeld ist und diese Meldung nicht verarbeitet, antwortet die [**defdlgproc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) -Funktion entsprechend dem Typ des Dialog Felds (Unicode oder ANSI).

Ein übergeordnetes Fenster kann den Typ der Strukturen ändern, die von einem allgemeinen Steuerelement in [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen verwendet werden, indem *LPARAM* auf \_ die NF-Anforderung festgelegt und eine **WM \_ notifyformat** -Nachricht an das Steuerelement gesendet Dies bewirkt, dass das Steuerelement ein NF- \_ Abfrageformular der **WM \_ notifyformat** -Nachricht an das übergeordnete Fenster sendet.

Alle allgemeinen Steuerelemente senden **WM \_ notifyformat** -Meldungen. Bei den standardmäßigen Windows-Steuerelementen (Bearbeitungs Steuerelemente, Kombinations Felder, Listenfelder, Schaltflächen, Bild Lauf leisten und statische Steuerelemente) ist dies jedoch nicht der Fall.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

