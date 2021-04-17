---
title: TVM_EXPAND Meldung (kommstrg. h)
description: Die TVM \_ Expand Message erweitert oder reduziert die Liste der untergeordneten Elemente, die dem angegebenen übergeordneten Element zugeordnet sind, sofern vorhanden. Sie können diese Nachricht explizit oder mithilfe des TreeView Expand- \_ Makros senden.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- Windows-Steuerelemente für TVM_EXPAND Meldung
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478486"
---
# <a name="tvm_expand-message"></a>TVM \_ Expand Message

Die **TVM \_ Expand** Message erweitert oder reduziert die Liste der untergeordneten Elemente, die dem angegebenen übergeordneten Element zugeordnet sind, sofern vorhanden. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Aktionsflag. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <dt>**TVE \_ zuklappen**</dt> </dl>                | Reduziert die Liste. <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <dt>**TVE- \_ redusereset**</dt> </dl> | Reduziert die Liste und entfernt die untergeordneten Elemente. Das [**Tvis \_ expandebug**](tree-view-control-item-states.md) State-Flag wird zurückgesetzt. Dieses Flag muss mit dem "TVE Collapse"-Flag verwendet werden \_ .<br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <dt>**TVE \_ erweitern**</dt> </dl>                      | Erweitert die Liste.<br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <dt>**TVE \_ expandpartial**</dt> </dl> | [Version 4,70](common-control-versions.md). Erweitert die Liste teilweise. In diesem Zustand werden die untergeordneten Elemente sichtbar, und das Pluszeichen (+) des übergeordneten Elements, das angibt, dass es erweitert werden kann, wird angezeigt. Dieses Flag muss in Kombination mit dem "TVE expand"-Flag verwendet werden \_ .<br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <dt>**TVE \_ Umschalten**</dt> </dl>                      | Reduziert die Liste, wenn Sie erweitert wird, oder erweitert Sie, wenn Sie reduziert ist.<br/>                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das übergeordnete Element, das erweitert oder reduziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn der Vorgang erfolgreich war, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Das Erweitern eines Knotens, der bereits erweitert ist, gilt als erfolgreicher Vorgang, und [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) gibt einen Wert ungleich 0 (null) zurück. Beim Reduzieren eines Knotens wird 0 zurückgegeben, wenn der Knoten bereits reduziert ist. Andernfalls wird ein Wert ungleich NULL zurückgegeben. Der Versuch, einen Knoten zu erweitern oder zu reduzieren, der keine untergeordneten Elemente hat, wird als Fehler betrachtet, und **SendMessage** gibt NULL zurück

Wenn ein Element erstmalig durch eine **TVM \_** -Erweiterungs Meldung erweitert wird, generiert die Aktion [TVN \_ itemexpandeing](tvn-itemexpanding.md) und [TVN \_ itemexpanded](tvn-itemexpanded.md) -Benachrichtigungs Codes, und das [**Tvis \_**](tree-view-control-item-states.md) -Statusflag des Elements wird festgelegt. Solange dieses Statusflag festgelegt bleibt, generieren nachfolgende **TVM \_ Expand** Messages keine TVN \_ itemexpandor-und TVN \_ itemexpanded-Benachrichtigungen. Um das **Tvis \_ expandedonce** State-Flag zurückzusetzen, müssen Sie eine **TVM- \_** Erweiterungs Meldung mit den \_ festgelegten Flags "TVE Collapse" und "TVE \_ redusereset" senden. Der Versuch, **Tvis \_ expandedonce** explizit festzulegen, führt zu unvorhersehbarem Verhalten.

Der Erweiterungs Vorgang kann fehlschlagen, wenn der Besitzer des TreeView-Steuer Elements den Vorgang als Reaktion auf eine [TVN \_ itemexpandeing](tvn-itemexpanding.md) -Benachrichtigung ablehnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

