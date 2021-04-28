---
description: 'Shell.GetSetting-Methode: Ruft eine globale Shelleinstellung ab.'
ms.assetid: 3E8C7C6A-5696-4756-B4BF-902FA2420AE9
title: Shell.GetSetting-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: dc8fe6277208808ad5f5b182f3eee416daf4a5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083738"
---
# <a name="shellgetsetting-method"></a>Shell.GetSetting-Methode

Ruft eine globale Shelleinstellung ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.GetSetting(
  lSetting
)
```


```VB

Shell.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lSetting* \[ In\]
</dt> <dd>

Typ: **long**

Ein -Wert, der die aktuelle abzurufende Shelleinstellung angibt. In jedem Aufruf kann nur eine Einstellung abgerufen werden. Die folgenden Werte werden von dieser Methode erkannt.

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)


</dt> <dd>

**Windows Vista und höher.** Der Status der Option **Elemente mithilfe der Kontrollkästchen** auswählen. Diese Option wird automatisch aktiviert, wenn für das System ein Stifteingabegerät konfiguriert ist.

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)


</dt> <dd>

Der Status der Option **Alle Großbuchstaben zulassen.** Ab Windows Vista ist diese Ordneroption nicht mehr verfügbar.

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)


</dt> <dd>

Der Status der Option **Doppelklicken, um ein Element zu öffnen (einfaches Klicken zum Auswählen).**

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)


</dt> <dd>

Der Status des Symbols, der in der listenansicht Windows-Explorer angezeigt wird. Wenn diese Option aktiv ist, werden in der Listenansicht keine Symbole angezeigt.

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)


</dt> <dd>

**Windows Vista und höher.** Der Status des Anzeigenamens, der in der Windows-Explorer Listenansicht angezeigt wird. Wenn diese Option aktiv ist, werden Symbole in der Listenansicht angezeigt, Anzeigenamen jedoch nicht.

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)


</dt> <dd>

Der Status der **Schaltfläche Kartennetzwerklaufwerk anzeigen in der Symbolleistenoption.** Ab Windows Vista ist diese Option nicht mehr verfügbar.

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)


</dt> <dd>

Der Status der **Bestätigungsdialogoption Löschbestätigung anzeigen** des Papierkorb.

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)


</dt> <dd>

Der Status der Option **Automatisch nach Netzwerkordnern und Druckern suchen.** Ab Windows Vista ist diese Option nicht mehr verfügbar.

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)


</dt> <dd>

Der Status der **Ordnerfenster in einem separaten Prozess starten.**

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)


</dt> <dd>

Der Status der Option **Ausgeblendete Dateien und** Ordner.

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)


</dt> <dd>

Der Status der Option **Dateiattribute in Detailansicht** anzeigen. Ab Windows Vista ist diese Option nicht mehr verfügbar.

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)


</dt> <dd>

Der Status der Option **Verschlüsselte oder komprimierte NTFS-Dateien in Farbe** anzeigen.

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ SHOWEXTENSIONS** (0x00000002)


</dt> <dd>

Der Status der Option **Erweiterungen für bekannte Dateitypen ausblenden.**

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)


</dt> <dd>

Der Status der Option **Popupbeschreibung für Ordner** und Desktopelemente anzeigen.

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ SHOWSTARTPAGE** (0x00400000)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)


</dt> <dd>

Der Status der Option **Geschützte Betriebssystemdateien ausblenden.**

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)


</dt> <dd>

Der Status der Option **Ausgeblendete Dateien und** Ordner. In Windows Vista und höher entspricht dies SSF \_ SHOWALLOBJECTS. In Windows-Versionen vor Windows Vista wurde dieser Wert auf den Status der Option **Ausgeblendete** Dateien und Ordner nicht anzeigen verwiesen.

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)


</dt> <dd>

**Windows Vista und höher.** Der Status der Option **Dateisymbol für Miniaturansichten** anzeigen. Wenn diese Option aktiv ist, wird eine Dateitypüberlagerung angewendet, wenn eine Datei eine Miniaturansichtsdarstellung liefert.

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)


</dt> <dd>

Der Status der Windows XP-Anzeigeoption, die zwischen dem Windows XP-Stil und dem klassischen Stil auswählt. Ab Windows Vista ist diese Option nicht mehr verfügbar.

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WEBVIEW** (0x00020000)


</dt> <dd>

Der Status der **Option Als Webansicht anzeigen.** Ab Windows Vista ist diese Option nicht mehr verfügbar.

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)


</dt> <dd>

Der Status der Option **"Klassischer Stil".** Ab Windows Vista ist diese Option nicht mehr verfügbar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **VARIANT \_ BOOL \***

Legen Sie auf **TRUE** fest, wenn die Einstellung vorhanden ist. andernfalls **FALSE.**

### <a name="vb"></a>VB

Typ: **VARIANT \_ BOOL \***

Legen Sie auf **TRUE** fest, wenn die Einstellung vorhanden ist. andernfalls **FALSE.**

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **GetSetting** für JScript, VBScript und Visual Basic.

Jscript:


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6.0 oder höher)</dt> </dl> |



 

 




