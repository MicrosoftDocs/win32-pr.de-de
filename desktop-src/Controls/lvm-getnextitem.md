---
title: LVM_GETNEXTITEM (Commctrl.h)
description: Sucht nach einem Listenansichtselement, das über die angegebenen Eigenschaften verfügt und die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetNextItem-Makros senden.
ms.assetid: 2d458f12-b9d3-4b9e-bcb4-927c14c16537
keywords:
- LVM_GETNEXTITEM der Windows Steuerelemente
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
ms.openlocfilehash: 40e8e6fdf068f06176d6965a2fb885b349a74ea5cde73c5952d16d7c76512ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002560"
---
# <a name="lvm_getnextitem-message"></a>LVM \_ GETNEXTITEM-Nachricht

Sucht nach einem Listenansichtselement, das über die angegebenen Eigenschaften verfügt und die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetNextItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Elements, mit dem die Suche beginnen soll, oder -1, um das erste Element zu finden, das den angegebenen Flags entspricht. Das angegebene Element selbst wird von der Suche ausgeschlossen.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die Beziehung zu dem in *wParam angegebenen Element an.* Dies kann eine oder eine Kombination der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Sucht nach Index.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ ALL**</dt><dt></dt> </dl>                               | Sucht nach einem nachfolgenden Element nach Index, dem Standardwert.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ PREVIOUS**</dt><dt></dt> </dl>                | **Windows Vista und höher:** Sucht nach einem Element, das vor dem in wParam angegebenen *Element geordnet ist.* Das LVNI PREVIOUS-Flag ist nicht direktional (LVNI ABOVE findet das oben positionierte Element, während LVNI PREVIOUS das zuvor \_ \_ geordnete Element \_ findet.) Das LVNI PREVIOUS-Flag kehrt im Grunde die Logik der Suche um, die von \_ **den LVM \_ GETNEXTITEM-** oder [**LVM \_ GETNEXTITEMINDEX-Nachrichten ausgeführt**](lvm-getnextitemindex.md) wird.<br/> |
| <dl> <dt></dt><dt>Sucht nach physischer Beziehung zum Index des Elements, an dem die Suche beginnen soll.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ OBEN**</dt><dt></dt> </dl>                         | Sucht nach einem Element, das sich über dem angegebenen Element befindet.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ UNTEN**</dt><dt></dt> </dl>                         | Sucht nach einem Element unterhalb des angegebenen Elements.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ TOLEFT**</dt><dt></dt> </dl>                      | Sucht nach einem Element links vom angegebenen Element.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ TORIGHT**</dt><dt></dt> </dl>                   | Sucht nach einem Element rechts vom angegebenen Element.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista und höher:** Eine direktionale Flagmaske mit folgendem Wert: LVNI \_ ABOVE \| LVNI \_ BELOW \| LVNI \_ TOLEFT \| LVNI \_ TORIGHT.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Der Zustand des zu suchenden Elements kann mit</dt> einem oder einer Kombination der folgenden Werte angegeben werden: </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ CUT**</dt><dt></dt> </dl>                               | Für das Element ist das [**LVIS \_ CUT-Zustandsflag**](list-view-item-states.md) festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | Für das Element ist das [**LVIS \_ DROPHILITED-Zustandsflag**](list-view-item-states.md) festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **\_ LVNI-FOKUS**</dt><dt></dt> </dl>                   | Für das Element ist das [**LVIS \_ FOCUSED-Zustandsflag**](list-view-item-states.md) festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ SELECTED**</dt><dt></dt> </dl>                | Für das Element ist das [**LVIS \_ SELECTED-Statusflag**](list-view-item-states.md) festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista und höher:** Eine Zustandsflagmaske mit folgendem Wert: LVNI \_ FOCUSED \| LVNI \_ SELECTED \| LVNI CUT \_ \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Suchen nach Darstellung von Elementen oder nach Gruppe</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista und höher:** Suchen Sie die sichtbare Reihenfolge.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista und höher:** Durchsuchen Sie die sichtbaren Elemente.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista und höher:** Durchsuchen Sie die aktuelle Gruppe.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt></dt><dt>Wenn für ein Element nicht alle angegebenen Zustandsflags</dt> festgelegt sind, wird die Suche mit dem nächsten Element fortgesetzt. </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index des nächsten Elements zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass die folgenden Flags, die nur mit Windows Vista verwendet werden, sich gegenseitig von anderen flags ausschließen, die verwendet werden: LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK und LVNI \_ STATEMASK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





