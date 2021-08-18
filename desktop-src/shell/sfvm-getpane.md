---
description: SFVM \_ GETPANE kann geändert oder nicht verfügbar sein.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: SFVM_GETPANE Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef936d4218c29c8d0574e97b8de73c1a0d54f4d62df7dba4f43f371bfeaf95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968669"
---
# <a name="sfvm_getpane-message"></a>SFVM \_ GETPANE-Nachricht

\[**SFVM \_ GETPANE** steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Ermöglicht es dem Rückrufobjekt, den Statusleistenbereich bereitzustellen, in dem die Informationen zur Internetzone angezeigt werden sollen. Wird von [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*paneID* \[ In\]
</dt> <dd>

ID des angeforderten Bereichs. Dies ist normalerweise PANE \_ ZONE, kann aber einer der folgenden Werte sein.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**BEREICH \_ KEINE**


</dt> <dd>

Kein Bereich.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**\_BEREICHSZONE**


</dt> <dd>

Der Bereich Internetzone.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**\_BEREICH OFFLINE**


</dt> <dd>

Der Offlinebereich.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**\_BEREICHSDRUCKER**


</dt> <dd>

Der Bereich für die Druckanzeige.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE \_ SSL**


</dt> <dd>

Der Bereich SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**NAVIGATION IM BEREICH \_**


</dt> <dd>

Der Navigationsbereich.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**\_BEREICHSFORTSCHRITT**


</dt> <dd>

Der Statusanzeigebereich.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**\_BEREICH "DATENSCHUTZ"**


</dt> <dd>

Der Bereich "Datenschutzindikator".

</dd> </dl> </dd> <dt>

*Bereich* \[ out\]
</dt> <dd>

Zeiger auf ein **DWORD** mit der Bereichsnummer.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
