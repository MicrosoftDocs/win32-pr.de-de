---
title: TVM_GETNEXTITEM Meldung (kommstrg. h)
description: Ruft das Struktur Ansichts Element ab, das die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit senden, indem Sie das TreeView \_ GetNextItem-Makro verwenden.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- Windows-Steuerelemente für TVM_GETNEXTITEM Meldung
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
ms.openlocfilehash: 3099af5e9abcd3e9c144cfc615a12dd2acb0332b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103211"
---
# <a name="tvm_getnextitem-message"></a>TVM \_ GetNextItem-Meldung

Ruft das Struktur Ansichts Element ab, das die angegebene Beziehung zu einem angegebenen Element trägt. Sie können diese Nachricht explizit senden, indem Sie das [**TreeView \_ GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag zum Angeben des abzurufenden Elements. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**Tvgn- \_ Caretzeichen**</dt> </dl>                               | Ruft das aktuell ausgewählte Element ab. Sie können das [**TreeView- \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) -Makro verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**untergeordnetes \_ Tvgn**</dt> </dl>                               | Ruft das erste untergeordnete Element des Elements ab, das durch den *Hitem* -Parameter angegeben wird. Sie können diese Nachricht mit dem [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) -Makro senden.<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**Tvgn \_ drophilite**</dt> </dl>                | Ruft das Element ab, das das Ziel eines Drag & Drop-Vorgangs ist. Sie können das [**TreeView \_ getdrophilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) -Makro verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**Tvgn \_ firstvisible**</dt> </dl>          | Ruft das erste Element ab, das im Struktur Ansichts Fenster sichtbar ist. Sie können das [**TreeView \_ getfirstvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) -Makro verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**Tvgn \_ lastvisible**</dt> </dl>             | [Version 4,71](common-control-versions.md). Ruft das letzte erweiterte Element in der Struktur ab. Dadurch wird das letzte Element, das im Struktur Ansichts Fenster sichtbar ist, nicht abgerufen. Sie können das [**TreeView \_ getlastvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) -Makro verwenden, um diese Nachricht zu senden.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**Tvgn \_ Next**</dt> </dl>                                  | Ruft das nächste neben geordnete Element ab. Sie können das [**TreeView \_ getnextsierend**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) -Makro verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**Tvgn \_ nextselected**</dt> </dl>          | **Windows Vista und höher.** Ruft das folgende ausgewählte Element ab. Sie können das [**TreeView \_ getnextselected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) -Makro verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**Tvgn \_ NextVisible**</dt> </dl>             | Ruft das nächste sichtbare Element ab, das auf das angegebene Element folgt. Das angegebene Element muss sichtbar sein. Verwenden Sie die [**TVM \_ GetItemRect**](tvm-getitemrect.md) -Meldung, um zu bestimmen, ob ein Element sichtbar ist. Sie können das [**TreeView \_ getnextvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) -Makro verwenden, um diese Nachricht zu senden.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**übergeordnetes Tvgn \_**</dt> </dl>                            | Ruft das übergeordnete Element des angegebenen Elements ab. Sie können das [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) -Makro verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**\_Vorheriges Tvgn**</dt> </dl>                      | Ruft das vorherige neben geordnete Element ab. Sie können das [**TreeView \_ getprevsierend**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) -Makro verwenden, um diese Nachricht zu senden.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**Tvgn \_ PreviousVisible**</dt> </dl> | Ruft das erste sichtbare Element ab, das dem angegebenen Element vorangestellt ist. Das angegebene Element muss sichtbar sein. Verwenden Sie die [**TVM \_ GetItemRect**](tvm-getitemrect.md) -Meldung, um zu bestimmen, ob ein Element sichtbar ist. Sie können das [**TreeView \_ getprevvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) -Makro verwenden, um diese Nachricht zu senden.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**Tvgn \_ -Stamm**</dt> </dl>                                  | Ruft das oberste oder erste Element des Strukturansicht-Steuer Elements ab. Sie können das [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) -Makro verwenden, um diese Nachricht zu senden. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für ein Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Element zurück, wenn erfolgreich. In den meisten Fällen gibt die Meldung einen **null** -Wert zurück, um einen Fehler anzugeben. Weitere Informationen finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Bemerkungen

Diese Meldung gibt **null** zurück, wenn das abgerufene Element der Stamm Knoten der Struktur ist. Wenn Sie diese Meldung z. b. mit dem \_ übergeordneten Flag Tvgn auf einem untergeordneten Element der Strukturansicht des Stamm Knotens der Strukturansicht verwenden, gibt die Meldung **null** zurück.

Sie können auch eines dieser verknüpften Makros verwenden:



|                                                               |
|---------------------------------------------------------------|
| [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**TreeView \_ getdrophilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**TreeView \_ getfirstvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**TreeView \_ getlastvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**TreeView \_ getnextsigend**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**TreeView \_ getnextvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**TreeView \_ getprevsierend**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**TreeView \_ getprevvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





