---
description: Wird von der SHGetSetSettings-Funktion verwendet, um anzugeben, welche Member der SHELLSTATE-Struktur festgelegt oder wiederholt werden sollen.
title: SSF-Konstanten (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2a883110-fdc3-4451-9e47-e58894600e3b
api_name:
- SSF_SHOWALLOBJECTS
- SSF_SHOWEXTENSIONS
- SSF_HIDDENFILEEXTS
- SSF_SERVERADMINUI
- SSF_SHOWCOMPCOLOR
- SSF_SORTCOLUMNS
- SSF_SHOWSYSFILES
- SSF_DOUBLECLICKINWEBVIEW
- SSF_SHOWATTRIBCOL
- SSF_DESKTOPHTML
- SSF_WIN95CLASSIC
- SSF_DONTPRETTYPATH
- SSF_MAPNETDRVBUTTON
- SSF_SHOWINFOTIP
- SSF_HIDEICONS
- SSF_NOCONFIRMRECYCLE
- SSF_FILTER
- SSF_WEBVIEW
- SSF_SHOWSUPERHIDDEN
- SSF_SEPPROCESS
- SSF_NONETCRAWLING
- SSF_STARTPANELON
- SSF_SHOWSTARTPAGE
- SSF_AUTOCHECKSELECT
- SSF_ICONSONLY
- SSF_SHOWTYPEOVERLAY
- SSF_SHOWSTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c022b1d93cb411f0cce73822a47f2d8f85b30e8093bbe2064fb3c50eab5c4870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967939"
---
# <a name="ssf-constants"></a>SSF-Konstanten

Wird von der [**SHGetSetSettings-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings) verwendet, um anzugeben, welche Member der [**SHELLSTATE-Struktur**](/windows/win32/api/shlobj_core/ns-shlobj_core-shellstatea) festgelegt oder wiederholt werden sollen.

<dl> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Das **fShowAllObjects-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Das **fShowExtensions-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Wird nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Wird nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Das **fShowCompColor-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Die **Member lParamSort** **und iSortDirection** werden angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Das **fShowSysFiles-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Das **fDoubleClickInWebView-Mitglied** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Das **fShowAttribCol-Member** wird angefordert.

**Windows Vista:** Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Das **fDesktopHTML-Member** wird angefordert. Set ist nicht verfügbar. Aktivieren Sie stattdessen für Versionen von Windows vor Windows XP Desktop-HTML von [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop). Die Verwendung von **IActiveDesktop** für diesen Zweck wird jedoch für Windows XP und spätere Versionen von Windows nicht empfohlen und ist in Windows Vista veraltet.


</dt> </dl> </dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Der **fWin95Classic-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Das **fDontPrettyPath-Mitglied** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Das **fMapNetDrvBtn-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Das **fShowInfoTip-Element** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**\_SSF-HIDEICONS**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Das **fHideIcons-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Das **fNoConfirmRecycle-Mitglied** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF-FILTER \_**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Das **fFilter-Member** wird angefordert.

**Windows Vista:** Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**\_SSF-WEBVIEW**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Das **fWebView-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Das **fShowSuperHidden-Mitglied** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Das **fSepProcess-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



**Windows XP und höher.** Der **fNoNetCrawling-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



**Windows XP und höher.** Das **fStartPanelOn-Element** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Wird nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



**Windows Vista und höher.** Das **fAutoCheckSelect-Mitglied** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**\_SSF-SYMBOLEONLY**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



**Windows Vista und höher.** Das **fIconsOnly-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



**Windows Vista und höher.** Das **fShowTypeOverlay-Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTATUSBAR"></span><span id="ssf_showstatusbar"></span>**SSF \_ SHOWSTATUSBAR**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



**Windows 8 und höher:** Das **fShowStatusBar-Member** wird angefordert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
