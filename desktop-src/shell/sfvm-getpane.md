---
description: Sfvm \_ GetPane kann geändert oder nicht verfügbar sein.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: SFVM_GETPANE Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960086"
---
# <a name="sfvm_getpane-message"></a>Sfvm \_ GetPane-Nachricht

\[**Sfvm \_ "GetPane** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Ermöglicht dem Rückruf Objekt, den Status Leistenbereich bereitzustellen, in dem die Internet Zonen Informationen angezeigt werden. Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*paneid* \[ in\]
</dt> <dd>

ID des angeforderten Bereichs. Dabei handelt es sich normalerweise um \_ eine Bereichs Zone, bei der es sich um einen der folgenden Werte handeln kann.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**Bereich " \_ None"**


</dt> <dd>

Kein Bereich.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**\_Bereichs Zone**


</dt> <dd>

Der Bereich "Internet Zone".

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**Bereich \_ Offline**


</dt> <dd>

Der Offline-Bereich.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**Bereichs \_ Drucker**


</dt> <dd>

Der Druckanzeige Bereich.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**Bereich- \_ SSL**


</dt> <dd>

Der SSL-Bereich.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**Bereichs \_ Navigation**


</dt> <dd>

Der Navigationsbereich.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**Bereichs Status \_**


</dt> <dd>

Der Bereich der Statusanzeige.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**\_Datenschutz im Bereich**


</dt> <dd>

Der Datenschutz Indikator Bereich.

</dd> </dl> </dd> <dt>

 Bereich \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein **DWORD** , das die Bereichs Nummer enthält.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
