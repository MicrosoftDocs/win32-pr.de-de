---
title: LVM_SETITEMCOUNT Meldung (kommstrg. h)
description: Bewirkt, dass das Listenansicht-Steuerelement Arbeitsspeicher für die angegebene Anzahl von Elementen zuweist oder die virtuelle Anzahl von Elementen in einem Steuerelement für die virtuelle Listenansicht festlegt.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- Windows-Steuerelemente für LVM_SETITEMCOUNT Meldung
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103227"
---
# <a name="lvm_setitemcount-message"></a>LVM- \_ Nachricht

Bewirkt, dass das Listenansicht-Steuerelement Arbeitsspeicher für die angegebene Anzahl von Elementen zuweist oder die virtuelle Anzahl von Elementen in einem Steuerelement für die [virtuelle Listenansicht](list-view-controls-overview.md)festlegt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der Elemente, die das Listenansicht-Steuerelement letztendlich enthalten wird.

</dd> <dt>

*lParam* 
</dt> <dd>

[Version 4,70](common-control-versions.md). Werte, die das Verhalten des Listenansicht-Steuer Elements nach dem Zurücksetzen der Element Anzahl angeben. Dieser Wert kann eine Kombination folgender Werte sein:



| Wert                                                                                                                                                                                    | Bedeutung                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**lvsicf \_ noinvalidateall**</dt> </dl> | Das Listenansicht-Steuerelement wird nicht neu gezeichnet, es sei denn, die betroffenen Elemente sind aktuell in der Ansicht.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**lvsicf \_ NoScroll**</dt> </dl>                      | Das Listenansicht-Steuerelement ändert die Bild Lauf Position nicht, wenn die Element Anzahl geändert wird.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Wie der Arbeitsspeicher zugewiesen wird, hängt davon ab, wie das Listenansicht-Steuerelement erstellt wurde. Sie können diese Nachricht explizit senden oder das [**ListView- \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) /ListView-oder [**ListView \_ -/ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) -Makro verwenden. Weitere Informationen finden Sie unter [virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).

Wenn das Listenansicht-Steuerelement ohne den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil erstellt wurde, bewirkt das Senden dieser Nachricht, dass das Steuerelement seine internen Datenstrukturen für die angegebene Anzahl von Elementen zuweist. Dadurch wird verhindert, dass das-Steuerelement die Datenstrukturen jedes Mal zuordnen muss, wenn ein Element hinzugefügt wird.

Wenn das Listenansicht-Steuerelement mit dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil (eine virtuelle Listenansicht) erstellt wurde, wird beim Senden dieser Nachricht die virtuelle Anzahl der im Steuerelement enthaltenen Elemente festgelegt.

Der *LPARAM* -Parameter ist nur für Listenansicht-Steuerelemente vorgesehen, die den [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) -und [**LVS- \_ Bericht**](list-view-window-styles.md) oder [**LVS- \_ Listen**](list-view-window-styles.md) Stile verwenden.

Wenn es sich bei der allgemeinen Steuerelement Listenansicht um eine virtualisierte Listenansicht ([**LVS-Besitzer \_ Daten**](list-view-window-styles.md)) handelt, gibt es in der Listenansicht einen Grenzwert von 100 Millionen Elementen. In diesem Szenario gibt **LVM " \_ sstitemcount** " den Wert "false" zurück, wenn er einen *wParam* -Wert von 100.000.001 hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

