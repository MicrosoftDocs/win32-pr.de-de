---
title: TVM_GETNEXTITEM Meldung (Commctrl.h)
description: Ruft das Strukturansichtselement ab, das die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit senden, indem Sie das TreeView \_ GetNextItem-Makro verwenden.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- TVM_GETNEXTITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dbbd39ca347bcf1084ddfaa46c997cc5c4e5dd4d52250136a230dd834ac836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698680"
---
# <a name="tvm_getnextitem-message"></a>TVM \_ GETNEXTITEM-Nachricht

Ruft das Strukturansichtselement ab, das die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit senden, indem Sie das [**TreeView \_ GetNextItem-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag, das das abzurufende Element angibt. Dieser Parameter kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**TVGN \_ CARET**</dt> </dl>                               | Ruft das aktuell ausgewählte Element ab. Sie können das [**TreeView \_ GetSelection-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**TVGN \_ CHILD**</dt> </dl>                               | Ruft das erste untergeordnete Element des elements ab, das durch den *Hitem-Parameter* angegeben wird. Sie können das [**TreeView \_ GetChild-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**TVGN \_ DROPHILITE**</dt> </dl>                | Ruft das Element ab, das das Ziel eines Drag & Drop-Vorgangs ist. Sie können das [**\_ TreeView-Makro GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**TVGN \_ FIRSTVISIBLE**</dt> </dl>          | Ruft das erste Element ab, das im Strukturansichtsfenster sichtbar ist. Sie können das [**TreeView \_ GetFirstVisible-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**TVGN \_ LASTVISIBLE**</dt> </dl>             | [Version 4.71.](common-control-versions.md) Ruft das letzte erweiterte Element in der Struktur ab. Dadurch wird nicht das letzte im Strukturansichtsfenster sichtbare Element abgerufen. Sie können das [**TreeView \_ GetLastVisible-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) verwenden, um diese Nachricht zu senden.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ NEXT**</dt> </dl>                                  | Ruft das nächste nebengeordnete Element ab. Sie können das [**TreeView \_ GetNextSibling-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**TVGN \_ NEXTSELECTED**</dt> </dl>          | **Windows Vista und höher.** Ruft das folgende ausgewählte Element ab. Sie können das [**TreeView \_ GetNextSelected-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**TVGN \_ NEXTVISIBLE**</dt> </dl>             | Ruft das nächste sichtbare Element ab, das dem angegebenen Element folgt. Das angegebene Element muss sichtbar sein. Verwenden Sie die [**TVM \_ GETITEMRECT-Nachricht,**](tvm-getitemrect.md) um zu bestimmen, ob ein Element sichtbar ist. Sie können das [**\_ TreeView-Makro GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) verwenden, um diese Nachricht zu senden.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**ÜBERGEORDNETEs \_ TVGN**</dt> </dl>                            | Ruft das übergeordnete Element des angegebenen Elements ab. Sie können das [**TreeView \_ GetParent-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ ZURÜCK**</dt> </dl>                      | Ruft das vorherige gleichgeordnete Element ab. Sie können das [**TreeView \_ GetPrevSibling-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**TVGN \_ PREVIOUSVISIBLE**</dt> </dl> | Ruft das erste sichtbare Element ab, das dem angegebenen Element vorangestellt ist. Das angegebene Element muss sichtbar sein. Verwenden Sie die [**TVM \_ GETITEMRECT-Nachricht,**](tvm-getitemrect.md) um zu bestimmen, ob ein Element sichtbar ist. Sie können das [**TreeView \_ GetPrevVisible-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) verwenden, um diese Nachricht zu senden.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**TVGN \_ ROOT**</dt> </dl>                                  | Ruft das oberste oder das erste Element des Strukturansichtssteuerelements ab. Sie können das [**TreeView \_ GetRoot-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) verwenden, um diese Nachricht zu senden. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für ein Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg das Handle für das Element zurück. In den meisten Fällen gibt die Nachricht einen **NULL-Wert** zurück, um einen Fehler anzugeben. Weitere Informationen finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Hinweise

Diese Meldung gibt **NULL** zurück, wenn das abgerufene Element der Stammknoten der Struktur ist. Wenn Sie diese Nachricht beispielsweise mit dem FLAG TVGN PARENT auf einem untergeordneten Element \_ der ersten Ebene des Stammknotens der Strukturansicht verwenden, gibt die Nachricht **NULL** zurück.

Sie können auch eines der folgenden verwandten Makros verwenden:



|                                                               |
|---------------------------------------------------------------|
| [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





