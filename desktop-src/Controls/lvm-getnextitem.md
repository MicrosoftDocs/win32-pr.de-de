---
title: LVM_GETNEXTITEM Meldung (kommstrg. h)
description: Sucht nach einem Listen Ansichts Element, das über die angegebenen Eigenschaften verfügt und die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetNextItem-Makros senden.
ms.assetid: 2d458f12-b9d3-4b9e-bcb4-927c14c16537
keywords:
- Windows-Steuerelemente für LVM_GETNEXTITEM Meldung
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c4282ebf3572587dd5c8b8b3df1906a51a920e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956988"
---
# <a name="lvm_getnextitem-message"></a>LVM \_ GetNextItem-Meldung

Sucht nach einem Listen Ansichts Element, das über die angegebenen Eigenschaften verfügt und die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, mit dem mit der Suche begonnen werden soll, oder-1, um das erste Element zu finden, das mit den angegebenen Flags übereinstimmt. Das angegebene Element selbst wird von der Suche ausgeschlossen.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Beziehung zu dem in *wParam* angegebenen Element an. Dies kann eine oder eine Kombination der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Sucht nach Index.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **\_ alle "lvni**</dt> "<dt></dt> </dl>                               | Sucht nach einem nachfolgenden Element nach dem Index, dem Standardwert.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **\_ vorherige "lvni**</dt> "<dt></dt> </dl>                | **Windows Vista und höher:** Sucht nach einem Element, das vor dem in *wParam* angegebenen Element geordnet ist. Das "lvni Previous"- \_ Flag ist nicht direktional (in \_ der obigen Version wird das oben positionierte Element gefunden, während "lvni \_ Previous" das zuvor geordnete Element findet). Das "lvni Previous"- \_ Flag kehrt im Grunde die Logik der Suche um, die von den **LVM \_ GetNextItem** -oder [**LVM \_ getnextitemindex**](lvm-getnextitemindex.md) -Nachrichten durchgeführt wird.<br/> |
| <dl> <dt></dt><dt>Sucht nach physischer Beziehung zum Index des Elements, an dem die Suche beginnen soll.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **\_ oben genannte lvni**</dt><dt></dt> </dl>                         | Sucht nach einem Element, das über dem angegebenen Element liegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> nach <dt> **\_ stehende lvni**</dt><dt></dt> </dl>                         | Sucht nach einem Element unterhalb des angegebenen Elements.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **lvni \_ ToLeft**</dt><dt></dt> </dl>                      | Sucht auf der linken Seite des angegebenen Elements nach einem Element.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **lvni- \_ ToRight**</dt><dt></dt> </dl>                   | Sucht nach einem Element auf der rechten Seite des angegebenen Elements.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **lvni- \_ directionmask**</dt><dt></dt> </dl> | **Windows Vista und höher:** Eine direktionale flagmaske mit folgendem Wert: "lvni" oberhalb von "lvni" unterhalb von " \_ \| \_ \| lvni \_ ToLeft \| lvni \_ ToRight".<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Der Status des zu suchenden Elements kann mit einer oder einer Kombination der folgenden Werte angegeben werden:</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **lvni- \_ Ausschneiden**</dt><dt></dt> </dl>                               | Für das Element wurde das [**LVIS- \_ Ausschneide**](list-view-item-states.md) Zustands Flag festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> " <dt> **lvni \_**</dt> " wurde beendet.<dt></dt> </dl>       | Für das Element wurde das LVIS-Flag " [**\_ drophilited**](list-view-item-states.md) State" festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **lvni mit \_ Fokus**</dt><dt></dt> </dl>                   | Für das Element wurde das [**LVIS- \_ fokussierte**](list-view-item-states.md) Statusflag festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> von <dt> **lvni \_ ausgewählt**</dt><dt></dt> </dl>                | Für das Element wurde das LVIS-Flag für den [**\_ ausgewählten**](list-view-item-states.md) Zustand festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **lvni- \_ Statusfrage**</dt><dt></dt> </dl>             | **Windows Vista und höher:** Eine Statusflags-Maske mit dem folgenden Wert: mit dem folgenden Wert: mit dem Ziel "lvni- \_ Fokus \| \_ \| \_ \| \_ .<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Sucht nach Darstellung von Elementen oder nach Gruppe</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **lvni \_ visibleorder**</dt><dt></dt> </dl>    | **Windows Vista und höher:** Durchsuchen Sie die sichtbare Reihenfolge.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **lvni \_ visibleonly**</dt><dt></dt> </dl>       | **Windows Vista und höher:** Durchsuchen Sie die sichtbaren Elemente.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> " <dt> **lvni \_ samegrouponly**</dt> "<dt></dt> </dl> | **Windows Vista und höher:** Durchsuchen der aktuellen Gruppe.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt></dt><dt>Wenn für ein Element nicht alle angegebenen Statusflags festgelegt sind, wird die Suche mit dem nächsten Element fortgesetzt.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des nächsten Elements zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die folgenden Flags, die nur mit Windows Vista verwendet werden, sich gegenseitig von anderen verwendeten Flags ausschließen: "lvni \_ visibleonly", "lvni \_ samegrouponly", "lvni \_ visibleorder", "lvni \_ directionmask" und "lvni \_ Status".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





