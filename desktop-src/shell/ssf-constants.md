---
description: Wird von der shgetsetsettings-Funktion verwendet, um anzugeben, welche Member der shellstate-Struktur festgelegt oder abgerufen werden sollen.
title: SSF-Konstanten (shlobj. h)
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
ms.openlocfilehash: b26ba102ff72caf235a51d3888183ccafba9d639
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994830"
---
# <a name="ssf-constants"></a>SSF-Konstanten

Wird von der [**shgetsetsettings**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings) -Funktion verwendet, um anzugeben, welche Member der [**shellstate**](/windows/win32/api/shlobj_core/ns-shlobj_core-shellstatea) -Struktur festgelegt oder abgerufen werden sollen.

<dl> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF- \_ showallobjects**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Der **fshowallobjects** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF- \_ showextensions**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Der **fshowextensions** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF- \_ hiddenfileexts**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ serveradminui**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF- \_ showcompcolor**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Der **fshowcompcolor** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ sortColumns**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Die Member **lparamsort** und **isortdirection** werden angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF- \_ showsysfiles**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Der **fshowsysfiles** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ doubleclickinwebview**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Der **fdoubleclickinwebview** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ ShowAttribCol**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Der **fshowattribcol** -Member wird angefordert.

**Windows Vista:** Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ desktophtml**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Der **fdesktophtml** -Member wird angefordert. Set ist nicht verfügbar. Aktivieren Sie stattdessen für Windows-Versionen vor Windows XP Desktop-HTML von [**iactivedesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop). Die Verwendung von **iactivedesktop** zu diesem Zweck wird jedoch für Windows XP und höhere Versionen von Windows nicht empfohlen und ist in Windows Vista veraltet.


</dt> </dl> </dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Der **fWin95Classic** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF- \_ dontprettypath**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Der Member " **fdontprettypath** " wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ mapnetdrvbutton**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Der **fmapnetdrvbtn** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF- \_ ShowInfoTip**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Der **fshowinfotip** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF- \_ hideicons**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Der **fhideicons** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF- \_ noconfirm-Wiederverwendung**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Der **fnoconfirmrecycle** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF- \_ Filter**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Der **ffilter** -Member wird angefordert.

**Windows Vista:** Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF- \_ WebView**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Der **fwebview** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ ShowSuperHidden**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Der **fshowsuperhidden** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF- \_ sepprocess**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Der **fsepprocess** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF- \_ nonetcrawlen**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



**Windows XP und** höher. Der **fnonetcrawlen** -Member wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ startpanelon**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



**Windows XP und** höher. Das **fstartpanelon** -Element wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF- \_ showstartpage**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ autocheckselect**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



**Windows Vista und** höher. Das **fautocheckselect** -Element wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF ( \_ iconsonly)**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



**Windows Vista und** höher. Der **Member** wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF- \_ showtypeoverlay**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



**Windows Vista und** höher. Das **fshowtypeoverlay** -Element wird angefordert.


</dt> </dl> </dd> <dt>

<span id="SSF_SHOWSTATUSBAR"></span><span id="ssf_showstatusbar"></span>**SSF- \_ ShowStatusBar**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



**Windows 8 und** höher: der **fshowstatusbar** -Member wird angefordert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
