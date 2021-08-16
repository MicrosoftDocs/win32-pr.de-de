---
title: DirectDraw-Rückgabecodes (Ddraw.h)
description: 'DirectDraw-Rückgabecodes: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.'
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
ms.openlocfilehash: 1e937ad9cc32a7837303d535b73b176c7e16f2d0ab0033bf625f629d2d5f7bc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504352"
---
# <a name="directdraw-return-codes"></a>DirectDraw-Rückgabecodes

Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden. In dieser Tabelle sind die Werte aufgeführt, die von allen Methoden der [DirectDraw-Schnittstellen](directdraw-interfaces.md) und [DirectDraw-Funktionen zurückgegeben werden können.](directdraw-functions.md) Eine Liste der Fehlercodes, die jede Methode oder Funktion zurückgeben kann, finden Sie in der Methoden- oder Funktionsbeschreibung.

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**
</dt> <dd> <dl> <dt>



Die Anforderung wurde erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ ALREADYINITIALIZED**
</dt> <dd> <dl> <dt>



Das -Objekt wurde bereits initialisiert.


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**
</dt> <dd> <dl> <dt>



Ein DirectDrawClipper-Objekt wird an eine Quelloberfläche angefügt, die an einen Aufruf der [**IDirectDrawSurface7::BltFast-Methode übergeben**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**
</dt> <dd> <dl> <dt>



Eine Oberfläche kann nicht an eine andere angeforderte Oberfläche angefügt werden.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**
</dt> <dd> <dl> <dt>



Eine Oberfläche kann nicht von einer anderen angeforderten Oberfläche getrennt werden.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**
</dt> <dd> <dl> <dt>



Windows können keine gerätespezifischen Kontexte (DCs) mehr erstellen, oder ein DC hat eine palettenindizierte Oberfläche angefordert, wenn die Oberfläche keine Palette hatte und der Anzeigemodus nicht palettenindiziert wurde (in diesem Fall kann DirectDraw keine richtige Palette im DC auswählen).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**
</dt> <dd> <dl> <dt>



Primäre und 3D-Oberflächen oder implizit erstellte Oberflächen können nicht dupliziert werden.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**
</dt> <dd> <dl> <dt>



Der Zugriff auf diese Oberfläche wird verweigert, weil versucht wurde, die primäre Oberfläche ohne DCI-Unterstützung (Display Control Interface) zu sperren.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**
</dt> <dd> <dl> <dt>



Fehler beim Sperren einer Oberfläche. Die Seitensperre funktioniert auf einer Anzeigespeicheroberfläche oder einer emulierten primären Oberfläche nicht.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**
</dt> <dd> <dl> <dt>



Fehler beim Entsperren einer Oberfläche. Das Entsperren von Seiten funktioniert auf einer Anzeigespeicheroberfläche oder einer emulierten primären Oberfläche nicht.


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR \_ CLIPPERISUSINGHWND**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Clipliste für ein DirectDrawClipper-Objekt zu erstellen, das bereits ein Fensterhandle überwacht.


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**
</dt> <dd> <dl> <dt>



Für diesen Vorgang ist kein Quellfarbschlüssel angegeben.


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ CURRENTLYNOTAVAIL**
</dt> <dd> <dl> <dt>



Derzeit ist keine Unterstützung verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**
</dt> <dd> <dl> <dt>



Neu für DirectX 7.0. Die Oberfläche erfordert das DDSCAPS \_ COMPLEX-Flag.


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**
</dt> <dd> <dl> <dt>



Für diese Oberfläche wurde bereits ein Gerätekontext (DC) zurückgegeben. Für jede Oberfläche kann nur ein DC abgerufen werden.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNSURFACE**
</dt> <dd> <dl> <dt>



Von einem DirectDraw-Gerät erstellte Oberflächen können nicht direkt von einem anderen DirectDraw-Gerät verwendet werden.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**
</dt> <dd> <dl> <dt>



Für diesen Prozess wurde bereits ein DirectDraw-Objekt erstellt, das diesen Treiber darstellt.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR \_ EXCEPTION**
</dt> <dd> <dl> <dt>



Beim Ausführen des angeforderten Vorgangs ist eine Ausnahme aufgetreten.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**
</dt> <dd> <dl> <dt>



Es wurde versucht, die kooperative Ebene so zu setzen, dass sie bereits auf exklusiv festgelegt wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ ABGELAUFEN**
</dt> <dd> <dl> <dt>



Die Daten sind abgelaufen und daher nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ GENERIC**
</dt> <dd> <dl> <dt>



Es gibt eine nicht definierte Fehlerbedingung.


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**
</dt> <dd> <dl> <dt>



Die Höhe des bereitgestellten Rechtecks ist kein Vielfaches der erforderlichen Ausrichtung.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWNDALREADYSET**
</dt> <dd> <dl> <dt>



Das DirectDraw-Fensterhand handle auf kooperativer Ebene wurde bereits festgelegt. Sie kann nicht zurückgesetzt werden, während für den Prozess Oberflächen oder Paletten erstellt wurden.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**
</dt> <dd> <dl> <dt>



DirectDraw kann den Zustand nicht wiederherstellen, da das DirectDraw-Fensterhand handle auf kooperativer Ebene untergliedert wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ IMPLICITLYCREATED**
</dt> <dd> <dl> <dt>



Die Oberfläche kann nicht wiederhergestellt werden, da es sich um eine implizit erstellte Oberfläche handelt.


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**
</dt> <dd> <dl> <dt>



Die Anforderung zur Erstellung der primären Oberfläche passt nicht zur vorhandenen primären Oberfläche.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR \_ INVALIDCAPS**
</dt> <dd> <dl> <dt>



Mindestens ein Funktionsbit, das an die Rückruffunktion übergeben wird, ist falsch.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**
</dt> <dd> <dl> <dt>



DirectDraw unterstützt die bereitgestellte Clipliste nicht.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**
</dt> <dd> <dl> <dt>



Der guiD (Globally Unique Identifier), der an die [**DirectDrawCreate-Funktion**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) übergeben wird, ist kein gültiger DirectDraw-Treiberbezeichner.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INVALIDMODE**
</dt> <dd> <dl> <dt>



DirectDraw unterstützt den angeforderten Modus nicht.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INVALIDOBJECT**
</dt> <dd> <dl> <dt>



DirectDraw hat einen Zeiger empfangen, der ein ungültiges DirectDraw-Objekt war.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR \_ INVALIDPARAMS**
</dt> <dd> <dl> <dt>



Mindestens einer der an die -Methode übergebenen Parameter ist falsch.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**
</dt> <dd> <dl> <dt>



Das Pixelformat war wie angegeben ungültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR \_ INVALIDPOSITION**
</dt> <dd> <dl> <dt>



Die Position der Überlagerung auf dem Ziel ist nicht mehr gültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**
</dt> <dd> <dl> <dt>



Das bereitgestellte Rechteck war ungültig.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**
</dt> <dd> <dl> <dt>



Der angegebene Stream enthält ungültige Daten.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**
</dt> <dd> <dl> <dt>



Die Oberfläche war vom falschen Typ.


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**
</dt> <dd> <dl> <dt>



Eine oder mehrere Oberflächen sind gesperrt, was den Fehler des angeforderten Vorgangs verursacht.


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**
</dt> <dd> <dl> <dt>



Es sind mehr Daten verfügbar, als von der angegebenen Puffergröße gespeichert werden können.


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR \_ NEWMODE**
</dt> <dd> <dl> <dt>



Neu für DirectX 7.0. Wenn [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) mit dem DDSMT ISTESTREQUIRED-Flag aufgerufen wird, wird dieser Wert möglicherweise zurückgeben, um zu kennzeichnen, dass einige oder alle Auflösungen getestet werden können und \_ sollten. [**IDirectDraw7::EvaluateMode gibt**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) diesen Wert zurück, um anzugeben, dass der Test in einen neuen Anzeigemodus umgeschaltet wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**
</dt> <dd> <dl> <dt>



Es ist keine 3D-Hardware oder Emulation vorhanden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**
</dt> <dd> <dl> <dt>



Es ist keine Hardware für die Alphabeschleunigung vorhanden oder verfügbar, die den Fehler des angeforderten Vorgangs verursacht.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**
</dt> <dd> <dl> <dt>



Es ist keine Bitblockübertragungshardware vorhanden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOCLIPLIST**
</dt> <dd> <dl> <dt>



Es ist keine Clipliste verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**
</dt> <dd> <dl> <dt>



An das Surface-Objekt ist kein DirectDrawClipper-Objekt angefügt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**
</dt> <dd> <dl> <dt>



Es ist keine Hardware für die Farbkonvertierung vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**
</dt> <dd> <dl> <dt>



Die Oberfläche verfügt derzeit nicht über einen Farbschlüssel.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für den Zielfarbschlüssel.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**
</dt> <dd> <dl> <dt>



Eine create-Funktion wurde ohne die [**IDirectDraw7::SetCooperativeLevel-Methode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) aufgerufen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ NODC**
</dt> <dd> <dl> <dt>



Für diese Oberfläche wurde noch kein Gerätekontext (DC) erstellt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**
</dt> <dd> <dl> <dt>



Es ist keine DirectDraw-ROP-Hardware (Raster-Operation) verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**
</dt> <dd> <dl> <dt>



Die ausschließliche Hardware-DirectDraw-Objekterstellung ist nicht möglich. Der Treiber unterstützt keine Hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**
</dt> <dd> <dl> <dt>



DirectDraw-Unterstützung ist mit dem aktuellen Anzeigetreiber nicht möglich.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**
</dt> <dd> <dl> <dt>



Neu für DirectX 7.0. Die Tests können nicht fortgesetzt werden, da der Treiber für den Anzeigeadapter keine Aktualisierungsraten aufzählt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**\_DDERR-NOEMULATION**
</dt> <dd> <dl> <dt>



Softwareemulation ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOEXCLUSIVEMODE**
</dt> <dd> <dl> <dt>



Für den Vorgang muss die Anwendung über den exklusiven Modus verfügen, die Anwendung jedoch nicht über den exklusiven Modus.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**
</dt> <dd> <dl> <dt>



Das Spiegeln sichtbarer Oberflächen wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**
</dt> <dd> <dl> <dt>



Es wurde versucht, ein Gerätefenster zu erstellen oder festzulegen, ohne zuerst das Fokusfenster festzulegen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**
</dt> <dd> <dl> <dt>



Es ist keine GDI vorhanden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOHWND**
</dt> <dd> <dl> <dt>



Clipper Benachrichtigung erfordert ein Fensterhandle, oder es wurde zuvor kein Fensterhandle als Fensterhandle auf kooperativer Ebene festgelegt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**
</dt> <dd> <dl> <dt>



Es ist keine Mipmap-fähige Hardware für die Texturzuordnung vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**
</dt> <dd> <dl> <dt>



Es ist keine Spiegelungshardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**
</dt> <dd> <dl> <dt>



Neu für DirectX 7.0. Die Tests können nicht fortgesetzt werden, da dem Monitor keine EDID-Daten zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**
</dt> <dd> <dl> <dt>



Es wurde versucht, nichtlokalen Videospeicher von einem Gerät zuzuordnen, das keinen nicht lokalen Videospeicher unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**
</dt> <dd> <dl> <dt>



Das Gerät unterstützt keine optimierten Oberflächen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**
</dt> <dd> <dl> <dt>



Die [**IDirectDrawSurface7::GetOverlayPosition-Methode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) wird für eine Überlagerung aufgerufen, für die die [**IDirectDrawSurface7::UpdateOverlay-Methode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) nicht aufgerufen wurde, um als Ziel festzulegen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**
</dt> <dd> <dl> <dt>



Es ist keine Überlagerungshardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**
</dt> <dd> <dl> <dt>



An diese Oberfläche ist kein Palettenobjekt angefügt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für Paletten mit 16 oder 256 Farben.


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**
</dt> <dd> <dl> <dt>



Es ist keine geeignete Hardware für rasterbasierte Vorgänge vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**
</dt> <dd> <dl> <dt>



Es ist keine Rotationshardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**
</dt> <dd> <dl> <dt>



Es ist keine Stereohardware vorhanden oder verfügbar.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für Stretching.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**
</dt> <dd> <dl> <dt>



Es ist keine Hardware vorhanden, die Stereooberflächen unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**
</dt> <dd> <dl> <dt>



Das DirectDrawSurface-Objekt verwendet keine 4-Bit-Farbpalette, und der angeforderte Vorgang erfordert eine 4-Bit-Farbpalette.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**
</dt> <dd> <dl> <dt>



Das DirectDrawSurface-Objekt verwendet keine 4-Bit-Farbindexpalette, und der angeforderte Vorgang erfordert eine 4-Bit-Farbindexpalette.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**
</dt> <dd> <dl> <dt>



Das DirectDrawSurface-Objekt verwendet keine 8-Bit-Farbpalette, und der angeforderte Vorgang erfordert eine 8-Bit-Farbpalette.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**
</dt> <dd> <dl> <dt>



Eine Überlagerungskomponente wird für eine nicht überlappende Oberfläche aufgerufen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**
</dt> <dd> <dl> <dt>



Der Vorgang kann nicht ausgeführt werden, da keine Hardware für die Texturzuordnung vorhanden oder verfügbar ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR \_ NOTFLIPPABLE**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche zu spiegeln, die nicht gekippt werden kann.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR \_ NOTFOUND**
</dt> <dd> <dl> <dt>



Das angeforderte Element wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR \_ NOTINITIALIZED**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Schnittstellenmethode eines DirectDraw-Objekts aufzurufen, das von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt wurde, bevor das Objekt initialisiert wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR \_ NOTLOADED**
</dt> <dd> <dl> <dt>



Die Oberfläche ist eine optimierte Oberfläche, aber ihr wurde noch kein Arbeitsspeicher zugeordnet.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR \_ NOTLOCKED**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche zu entsperren, die nicht gesperrt war.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche ohne ausstehende Seitensperren zu entsperren.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**
</dt> <dd> <dl> <dt>



Die verwendete Oberfläche ist keine palettenbasierte Oberfläche.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**
</dt> <dd> <dl> <dt>



Es gibt keine Hardwareunterstützung für synchronisierte Vorgänge mit vertikalem Leerstellen.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOFLOUFFERHW**
</dt> <dd> <dl> <dt>



Der Vorgang zum Erstellen eines Z-Puffers im Anzeigespeicher oder zum Ausführen einer Bitblockübertragung (bitblt) mithilfe eines Z-Puffers kann nicht ausgeführt werden, da keine Hardwareunterstützung für Z-Puffer vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**
</dt> <dd> <dl> <dt>



Die Überlagerungsoberflächen können nicht auf Z-Schicht basierend auf der Z-Reihenfolge angeordnet werden, da die Hardware keine Z-Reihenfolge von Überlagerungen unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR \_ OUTOFCAPS**
</dt> <dd> <dl> <dt>



Die für den angeforderten Vorgang benötigte Hardware wurde bereits zugeordnet.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw verfügt nicht über genügend Arbeitsspeicher, um den Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw verfügt nicht über genügend Anzeigespeicher, um den Vorgang auszuführen.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**\_DDERR-ÜBERLAPPENDERECTS**
</dt> <dd> <dl> <dt>



Die Quell- und Zielrechtecke befinden sich auf derselben Oberfläche und überlappen sich.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR \_ OVERLAYCLIP**
</dt> <dd> <dl> <dt>



Die Hardware unterstützt keine beschnittenen Überlagerungen.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR \_ OVERLAYCOLORKEYONLYONEACTIVE**
</dt> <dd> <dl> <dt>



Es wurde versucht, mehr als einen Farbschlüssel für eine Überlagerung zu aktivieren.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR \_ OVERLAYNOTVISIBLE**
</dt> <dd> <dl> <dt>



Die [**IDirectDrawSurface7::GetOverlayPosition-Methode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) wurde für eine ausgeblendete Überlagerung aufgerufen.


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR \_ PALETTEBUSY**
</dt> <dd> <dl> <dt>



Der Zugriff auf diese Palette wird verweigert, da die Palette durch einen anderen Thread gesperrt ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**
</dt> <dd> <dl> <dt>



Dieser Prozess hat bereits eine primäre Oberfläche erstellt.


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR \_ REGIONTOOSMALL**
</dt> <dd> <dl> <dt>



Der an die [**IDirectDrawClipper::GetClipList-Methode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) übergebene Bereich ist zu klein.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche an eine andere Oberfläche anzufügen, an die sie bereits angefügt ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**
</dt> <dd> <dl> <dt>



Es wurde versucht, eine Oberfläche zu einer Abhängigkeit einer anderen Oberfläche zu machen, von der sie bereits abhängig ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**
</dt> <dd> <dl> <dt>



Der Zugriff auf die Oberfläche wird verweigert, da die Oberfläche durch einen anderen Thread gesperrt ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR \_ SURFACEISOBSCURED**
</dt> <dd> <dl> <dt>



Der Zugriff auf die Oberfläche wird verweigert, da die Oberfläche verdeckt ist.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**
</dt> <dd> <dl> <dt>



Der Zugriff auf die Oberfläche wird verweigert, da der Oberflächenspeicher nicht mehr vorhanden ist. Rufen Sie auf dieser Oberfläche die [**IDirectDrawSurface7::Restore-Methode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) auf, um den zugeordneten Arbeitsspeicher wiederherzustellen.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**
</dt> <dd> <dl> <dt>



Die angeforderte Oberfläche ist nicht angefügt.


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR \_ TESTFINISHED**
</dt> <dd> <dl> <dt>



Neu für DirectX 7.0. Wenn dieser Wert von der [**IDirectDraw7::StartModeTest-Methode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) zurückgegeben wird, bedeutet dies, dass kein Test initiiert werden konnte, da alle für tests ausgewählten Lösungen bereits Aktualisierungsrateinformationen in der Registrierung enthalten. Bei Rückgabe durch [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)bedeutet der Wert, dass DirectDraw einen Aktualisierungsratentest abgeschlossen hat.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIGHEIGHT**
</dt> <dd> <dl> <dt>



Die von DirectDraw angeforderte Höhe ist zu groß.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**
</dt> <dd> <dl> <dt>



Die von DirectDraw angeforderte Größe ist zu groß. Die individuelle Höhe und Breite sind jedoch gültige Größen.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**
</dt> <dd> <dl> <dt>



Die von DirectDraw angeforderte Breite ist zu groß.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR \_ NICHT UNTERSTÜTZT**
</dt> <dd> <dl> <dt>



Der Vorgang wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**
</dt> <dd> <dl> <dt>



Das angeforderte Pixelformat wird von DirectDraw nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**
</dt> <dd> <dl> <dt>



Die Bitmaske im angeforderten Pixelformat wird von DirectDraw nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ UNSUPPORTEDMODE**
</dt> <dd> <dl> <dt>



Die Anzeige befindet sich derzeit in einem nicht unterstützten Modus.


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**
</dt> <dd> <dl> <dt>



Ein vertikales Leerzeichen wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR \_ VIDEONOTACTIVE**
</dt> <dd> <dl> <dt>



Der Videoport ist nicht aktiv.


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASDRAWING**
</dt> <dd> <dl> <dt>



Der vorherige Bitblt-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig.


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ WRONGMODE**
</dt> <dd> <dl> <dt>



Diese Oberfläche kann nicht wiederhergestellt werden, da sie in einem anderen Modus erstellt wurde.


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**
</dt> <dd> <dl> <dt>



Das bereitgestellte Rechteck wurde nicht horizontal an einer erforderlichen Grenze ausgerichtet.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ddraw.h</dt> </dl> |



 

