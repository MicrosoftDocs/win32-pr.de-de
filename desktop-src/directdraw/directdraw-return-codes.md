---
title: DirectDraw-Rückgabe Codes (ddraw. h)
description: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70ff2003edc382bac2823235f01f58ffea0d91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870155"
---
# <a name="directdraw-return-codes"></a>DirectDraw-Rückgabe Codes

Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden. In dieser Tabelle sind die Werte aufgelistet, die von allen Methoden der [DirectDraw-Schnittstellen](directdraw-interfaces.md) und [DirectDraw-Funktionen](directdraw-functions.md)zurückgegeben werden können. Eine Liste der Fehlercodes, die von den einzelnen Methoden oder Funktionen zurückgegeben werden können, finden Sie in der Beschreibung der Methode oder Funktion.

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**
</dt> <dd> <dl> <dt>



Die Anforderung wurde erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**dderr \_ alread-initialisiert**
</dt> <dd> <dl> <dt>



Das Objekt wurde bereits initialisiert.


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**dderr \_ bltfastcantclip**
</dt> <dd> <dl> <dt>



Ein directdrawclipperobjekt wird an eine Quell Oberfläche angefügt, die an einen aufzurufenden Befehl der [**IDirectDrawSurface7:: bltfast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) -Methode übergeben wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**dderr \_ cannotattachsurface**
</dt> <dd> <dl> <dt>



Eine Oberfläche kann nicht an eine andere angeforderte Oberfläche angehängt werden.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**dderr \_ cannotdetachsurface**
</dt> <dd> <dl> <dt>



Eine Oberfläche kann nicht von einer anderen angeforderten Oberfläche getrennt werden.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**dderr \_ kankreatedc**
</dt> <dd> <dl> <dt>



Windows kann keine weiteren Geräte Kontexte (DCS) erstellen, oder ein DC hat eine palettenindizierte Oberfläche angefordert, wenn die Oberfläche keine Palette enthielt und der Anzeigemodus nicht palettenindiziert war (in diesem Fall kann DirectDraw keine passende Palette in den DC auswählen).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**dderr- \_ kanduplikat**
</dt> <dd> <dl> <dt>



Primär-und 3D-Oberflächen oder Flächen, die implizit erstellt werden, können nicht dupliziert werden.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**dderr- \_ kanlocksurface**
</dt> <dd> <dl> <dt>



Der Zugriff auf diese Oberfläche wurde abgelehnt, weil versucht wurde, die primäre Oberfläche ohne die Unterstützung der Anzeige Steuerungs Schnittstelle


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**dderr- \_ kanpagelock**
</dt> <dd> <dl> <dt>



Der Versuch, eine Oberfläche zu sperren, ist fehlgeschlagen. Die Seiten Sperre funktioniert nicht auf einer Anzeige Speicher Oberfläche oder einer emulierten primären Oberfläche.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**dderr- \_ kanpageunlock**
</dt> <dd> <dl> <dt>



Der Versuch, eine Oberfläche zu entsperren, ist fehlgeschlagen. Das Entsperren von Seiten funktioniert nicht auf einer Anzeige-oder einer emulierten primären Oberfläche.


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**dderr \_ clipperisusinghwnd**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Clip Liste für ein directdrawclipperobjekt festzulegen, das bereits ein Fenster Handle überwacht.


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**dderr \_ colorkeynotset**
</dt> <dd> <dl> <dt>



Für diesen Vorgang ist kein Quell Farbschlüssel angegeben.


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**dderr \_ currentlynotavail**
</dt> <dd> <dl> <dt>



Zurzeit ist keine Unterstützung verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**dderr \_ ddscapscomplexrequired**
</dt> <dd> <dl> <dt>



Neu bei DirectX 7,0. Die Oberfläche erfordert das komplexe DDSCAPS- \_ Flag.


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**dderr \_ dcalsorycreated**
</dt> <dd> <dl> <dt>



Für diese Oberfläche wurde bereits ein Gerätekontext (DC) zurückgegeben. Für jede Oberfläche kann nur ein DC abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>dderr \_ devicedoesntownsurface**
</dt> <dd> <dl> <dt>



Von einem DirectDraw-Gerät erstellte Oberflächen können nicht direkt von einem anderen DirectDraw-Gerät verwendet werden.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>dderr \_ directdrawalleserycreated**
</dt> <dd> <dl> <dt>



Ein DirectDraw-Objekt, das diesen Treiber darstellt, wurde für diesen Prozess bereits erstellt.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**dderr- \_ Ausnahme**
</dt> <dd> <dl> <dt>



Beim Ausführen des angeforderten Vorgangs ist eine Ausnahme aufgetreten.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**dderr \_ exclusivemu-leseryset**
</dt> <dd> <dl> <dt>



Es wurde versucht, die kooperative Ebene festzulegen, als Sie bereits auf exklusiv festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**dderr \_ abgelaufen**
</dt> <dd> <dl> <dt>



Die Daten sind abgelaufen und daher nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**dderr ( \_ generisch)**
</dt> <dd> <dl> <dt>



Es gibt eine nicht definierte Fehlerbedingung.


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**dderr- \_ heightalign**
</dt> <dd> <dl> <dt>



Die Höhe des bereitgestellten Rechtecks ist kein Vielfaches der erforderlichen Ausrichtung.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**dderr \_ hwndallesset**
</dt> <dd> <dl> <dt>



Das Fenster Handle der Zusammenführung auf der Basis von DirectDraw wurde bereits festgelegt. Sie kann nicht zurückgesetzt werden, während der Prozess Oberflächen oder Paletten erstellt hat.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**dderr \_ hwndsubklassiert**
</dt> <dd> <dl> <dt>



Das Wiederherstellen des Zustands durch DirectDraw wird verhindert, da das Fenster Handle für die Zusammenführung des DirectDraw-Fensters auf Genossenschafts Ebene untergeordnet ist


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**dderr \_ implicitlycreated**
</dt> <dd> <dl> <dt>



Die Oberfläche kann nicht wieder hergestellt werden, da Sie eine implizit erstellte Oberfläche ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**dderr \_ incompatibleprimary**
</dt> <dd> <dl> <dt>



Die primäre Oberflächen Erstellungs Anforderung stimmt nicht mit der vorhandenen primären Oberfläche identisch.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**dderr- \_ invalidcaps**
</dt> <dd> <dl> <dt>



Mindestens eine der an die Rückruffunktion weiter gegebenen Funktions Bits ist falsch.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**dderr \_ invalidcliplist**
</dt> <dd> <dl> <dt>



DirectDraw unterstützt die angegebene Clip Liste nicht.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**dderr \_ invaliddirectdrawguid**
</dt> <dd> <dl> <dt>



Die an die [**directdrawcreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) -Funktion über gegebene Globally Unique Identifier (GUID) ist kein gültiger DirectDraw-Treiber Bezeichner.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**dderr \_ invalidmode**
</dt> <dd> <dl> <dt>



DirectDraw unterstützt den angeforderten Modus nicht.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**dderr- \_ invalidobject**
</dt> <dd> <dl> <dt>



DirectDraw hat einen Zeiger empfangen, der ein ungültiges DirectDraw-Objekt war.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**dderr \_ invalidparametriams**
</dt> <dd> <dl> <dt>



Mindestens ein Parameter, der an die-Methode weitergegeben wurde, ist falsch.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**dderr \_ invalidpixelformat**
</dt> <dd> <dl> <dt>



Das Pixel Format war wie angegeben ungültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**dderr- \_ invalidposition**
</dt> <dd> <dl> <dt>



Die Position des Overlay auf dem Ziel ist nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**dderr \_ InvalidRect**
</dt> <dd> <dl> <dt>



Das angegebene Rechteck war ungültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**dderr \_ invalidstream**
</dt> <dd> <dl> <dt>



Der angegebene Stream enthält ungültige Daten.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**dderr \_ invalidsurfaketype**
</dt> <dd> <dl> <dt>



Die Oberfläche hatte den falschen Typ.


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**dderr \_ lockedoberflächen**
</dt> <dd> <dl> <dt>



Mindestens eine Oberfläche ist gesperrt, wodurch der angeforderte Vorgang fehlgeschlagen ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**dderr \_ MoreData**
</dt> <dd> <dl> <dt>



Es sind mehr Daten verfügbar, als die angegebene Puffergröße enthalten kann.


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**dderr- \_ NEWMODE**
</dt> <dd> <dl> <dt>



Neu bei DirectX 7,0. Wenn [**IDirectDraw7:: startmodetest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) mit dem ddsmt \_ istestrequired-Flag aufgerufen wird, kann dieser Wert zurückgegeben werden, um anzugeben, dass einige oder alle Auflösungen getestet werden können. [**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) gibt diesen Wert zurück, um anzugeben, dass der Test in einen neuen Anzeigemodus gewechselt hat.


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**Dderr \_ NO3D**
</dt> <dd> <dl> <dt>



Es ist keine 3D-Hardware oder Emulation vorhanden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**dderr- \_ noalphahw**
</dt> <dd> <dl> <dt>



Es ist keine Alpha Beschleunigung-Hardware vorhanden oder verfügbar, die den angeforderten Vorgang nicht bewirkt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**dderr \_ noblthw**
</dt> <dd> <dl> <dt>



Es ist kein Bitblock übertragen von Hardware vorhanden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**dderr- \_ nocliplist**
</dt> <dd> <dl> <dt>



Es ist keine Clip Liste verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**dderr- \_ noclipperattached**
</dt> <dd> <dl> <dt>



An das Surface-Objekt ist kein directdrawclipperobjekt angefügt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**dderr \_ nocolor-VHW**
</dt> <dd> <dl> <dt>



Es ist keine Farb Konvertierungs Hardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**dderr \_ nocolorkey**
</dt> <dd> <dl> <dt>



Die Oberfläche verfügt zurzeit nicht über einen Farbschlüssel.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**dderr \_ nocolorkeyhw**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für den Ziel Farbschlüssel.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**dderr \_ nokooperativelevelset**
</dt> <dd> <dl> <dt>



Eine Create-Funktion wurde ohne die [**IDirectDraw7:: setkooperativelevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) -Methode aufgerufen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**dderr- \_ nodc**
</dt> <dd> <dl> <dt>



Für diese Oberfläche wurde nie ein Gerätekontext (DC) erstellt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**dderr \_ noddropshw**
</dt> <dd> <dl> <dt>



Es ist keine DirectDraw-Raster-Operation-Hardware (ROP) verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**dderr \_ nodirectdrawhw**
</dt> <dd> <dl> <dt>



Reine Hardware-DirectDraw-Objekt Erstellung ist nicht möglich. der Treiber unterstützt keine Hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**dderr \_ nodirectdrawsupport**
</dt> <dd> <dl> <dt>



DirectDraw-Unterstützung ist mit dem aktuellen Anzeigetreiber nicht möglich.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**dderr \_ nodriversupport**
</dt> <dd> <dl> <dt>



Neu bei DirectX 7,0. Der Test kann nicht fortgesetzt werden, da der Anzeige Adapter Treiber keine Aktualisierungs Raten auflistet.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**dderr- \_ noemulation**
</dt> <dd> <dl> <dt>



Die Software Emulation ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**dderr \_ noexclusivemode**
</dt> <dd> <dl> <dt>



Der Vorgang erfordert, dass die Anwendung den exklusiven Modus hat, aber die Anwendung hat keinen exklusiven Modus.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**dderr \_ nofliphw**
</dt> <dd> <dl> <dt>



Das Kippen von sichtbaren Oberflächen wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**dderr \_ nofocenwindow**
</dt> <dd> <dl> <dt>



Es wurde versucht, ein Geräte Fenster zu erstellen oder festzulegen, ohne zuvor das Fokus Fenster festzulegen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**dderr- \_ nogdi**
</dt> <dd> <dl> <dt>



Es ist kein GDI vorhanden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**dderr- \_ nohwnd**
</dt> <dd> <dl> <dt>



Die clipperbenachrichtigung erfordert ein Fenster Handle, oder es wurde zuvor kein Fenster Handle als Fenster Handle der kooperativen Ebene festgelegt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**dderr \_ nomipmaphw**
</dt> <dd> <dl> <dt>



Es ist keine MipMap-fähige Textur Zuordnungs Hardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**dderr \_ nomirrorhw**
</dt> <dd> <dl> <dt>



Es ist keine Spiegelungs Hardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**dderr \_ nomonitorinformation**
</dt> <dd> <dl> <dt>



Neu bei DirectX 7,0. Das Testen kann nicht fortgesetzt werden, da dem Monitor keine EDID-Daten zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**dderr \_ nononlocalvidmem**
</dt> <dd> <dl> <dt>



Es wurde versucht, einen nicht lokalen Videospeicher von einem Gerät zuzuordnen, das nicht lokalen Videospeicher nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**dderr \_ nooptimizehw**
</dt> <dd> <dl> <dt>



Das Gerät unterstützt keine optimierten Oberflächen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**dderr \_ nooverlaydest**
</dt> <dd> <dl> <dt>



Die [**IDirectDrawSurface7:: gedeverlayposition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) -Methode wird auf einem Overlay aufgerufen, für das die [**IDirectDrawSurface7:: updateoverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) -Methode nicht aufgerufen wurde, um als Ziel festzulegen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**dderr \_ nooverlayhw**
</dt> <dd> <dl> <dt>



Es ist keine über Lagerungs Hardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**dderr \_ nopaletteattached**
</dt> <dd> <dl> <dt>



An diese Oberfläche ist kein Palettenobjekt angefügt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**dderr \_ nopalettehw**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für 16-oder 256-farbige Paletten.


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**dderr \_ norasterophw**
</dt> <dd> <dl> <dt>



Es ist keine geeignete Raster Betriebs Hardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**dderr \_ norotationhw**
</dt> <dd> <dl> <dt>



Es ist keine Rotations Hardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**dderr \_ nostereohardware**
</dt> <dd> <dl> <dt>



Es ist keine Stereo Hardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**dderr \_ nostretchhw**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für das Stretching.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**dderr- \_ nosurfakeleft**
</dt> <dd> <dl> <dt>



Es ist keine Hardware vorhanden, die Stereo Oberflächen unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**Dderr \_ NOT4BITCOLOR**
</dt> <dd> <dl> <dt>



Das directdrawsurface-Objekt verwendet keine 4-Bit-Farbpalette, und der angeforderte Vorgang erfordert eine 4-Bit-Farbpalette.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**Dderr \_ NOT4BITCOLORINDEX**
</dt> <dd> <dl> <dt>



Das directdrawsurface-Objekt verwendet keine 4-Bit-Farb Index Palette, und der angeforderte Vorgang erfordert eine 4-Bit-Farb Index Palette.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**Dderr \_ NOT8BITCOLOR**
</dt> <dd> <dl> <dt>



Das directdrawsurface-Objekt verwendet keine 8-Bit-Farbpalette, und der angeforderte Vorgang erfordert eine 8-Bit-Farbpalette.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**dderr \_ notaoverlaysurface**
</dt> <dd> <dl> <dt>



Eine Überlagerungs Komponente wird für eine nicht Überlagerungs Oberfläche aufgerufen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**dderr \_ notexturehw**
</dt> <dd> <dl> <dt>



Der Vorgang kann nicht ausgeführt werden, da keine Textur zuordnungshardware vorhanden oder verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**dderr \_ notflippable**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche zu kippen, die nicht gekippt werden kann.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**dderr \_ NotFound**
</dt> <dd> <dl> <dt>



Das angeforderte Element wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**dderr \_ notinitialisiert**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Schnittstellen Methode eines DirectDraw-Objekts aufzurufen, das von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt wurde, bevor das Objekt initialisiert wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**dderr \_ notloaded**
</dt> <dd> <dl> <dt>



Die Oberfläche ist eine optimierte Oberfläche, aber ihr wurde noch kein Arbeitsspeicher zugeordnet.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**dderr nicht \_ gesperrt**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche zu entsperren, die nicht gesperrt war.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**dderr \_ notpagelocked**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche ohne ausstehende Seiten Sperren auf eine Seite zu entsperren.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**dderr \_ notpalettisiert**
</dt> <dd> <dl> <dt>



Die verwendete Oberfläche ist keine palettenbasierte Oberfläche.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**dderr \_ novsynchronw**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für vertikale, leere synchronisierte Vorgänge.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**dderr \_ nozbufferhw**
</dt> <dd> <dl> <dt>



Der Vorgang zum Erstellen eines z-Puffers im Anzeige Speicher oder zum Ausführen einer Bitblock Übertragung (BitBLT) kann nicht ausgeführt werden, da keine Hardwareunterstützung für z-Puffer vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**dderr \_ nozoverlayhw**
</dt> <dd> <dl> <dt>



Die Überlagerungs Flächen können auf der z-Reihenfolge nicht auf z-Reihenfolge basieren, weil die Hardware keine z-Reihenfolge von Überlagerungen unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**dderr- \_ outo**
</dt> <dd> <dl> <dt>



Die für den angeforderten Vorgang erforderliche Hardware wurde bereits zugeordnet.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**dderr- \_ outo-Memory**
</dt> <dd> <dl> <dt>



DirectDraw verfügt nicht über genügend Arbeitsspeicher, um den Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**dderr \_ ouum-videomemory**
</dt> <dd> <dl> <dt>



DirectDraw verfügt nicht über genügend Anzeige Speicher, um den Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**dderr \_ overlappingrects**
</dt> <dd> <dl> <dt>



Die Quell-und Ziel Rechtecke befinden sich auf derselben Oberfläche und überlappen einander.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**dderr \_ overlaycantclip**
</dt> <dd> <dl> <dt>



Die Hardware unterstützt keine abgeschnitten-Überlagerungen.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**dderr \_ overlaycolorkeyonlyoneactive**
</dt> <dd> <dl> <dt>



Es wurde versucht, mehr als einen Farbschlüssel auf einem Overlay zu aktivieren.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**dderr \_ overlaynotvisible**
</dt> <dd> <dl> <dt>



Die [**IDirectDrawSurface7:: gedeverlayposition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) -Methode wurde für ein verborgenes Overlay aufgerufen.


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**dderr \_ palettebusy**
</dt> <dd> <dl> <dt>



Der Zugriff auf diese Palette wird verweigert, da die Palette von einem anderen Thread gesperrt ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**dderr \_ primarysurfacealread yexistiert**
</dt> <dd> <dl> <dt>



Dieser Prozess hat bereits eine primäre Oberfläche erstellt.


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**dderr \_ Regionin Small**
</dt> <dd> <dl> <dt>



Der an die [**idirectdrawclipper:: getcliplist**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) -Methode über gegebene Bereich ist zu klein.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**dderr \_ surfacealsoryattached**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche an eine andere Oberfläche anzufügen, an die Sie bereits angefügt wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**dderr \_ surfacealleserydependent**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche zu einer Abhängigkeit von einer anderen Oberfläche zu machen, von der Sie bereits abhängig ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**dderr \_ surfacebusy**
</dt> <dd> <dl> <dt>



Der Zugriff auf die-Oberfläche wird verweigert, da die Oberfläche von einem anderen Thread gesperrt ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**dderr \_ surfakeisobscgewöhnt**
</dt> <dd> <dl> <dt>



Der Zugriff auf die-Oberfläche wird verweigert, da die Oberfläche verdeckt ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**dderr \_ surfakelost**
</dt> <dd> <dl> <dt>



Der Zugriff auf die-Oberfläche wird verweigert, da der Arbeitsspeicher nicht mehr verfügbar ist. Wenden Sie die [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) -Methode auf dieser Oberfläche an, um den zugeordneten Arbeitsspeicher wiederherzustellen.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**dderr \_ surfakenotattached**
</dt> <dd> <dl> <dt>



Die angeforderte Oberfläche ist nicht angefügt.


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**dderr \_ testabgeschlossen**
</dt> <dd> <dl> <dt>



Neu bei DirectX 7,0. Wenn Sie von der [**IDirectDraw7:: startmodetest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) -Methode zurückgegeben wird, bedeutet dieser Wert, dass kein Test initiiert werden konnte, weil alle für das Testen ausgewählten Auflösungen bereits über Aktualisierungs rateninformationen in der Registrierung verfügen. Wenn Sie von [**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)zurückgegeben wird, bedeutet der Wert, dass DirectDraw einen Aktualisierungs Raten Test abgeschlossen hat.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**dderr \_ -Dienst**
</dt> <dd> <dl> <dt>



Die von DirectDraw angeforderte Höhe ist zu groß.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**dderr-Verzeichnis \_ Größe**
</dt> <dd> <dl> <dt>



Die von DirectDraw angeforderte Größe ist zu groß. Die einzelne Höhe und Breite sind jedoch gültige Größen.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**dderr-Verzeichnis \_ Breite**
</dt> <dd> <dl> <dt>



Die von DirectDraw angeforderte Breite ist zu groß.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**dderr \_ nicht unterstützt**
</dt> <dd> <dl> <dt>



Der Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**dderr \_ unsupportedformat**
</dt> <dd> <dl> <dt>



Das angeforderte Pixel Format wird von DirectDraw nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**dderr \_ unsupportedmask**
</dt> <dd> <dl> <dt>



Die Bitmaske im angeforderten Pixel Format wird von DirectDraw nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**dderr \_ unsupportedmode**
</dt> <dd> <dl> <dt>



Die Anzeige befindet sich zurzeit in einem nicht unterstützten Modus.


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**dderr \_ verticalblankinprogress**
</dt> <dd> <dl> <dt>



Ein vertikaler leerer Vorgang wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**dderr \_ videonotactive**
</dt> <dd> <dl> <dt>



Der Videoport ist nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**dderr \_ wasstilldrawing**
</dt> <dd> <dl> <dt>



Der vorherige BitBLT-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig.


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**dderr-Fehler \_ Modus**
</dt> <dd> <dl> <dt>



Diese Oberfläche kann nicht wieder hergestellt werden, da Sie in einem anderen Modus erstellt wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**dderr- \_ xalign**
</dt> <dd> <dl> <dt>



Das angegebene Rechteck wurde nicht horizontal an einer erforderlichen Grenze ausgerichtet.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

