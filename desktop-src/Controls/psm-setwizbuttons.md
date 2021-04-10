---
title: PSM_SETWIZBUTTONS Meldung (prsht. h)
description: Aktiviert oder deaktiviert die Schaltflächen "zurück", "weiter" und "Fertigstellen" in einem Assistenten. Sie können die Nachricht auch mit dem propsheet- \_ Makro für das ""-/twizbuttons-Makro veröffentlichen.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- Windows-Steuerelemente für PSM_SETWIZBUTTONS Meldung
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104193"
---
# <a name="psm_setwizbuttons-message"></a>PSM-Meldung "Setup \_ Buttons"

Aktiviert oder deaktiviert die Schaltflächen " **zurück**", " **weiter**" und " **Fertig** stellen" in einem Assistenten. Sie können die Nachricht auch mit dem propsheet-Makro für das ""- [**\_ /twizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) -Makro veröffentlichen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Legen Sie diesen Parameter auf pswizbf \_ elevationrequired fest, um das Symbol mit erhöhten Rechten auf den in *LPARAM* angegebenen Schaltflächen anzuzeigen. Das Symbol für erhöhte Rechte (oder das UAC-Schild Symbol) gibt an, dass die Eingabeaufforderung für erhöhte Rechte verwendet wird, um den Benutzer zur Genehmigung bzw Weitere Informationen finden Sie unter [Entwerfen von UAC-Anwendungen für Windows Vista]( /previous-versions/bb756973(v=msdn.10)).

> [!Note]  
> Das Anzeigen des UAC-Schild Symbols wird nur in den aerowizard (PSH \_ aerowizard) unterstützt.

 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Wert, der angibt, welche Eigenschaften Blatt Schaltflächen aktiviert sind. Sie können eines oder mehrere der folgenden Flags kombinieren.



| Wert                                                                                                                                                                                 | Bedeutung                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**pswizb \_ zurück**</dt> </dl>                               | Aktiviert die Schaltfläche " **zurück** ". Wenn dieses Flag nicht festgelegt ist, wird die Schaltfläche " **zurück** " als deaktiviert angezeigt.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**pswizb \_ disabledfinish**</dt> </dl> | Zeigt die Schaltfläche **Fertig** stellen deaktiviert an.<br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**pswizb- \_ Fertigstellen**</dt> </dl>                         | Zeigt die Schaltfläche **Fertig** stellen aktiviert an.<br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**pswizb \_ als nächstes**</dt> </dl>                               | Hiermit wird die Schaltfläche **Weiter** aktiviert. Wenn dieses Flag nicht festgelegt ist, wird die Schaltfläche **weiter** als deaktiviert angezeigt.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn Ihr Benachrichtigungs Handler [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) verwendet, um eine PSM-Nachricht mit dem Wert " **\_ pingzbuttons** " zu senden, führen Sie nichts aus, das den Fokus des Fensters auf den Fenster Fokus auswirkt Wenn Sie z. b. [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) sofort nach dem Verwenden von **PostMessage** zum Senden von PSM-Setup Schaltflächen abrufen, erhält das Meldungs Feld den Fokus. **\_** Da bereitgestellte Nachrichten erst übermittelt werden, wenn Sie den Anfang der Nachrichten Warteschlange erreichen, wird die PSM-Nachricht "Setup **\_ Buttons** " erst übermittelt, wenn der Fokus auf das Meldungs Feld verschoben wurde. Folglich kann das Eigenschaften Blatt den Fokus nicht ordnungsgemäß für die Schaltflächen festlegen.

Wenn Sie die PSM- \_ Nachricht "setwizbuttons" während der Behandlung der Benachrichtigung " [PSN \_ SETACTIVE](psn-setactive.md) " senden, verwenden Sie die Funktion " [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) " anstelle der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion. Andernfalls werden die Schaltflächen vom System nicht ordnungsgemäß aktualisiert. Wenn Sie die Nachricht mit dem propsheet-""-"" * [**\_ twizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) "-Makro senden, wird Sie gepostet. Zu einem beliebigen Zeitpunkt können Sie **SendMessage** zum Senden von **PSM- \_** Setup Schaltflächen verwenden.

Assistenten zeigen unter jeder Seite entweder drei oder vier Schaltflächen an. Diese Meldung wird verwendet, um anzugeben, welche Schaltflächen aktiviert sind. Assistenten werden normalerweise **zurück**, **Abbrechen** und entweder eine Schaltfläche " **weiter** " oder " **Fertig** stellen" angezeigt. Sie aktivieren in der Regel nur die Schaltfläche " **weiter** " für die Willkommensseite, " **Next** " und " **Back** " für innere Seiten und " **zurück** " und " **Fertig** " für die Seite Die Schaltfläche **Abbrechen** ist immer aktiviert. Normalerweise wird die Schaltfläche "weiter" durch das Festlegen von "pswizb \_ Finish" oder "pswizb \_ disabledfinish" durch eine Schaltfläche   Wenn Sie die Schaltflächen **weiter** und **Fertig** stellen gleichzeitig anzeigen möchten, legen \_ Sie beim Erstellen des Assistenten das Flag PSH wizardhasfinish im **dwFlags** -Member der [**propsheeder**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) -Struktur des Assistenten fest. Auf jeder Seite werden dann alle vier Schaltflächen angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

