---
description: Ruft eine globale shelleinstellung ab.
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: IShellDispatch4. GetSetting-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 755ee1d2bbd5026b1cc3ca165649e0fcb4ab20ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977985"
---
# <a name="ishelldispatch4getsetting-method"></a>IShellDispatch4. GetSetting-Methode

Ruft eine globale shelleinstellung ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lsetting* \[ in\]
</dt> <dd>

Type: **Long**

Ein-Wert, der die abzurufende aktuelle shelleinstellung angibt. In jedem-Befehl kann nur eine Einstellung abgerufen werden. Die folgenden Werte werden von dieser Methode erkannt.

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ Autocheckselect** (0x00800000)


</dt> <dd>

**Windows Vista und** höher. Der Status der Option **Kontrollkästchen zum Auswählen von Elementen verwenden** . Diese Option wird automatisch aktiviert, wenn für das System ein Stift Eingabegerät konfiguriert ist.

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ Desktophtml** (0x00000200)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ Dontprettypath** (0x00000800)


</dt> <dd>

Der Status der Option **alle Großbuchstaben zulassen** . Ab Windows Vista ist diese Ordner Option nicht mehr verfügbar.

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ Doubleclickinwebview** (0x00000080)


</dt> <dd>

Der Zustand des **Doppelklick-Elements, um ein Element (mit einem Mausklick ausgewählt) zu öffnen** .

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ Filter** (0x00010000 bis)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ Hiddenfileexts** (0x00000004)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ Hideicons** (0x00004000)


</dt> <dd>

Der Status der Symbol Anzeige in der Listenansicht von Windows-Explorer. Wenn diese Option aktiviert ist, werden keine Symbole in der Listenansicht angezeigt.

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ Iconsonly** (0x01000000)


</dt> <dd>

**Windows Vista und** höher. Der Status des anzeigen Amens wird in der Listenansicht von Windows-Explorer angezeigt. Wenn diese Option aktiviert ist, werden Symbole in der Listenansicht angezeigt, aber keine anzeigen Amen.

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ Mapnetdrvbutton** (0x00001000)


</dt> <dd>

Der Status der **Schaltfläche Zuordnungs Netzwerklaufwerk anzeigen in der Symbol** leisten Option. Ab Windows Vista steht diese Option nicht mehr zur Verfügung.

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ Noconfirmrecycle** (0x00008000)


</dt> <dd>

Der Status der Option zum Anzeigen von **Lösch Dialogfeld** für den Papierkorb.

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ Nonetcrawlen** (0x00100000)


</dt> <dd>

Der Status der Option **Netzwerkordner und Drucker automatisch suchen** . Ab Windows Vista steht diese Option nicht mehr zur Verfügung.

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ Sepprocess** (0x00080000)


</dt> <dd>

Der Zustand der **Fenster "Ordner starten" in einer separaten Prozess** Option.

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ Serveradminui** (0x00000004)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ Showallobjects** (0x00000001)


</dt> <dd>

Der Status der ausgeblendeten **Dateien und Ordner** .

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ ShowAttribCol** (0x00000100)


</dt> <dd>

Der Status der Option **Dateiattribute in Detail Ansicht anzeigen** . Ab Windows Vista steht diese Option nicht mehr zur Verfügung.

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ Showcompcolor** (0x00000008)


</dt> <dd>

Der Status der Option **verschlüsselte oder komprimierte NTFS-Dateien in Farbe anzeigen** .

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ Showextensions** (0x00000002)


</dt> <dd>

Der Status der Option **Erweiterungen für bekannte Dateitypen ausblenden** .

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ ShowInfoTip** (0x00002000)


</dt> <dd>

Der Status der Option **Popup Beschreibung für Ordner und Desktop Elemente anzeigen** .

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ Showstartpage** (0x00400000)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ ShowSuperHidden** (0x00040000)


</dt> <dd>

Der Status der Option **geschützte Betriebssystemdateien ausblenden** .

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ Showsysfiles** (0x00000020)


</dt> <dd>

Der Status der ausgeblendeten **Dateien und Ordner** . In Windows Vista und höher entspricht dies SSF \_ showallobjects. In Windows-Versionen vor Windows Vista bezog sich dieser Wert auf den Zustand der Option nicht ausgeblendete **Dateien und Ordner anzeigen** .

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ Showtypeoverlay** (0x02000000)


</dt> <dd>

**Windows Vista und** höher. Der Status des **Symbols für die Anzeige Datei in der Miniatur** Ansicht. Wenn diese Option aktiviert ist, wird eine Dateityp Überlagerung angewendet, wenn eine Datei eine Miniaturansicht bereitstellt.

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SortColumns** (0x00000010)


</dt> <dd>

Nicht verwendet.

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ Startpanelon** (0x00200000)


</dt> <dd>

Der Status der Anzeigeoption von Windows XP, die zwischen dem Windows XP-Stil und dem klassischen Stil auswählt. Ab Windows Vista steht diese Option nicht mehr zur Verfügung.

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WebView** (0x00020000)


</dt> <dd>

Der Zustand der **Anzeige als webansichts Option**. Ab Windows Vista steht diese Option nicht mehr zur Verfügung.

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)


</dt> <dd>

Der Status der **klassischen Stil** Option. Ab Windows Vista steht diese Option nicht mehr zur Verfügung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **Variant \_ bool \** _

Legen Sie auf _ *true** fest, wenn die Einstellung vorhanden ist. andernfalls **false**.

### <a name="vb"></a>VB

Typ: **Variant \_ bool \** _

Legen Sie auf _ *true** fest, wenn die Einstellung vorhanden ist. andernfalls **false**.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **GetSetting** für JScript, VBScript und Visual Basic veranschaulicht.

JScript


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



VBScript


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
</script>
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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6,0 oder höher)</dt> </dl> |



 

 




