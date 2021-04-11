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
# <a name="directdraw-return-codes"></a><span data-ttu-id="e1ea6-103">DirectDraw-Rückgabe Codes</span><span class="sxs-lookup"><span data-stu-id="e1ea6-103">DirectDraw Return Codes</span></span>

<span data-ttu-id="e1ea6-104">Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="e1ea6-105">In dieser Tabelle sind die Werte aufgelistet, die von allen Methoden der [DirectDraw-Schnittstellen](directdraw-interfaces.md) und [DirectDraw-Funktionen](directdraw-functions.md)zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-105">This table lists the values that can be returned by all methods of the [DirectDraw Interfaces](directdraw-interfaces.md) and [DirectDraw Functions](directdraw-functions.md).</span></span> <span data-ttu-id="e1ea6-106">Eine Liste der Fehlercodes, die von den einzelnen Methoden oder Funktionen zurückgegeben werden können, finden Sie in der Beschreibung der Methode oder Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-106">For a list of the error codes that each method or function can return, see the method or function description.</span></span>

<dl> <dt>

<span data-ttu-id="e1ea6-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD\_OK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-108">Die Anforderung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-108">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**dderr \_ alread-initialisiert**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR\_ALREADYINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-110">Das Objekt wurde bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-110">The object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**dderr \_ bltfastcantclip**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR\_BLTFASTCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-112">Ein directdrawclipperobjekt wird an eine Quell Oberfläche angefügt, die an einen aufzurufenden Befehl der [**IDirectDrawSurface7:: bltfast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) -Methode übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-112">A DirectDrawClipper object is attached to a source surface that has passed into a call to the [**IDirectDrawSurface7::BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**dderr \_ cannotattachsurface**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR\_CANNOTATTACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-114">Eine Oberfläche kann nicht an eine andere angeforderte Oberfläche angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-114">A surface cannot be attached to another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**dderr \_ cannotdetachsurface**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR\_CANNOTDETACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-116">Eine Oberfläche kann nicht von einer anderen angeforderten Oberfläche getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-116">A surface cannot be detached from another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**dderr \_ kankreatedc**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR\_CANTCREATEDC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-118">Windows kann keine weiteren Geräte Kontexte (DCS) erstellen, oder ein DC hat eine palettenindizierte Oberfläche angefordert, wenn die Oberfläche keine Palette enthielt und der Anzeigemodus nicht palettenindiziert war (in diesem Fall kann DirectDraw keine passende Palette in den DC auswählen).</span><span class="sxs-lookup"><span data-stu-id="e1ea6-118">Windows cannot create any more device contexts (DCs), or a DC has requested a palette-indexed surface when the surface had no palette and the display mode was not palette-indexed (in this case, DirectDraw cannot select a proper palette into the DC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**dderr- \_ kanduplikat**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR\_CANTDUPLICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-120">Primär-und 3D-Oberflächen oder Flächen, die implizit erstellt werden, können nicht dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-120">Primary and 3-D surfaces, or surfaces that are implicitly created, cannot be duplicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**dderr- \_ kanlocksurface**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR\_CANTLOCKSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-122">Der Zugriff auf diese Oberfläche wurde abgelehnt, weil versucht wurde, die primäre Oberfläche ohne die Unterstützung der Anzeige Steuerungs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e1ea6-122">Access to this surface is refused because an attempt was made to lock the primary surface without Display Control Interface (DCI) support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**dderr- \_ kanpagelock**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR\_CANTPAGELOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-124">Der Versuch, eine Oberfläche zu sperren, ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-124">An attempt to page-lock a surface failed.</span></span> <span data-ttu-id="e1ea6-125">Die Seiten Sperre funktioniert nicht auf einer Anzeige Speicher Oberfläche oder einer emulierten primären Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-125">Page lock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**dderr- \_ kanpageunlock**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR\_CANTPAGEUNLOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-127">Der Versuch, eine Oberfläche zu entsperren, ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-127">An attempt to page-unlock a surface failed.</span></span> <span data-ttu-id="e1ea6-128">Das Entsperren von Seiten funktioniert nicht auf einer Anzeige-oder einer emulierten primären Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-128">Page unlock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**dderr \_ clipperisusinghwnd**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR\_CLIPPERISUSINGHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-130">Es wurde versucht, eine Clip Liste für ein directdrawclipperobjekt festzulegen, das bereits ein Fenster Handle überwacht.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-130">An attempt was made to set a clip list for a DirectDrawClipper object that is already monitoring a window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**dderr \_ colorkeynotset**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR\_COLORKEYNOTSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-132">Für diesen Vorgang ist kein Quell Farbschlüssel angegeben.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-132">No source color key is specified for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**dderr \_ currentlynotavail**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR\_CURRENTLYNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-134">Zurzeit ist keine Unterstützung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-134">No support is currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**dderr \_ ddscapscomplexrequired**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR\_DDSCAPSCOMPLEXREQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-136">Neu bei DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-136">New for DirectX 7.0.</span></span> <span data-ttu-id="e1ea6-137">Die Oberfläche erfordert das komplexe DDSCAPS- \_ Flag.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-137">The surface requires the DDSCAPS\_COMPLEX flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**dderr \_ dcalsorycreated**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR\_DCALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-139">Für diese Oberfläche wurde bereits ein Gerätekontext (DC) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-139">A device context (DC) has already been returned for this surface.</span></span> <span data-ttu-id="e1ea6-140">Für jede Oberfläche kann nur ein DC abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-140">Only one DC can be retrieved for each surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>dderr \_ devicedoesntownsurface**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR\_DEVICEDOESNTOWNSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-142">Von einem DirectDraw-Gerät erstellte Oberflächen können nicht direkt von einem anderen DirectDraw-Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-142">Surfaces created by one DirectDraw device cannot be used directly by another DirectDraw device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>dderr \_ directdrawalleserycreated**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR\_DIRECTDRAWALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-144">Ein DirectDraw-Objekt, das diesen Treiber darstellt, wurde für diesen Prozess bereits erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-144">A DirectDraw object representing this driver has already been created for this process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**dderr- \_ Ausnahme**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-146">Beim Ausführen des angeforderten Vorgangs ist eine Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-146">An exception was encountered while performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**dderr \_ exclusivemu-leseryset**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR\_EXCLUSIVEMODEALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-148">Es wurde versucht, die kooperative Ebene festzulegen, als Sie bereits auf exklusiv festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-148">An attempt was made to set the cooperative level when it was already set to exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**dderr \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-150">Die Daten sind abgelaufen und daher nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-150">The data has expired and is therefore no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**dderr ( \_ generisch)**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-152">Es gibt eine nicht definierte Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-152">There is an undefined error condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**dderr- \_ heightalign**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR\_HEIGHTALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-154">Die Höhe des bereitgestellten Rechtecks ist kein Vielfaches der erforderlichen Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-154">The height of the provided rectangle is not a multiple of the required alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**dderr \_ hwndallesset**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR\_HWNDALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-156">Das Fenster Handle der Zusammenführung auf der Basis von DirectDraw wurde bereits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-156">The DirectDraw cooperative-level window handle has already been set.</span></span> <span data-ttu-id="e1ea6-157">Sie kann nicht zurückgesetzt werden, während der Prozess Oberflächen oder Paletten erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-157">It cannot be reset while the process has surfaces or palettes created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**dderr \_ hwndsubklassiert**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR\_HWNDSUBCLASSED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-159">Das Wiederherstellen des Zustands durch DirectDraw wird verhindert, da das Fenster Handle für die Zusammenführung des DirectDraw-Fensters auf Genossenschafts Ebene untergeordnet ist</span><span class="sxs-lookup"><span data-stu-id="e1ea6-159">DirectDraw is prevented from restoring state because the DirectDraw cooperative-level window handle has been subclassed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**dderr \_ implicitlycreated**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR\_IMPLICITLYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-161">Die Oberfläche kann nicht wieder hergestellt werden, da Sie eine implizit erstellte Oberfläche ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-161">The surface cannot be restored because it is an implicitly created surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**dderr \_ incompatibleprimary**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR\_INCOMPATIBLEPRIMARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-163">Die primäre Oberflächen Erstellungs Anforderung stimmt nicht mit der vorhandenen primären Oberfläche identisch.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-163">The primary surface creation request does not match the existing primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**dderr- \_ invalidcaps**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR\_INVALIDCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-165">Mindestens eine der an die Rückruffunktion weiter gegebenen Funktions Bits ist falsch.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-165">One or more of the capability bits passed to the callback function are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**dderr \_ invalidcliplist**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR\_INVALIDCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-167">DirectDraw unterstützt die angegebene Clip Liste nicht.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-167">DirectDraw does not support the provided clip list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**dderr \_ invaliddirectdrawguid**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR\_INVALIDDIRECTDRAWGUID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-169">Die an die [**directdrawcreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) -Funktion über gegebene Globally Unique Identifier (GUID) ist kein gültiger DirectDraw-Treiber Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-169">The globally unique identifier (GUID) passed to the [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) function is not a valid DirectDraw driver identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**dderr \_ invalidmode**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR\_INVALIDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-171">DirectDraw unterstützt den angeforderten Modus nicht.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-171">DirectDraw does not support the requested mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**dderr- \_ invalidobject**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR\_INVALIDOBJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-173">DirectDraw hat einen Zeiger empfangen, der ein ungültiges DirectDraw-Objekt war.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-173">DirectDraw received a pointer that was an invalid DirectDraw object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**dderr \_ invalidparametriams**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR\_INVALIDPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-175">Mindestens ein Parameter, der an die-Methode weitergegeben wurde, ist falsch.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-175">One or more of the parameters passed to the method are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**dderr \_ invalidpixelformat**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR\_INVALIDPIXELFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-177">Das Pixel Format war wie angegeben ungültig.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-177">The pixel format was invalid as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**dderr- \_ invalidposition**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR\_INVALIDPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-179">Die Position des Overlay auf dem Ziel ist nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-179">The position of the overlay on the destination is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**dderr \_ InvalidRect**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR\_INVALIDRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-181">Das angegebene Rechteck war ungültig.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-181">The provided rectangle was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**dderr \_ invalidstream**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR\_INVALIDSTREAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-183">Der angegebene Stream enthält ungültige Daten.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-183">The specified stream contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**dderr \_ invalidsurfaketype**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR\_INVALIDSURFACETYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-185">Die Oberfläche hatte den falschen Typ.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-185">The surface was of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**dderr \_ lockedoberflächen**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR\_LOCKEDSURFACES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-187">Mindestens eine Oberfläche ist gesperrt, wodurch der angeforderte Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-187">One or more surfaces are locked, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**dderr \_ MoreData**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR\_MOREDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-189">Es sind mehr Daten verfügbar, als die angegebene Puffergröße enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-189">There is more data available than the specified buffer size can hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**dderr- \_ NEWMODE**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR\_NEWMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-191">Neu bei DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-191">New for DirectX 7.0.</span></span> <span data-ttu-id="e1ea6-192">Wenn [**IDirectDraw7:: startmodetest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) mit dem ddsmt \_ istestrequired-Flag aufgerufen wird, kann dieser Wert zurückgegeben werden, um anzugeben, dass einige oder alle Auflösungen getestet werden können.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-192">When [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) is called with the DDSMT\_ISTESTREQUIRED flag, it might return this value to denote that some or all of the resolutions can and should be tested.</span></span> <span data-ttu-id="e1ea6-193">[**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) gibt diesen Wert zurück, um anzugeben, dass der Test in einen neuen Anzeigemodus gewechselt hat.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-193">[**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) returns this value to indicate that the test has switched to a new display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**Dderr \_ NO3D**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR\_NO3D**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-195">Es ist keine 3D-Hardware oder Emulation vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-195">No 3-D hardware or emulation is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**dderr- \_ noalphahw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR\_NOALPHAHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-197">Es ist keine Alpha Beschleunigung-Hardware vorhanden oder verfügbar, die den angeforderten Vorgang nicht bewirkt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-197">No alpha-acceleration hardware is present or available, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**dderr \_ noblthw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR\_NOBLTHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-199">Es ist kein Bitblock übertragen von Hardware vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-199">No bit block transferring hardware is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**dderr- \_ nocliplist**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR\_NOCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-201">Es ist keine Clip Liste verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-201">No clip list is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**dderr- \_ noclipperattached**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR\_NOCLIPPERATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-203">An das Surface-Objekt ist kein directdrawclipperobjekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-203">No DirectDrawClipper object is attached to the surface object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**dderr \_ nocolor-VHW**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR\_NOCOLORCONVHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-205">Es ist keine Farb Konvertierungs Hardware vorhanden oder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-205">No color-conversion hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**dderr \_ nocolorkey**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR\_NOCOLORKEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-207">Die Oberfläche verfügt zurzeit nicht über einen Farbschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-207">The surface does not currently have a color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**dderr \_ nocolorkeyhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR\_NOCOLORKEYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-209">Es gibt keine Hardwareunterstützung für den Ziel Farbschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-209">There is no hardware support for the destination color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**dderr \_ nokooperativelevelset**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR\_NOCOOPERATIVELEVELSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-211">Eine Create-Funktion wurde ohne die [**IDirectDraw7:: setkooperativelevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-211">A create function was called without the [**IDirectDraw7::SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**dderr- \_ nodc**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR\_NODC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-213">Für diese Oberfläche wurde nie ein Gerätekontext (DC) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-213">No device context (DC) has ever been created for this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**dderr \_ noddropshw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR\_NODDROPSHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-215">Es ist keine DirectDraw-Raster-Operation-Hardware (ROP) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-215">No DirectDraw raster-operation (ROP) hardware is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**dderr \_ nodirectdrawhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR\_NODIRECTDRAWHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-217">Reine Hardware-DirectDraw-Objekt Erstellung ist nicht möglich. der Treiber unterstützt keine Hardware.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-217">Hardware-only DirectDraw object creation is not possible; the driver does not support any hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**dderr \_ nodirectdrawsupport**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR\_NODIRECTDRAWSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-219">DirectDraw-Unterstützung ist mit dem aktuellen Anzeigetreiber nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-219">DirectDraw support is not possible with the current display driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**dderr \_ nodriversupport**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR\_NODRIVERSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-221">Neu bei DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-221">New for DirectX 7.0.</span></span> <span data-ttu-id="e1ea6-222">Der Test kann nicht fortgesetzt werden, da der Anzeige Adapter Treiber keine Aktualisierungs Raten auflistet.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-222">Testing cannot proceed because the display adapter driver does not enumerate refresh rates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**dderr- \_ noemulation**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR\_NOEMULATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-224">Die Software Emulation ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-224">Software emulation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**dderr \_ noexclusivemode**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR\_NOEXCLUSIVEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-226">Der Vorgang erfordert, dass die Anwendung den exklusiven Modus hat, aber die Anwendung hat keinen exklusiven Modus.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-226">The operation requires the application to have exclusive mode, but the application does not have exclusive mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**dderr \_ nofliphw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR\_NOFLIPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-228">Das Kippen von sichtbaren Oberflächen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-228">Flipping visible surfaces is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**dderr \_ nofocenwindow**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR\_NOFOCUSWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-230">Es wurde versucht, ein Geräte Fenster zu erstellen oder festzulegen, ohne zuvor das Fokus Fenster festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-230">An attempt was made to create or set a device window without first setting the focus window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**dderr- \_ nogdi**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR\_NOGDI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-232">Es ist kein GDI vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-232">No GDI is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**dderr- \_ nohwnd**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR\_NOHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-234">Die clipperbenachrichtigung erfordert ein Fenster Handle, oder es wurde zuvor kein Fenster Handle als Fenster Handle der kooperativen Ebene festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-234">Clipper notification requires a window handle, or no window handle has been previously set as the cooperative level window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**dderr \_ nomipmaphw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR\_NOMIPMAPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-236">Es ist keine MipMap-fähige Textur Zuordnungs Hardware vorhanden oder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-236">No mipmap-capable texture mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**dderr \_ nomirrorhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR\_NOMIRRORHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-238">Es ist keine Spiegelungs Hardware vorhanden oder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-238">No mirroring hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**dderr \_ nomonitorinformation**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR\_NOMONITORINFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-240">Neu bei DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-240">New for DirectX 7.0.</span></span> <span data-ttu-id="e1ea6-241">Das Testen kann nicht fortgesetzt werden, da dem Monitor keine EDID-Daten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-241">Testing cannot proceed because the monitor has no associated EDID data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**dderr \_ nononlocalvidmem**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR\_NONONLOCALVIDMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-243">Es wurde versucht, einen nicht lokalen Videospeicher von einem Gerät zuzuordnen, das nicht lokalen Videospeicher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-243">An attempt was made to allocate nonlocal video memory from a device that does not support nonlocal video memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**dderr \_ nooptimizehw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR\_NOOPTIMIZEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-245">Das Gerät unterstützt keine optimierten Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-245">The device does not support optimized surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**dderr \_ nooverlaydest**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR\_NOOVERLAYDEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-247">Die [**IDirectDrawSurface7:: gedeverlayposition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) -Methode wird auf einem Overlay aufgerufen, für das die [**IDirectDrawSurface7:: updateoverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) -Methode nicht aufgerufen wurde, um als Ziel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-247">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method is called on an overlay that the [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) method has not been called on to establish as a destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**dderr \_ nooverlayhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR\_NOOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-249">Es ist keine über Lagerungs Hardware vorhanden oder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-249">No overlay hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**dderr \_ nopaletteattached**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR\_NOPALETTEATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-251">An diese Oberfläche ist kein Palettenobjekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-251">No palette object is attached to this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**dderr \_ nopalettehw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR\_NOPALETTEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-253">Es gibt keine Hardwareunterstützung für 16-oder 256-farbige Paletten.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-253">There is no hardware support for 16- or 256-color palettes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**dderr \_ norasterophw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR\_NORASTEROPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-255">Es ist keine geeignete Raster Betriebs Hardware vorhanden oder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-255">No appropriate raster-operation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**dderr \_ norotationhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR\_NOROTATIONHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-257">Es ist keine Rotations Hardware vorhanden oder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-257">No rotation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**dderr \_ nostereohardware**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR\_NOSTEREOHARDWARE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-259">Es ist keine Stereo Hardware vorhanden oder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-259">There is no stereo hardware present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**dderr \_ nostretchhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR\_NOSTRETCHHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-261">Es gibt keine Hardwareunterstützung für das Stretching.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-261">There is no hardware support for stretching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**dderr- \_ nosurfakeleft**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR\_NOSURFACELEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-263">Es ist keine Hardware vorhanden, die Stereo Oberflächen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-263">There is no hardware present that supports stereo surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**Dderr \_ NOT4BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR\_NOT4BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-265">Das directdrawsurface-Objekt verwendet keine 4-Bit-Farbpalette, und der angeforderte Vorgang erfordert eine 4-Bit-Farbpalette.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-265">The DirectDrawSurface object is not using a 4-bit color palette, and the requested operation requires a 4-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**Dderr \_ NOT4BITCOLORINDEX**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR\_NOT4BITCOLORINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-267">Das directdrawsurface-Objekt verwendet keine 4-Bit-Farb Index Palette, und der angeforderte Vorgang erfordert eine 4-Bit-Farb Index Palette.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-267">The DirectDrawSurface object is not using a 4-bit color index palette, and the requested operation requires a 4-bit color index palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**Dderr \_ NOT8BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR\_NOT8BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-269">Das directdrawsurface-Objekt verwendet keine 8-Bit-Farbpalette, und der angeforderte Vorgang erfordert eine 8-Bit-Farbpalette.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-269">The DirectDrawSurface object is not using an 8-bit color palette, and the requested operation requires an 8-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**dderr \_ notaoverlaysurface**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR\_NOTAOVERLAYSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-271">Eine Überlagerungs Komponente wird für eine nicht Überlagerungs Oberfläche aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-271">An overlay component is called for a nonoverlay surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**dderr \_ notexturehw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR\_NOTEXTUREHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-273">Der Vorgang kann nicht ausgeführt werden, da keine Textur zuordnungshardware vorhanden oder verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-273">The operation cannot be carried out because no texture-mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**dderr \_ notflippable**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR\_NOTFLIPPABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-275">Es wurde versucht, eine Oberfläche zu kippen, die nicht gekippt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-275">An attempt was made to flip a surface that cannot be flipped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**dderr \_ NotFound**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-277">Das angeforderte Element wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-277">The requested item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**dderr \_ notinitialisiert**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR\_NOTINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-279">Es wurde versucht, eine Schnittstellen Methode eines DirectDraw-Objekts aufzurufen, das von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) erstellt wurde, bevor das Objekt initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-279">An attempt was made to call an interface method of a DirectDraw object created by [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) before the object was initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**dderr \_ notloaded**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR\_NOTLOADED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-281">Die Oberfläche ist eine optimierte Oberfläche, aber ihr wurde noch kein Arbeitsspeicher zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-281">The surface is an optimized surface, but it has not yet been allocated any memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**dderr nicht \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR\_NOTLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-283">Es wurde versucht, eine Oberfläche zu entsperren, die nicht gesperrt war.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-283">An attempt was made to unlock a surface that was not locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**dderr \_ notpagelocked**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR\_NOTPAGELOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-285">Es wurde versucht, eine Oberfläche ohne ausstehende Seiten Sperren auf eine Seite zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-285">An attempt was made to page-unlock a surface with no outstanding page locks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**dderr \_ notpalettisiert**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR\_NOTPALETTIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-287">Die verwendete Oberfläche ist keine palettenbasierte Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-287">The surface being used is not a palette-based surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**dderr \_ novsynchronw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR\_NOVSYNCHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-289">Es gibt keine Hardwareunterstützung für vertikale, leere synchronisierte Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-289">There is no hardware support for vertical blank synchronized operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**dderr \_ nozbufferhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR\_NOZBUFFERHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-291">Der Vorgang zum Erstellen eines z-Puffers im Anzeige Speicher oder zum Ausführen einer Bitblock Übertragung (BitBLT) kann nicht ausgeführt werden, da keine Hardwareunterstützung für z-Puffer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-291">The operation to create a z-buffer in display memory or to perform a bit block transfer (bitblt), using a z-buffer cannot be carried out because there is no hardware support for z-buffers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**dderr \_ nozoverlayhw**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR\_NOZOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-293">Die Überlagerungs Flächen können auf der z-Reihenfolge nicht auf z-Reihenfolge basieren, weil die Hardware keine z-Reihenfolge von Überlagerungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-293">The overlay surfaces cannot be z-layered, based on the z-order because the hardware does not support z-ordering of overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**dderr- \_ outo**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR\_OUTOFCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-295">Die für den angeforderten Vorgang erforderliche Hardware wurde bereits zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-295">The hardware needed for the requested operation has already been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**dderr- \_ outo-Memory**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-297">DirectDraw verfügt nicht über genügend Arbeitsspeicher, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-297">DirectDraw does not have enough memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**dderr \_ ouum-videomemory**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR\_OUTOFVIDEOMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-299">DirectDraw verfügt nicht über genügend Anzeige Speicher, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-299">DirectDraw does not have enough display memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**dderr \_ overlappingrects**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR\_OVERLAPPINGRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-301">Die Quell-und Ziel Rechtecke befinden sich auf derselben Oberfläche und überlappen einander.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-301">The source and destination rectangles are on the same surface and overlap each other.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**dderr \_ overlaycantclip**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR\_OVERLAYCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-303">Die Hardware unterstützt keine abgeschnitten-Überlagerungen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-303">The hardware does not support clipped overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**dderr \_ overlaycolorkeyonlyoneactive**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR\_OVERLAYCOLORKEYONLYONEACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-305">Es wurde versucht, mehr als einen Farbschlüssel auf einem Overlay zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-305">An attempt was made to have more than one color key active on an overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**dderr \_ overlaynotvisible**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR\_OVERLAYNOTVISIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-307">Die [**IDirectDrawSurface7:: gedeverlayposition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) -Methode wurde für ein verborgenes Overlay aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-307">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method was called on a hidden overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**dderr \_ palettebusy**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR\_PALETTEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-309">Der Zugriff auf diese Palette wird verweigert, da die Palette von einem anderen Thread gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-309">Access to this palette is refused because the palette is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**dderr \_ primarysurfacealread yexistiert**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR\_PRIMARYSURFACEALREADYEXISTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-311">Dieser Prozess hat bereits eine primäre Oberfläche erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-311">This process has already created a primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**dderr \_ Regionin Small**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR\_REGIONTOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-313">Der an die [**idirectdrawclipper:: getcliplist**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) -Methode über gegebene Bereich ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-313">The region passed to the [**IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) method is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**dderr \_ surfacealsoryattached**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR\_SURFACEALREADYATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-315">Es wurde versucht, eine Oberfläche an eine andere Oberfläche anzufügen, an die Sie bereits angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-315">An attempt was made to attach a surface to another surface to which it is already attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**dderr \_ surfacealleserydependent**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR\_SURFACEALREADYDEPENDENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-317">Es wurde versucht, eine Oberfläche zu einer Abhängigkeit von einer anderen Oberfläche zu machen, von der Sie bereits abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-317">An attempt was made to make a surface a dependency of another surface on which it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**dderr \_ surfacebusy**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR\_SURFACEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-319">Der Zugriff auf die-Oberfläche wird verweigert, da die Oberfläche von einem anderen Thread gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-319">Access to the surface is refused because the surface is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**dderr \_ surfakeisobscgewöhnt**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR\_SURFACEISOBSCURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-321">Der Zugriff auf die-Oberfläche wird verweigert, da die Oberfläche verdeckt ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-321">Access to the surface is refused because the surface is obscured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**dderr \_ surfakelost**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR\_SURFACELOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-323">Der Zugriff auf die-Oberfläche wird verweigert, da der Arbeitsspeicher nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-323">Access to the surface is refused because the surface memory is gone.</span></span> <span data-ttu-id="e1ea6-324">Wenden Sie die [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) -Methode auf dieser Oberfläche an, um den zugeordneten Arbeitsspeicher wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-324">Call the [**IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) method on this surface to restore the memory associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**dderr \_ surfakenotattached**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR\_SURFACENOTATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-326">Die angeforderte Oberfläche ist nicht angefügt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-326">The requested surface is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**dderr \_ testabgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR\_TESTFINISHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-328">Neu bei DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-328">New for DirectX 7.0.</span></span> <span data-ttu-id="e1ea6-329">Wenn Sie von der [**IDirectDraw7:: startmodetest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) -Methode zurückgegeben wird, bedeutet dieser Wert, dass kein Test initiiert werden konnte, weil alle für das Testen ausgewählten Auflösungen bereits über Aktualisierungs rateninformationen in der Registrierung verfügen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-329">When returned by the [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) method, this value means that no test could be initiated because all the resolutions chosen for testing already have refresh rate information in the registry.</span></span> <span data-ttu-id="e1ea6-330">Wenn Sie von [**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)zurückgegeben wird, bedeutet der Wert, dass DirectDraw einen Aktualisierungs Raten Test abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-330">When returned by [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), the value means that DirectDraw has completed a refresh rate test.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**dderr \_ -Dienst**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR\_TOOBIGHEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-332">Die von DirectDraw angeforderte Höhe ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-332">The height requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**dderr-Verzeichnis \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR\_TOOBIGSIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-334">Die von DirectDraw angeforderte Größe ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-334">The size requested by DirectDraw is too large.</span></span> <span data-ttu-id="e1ea6-335">Die einzelne Höhe und Breite sind jedoch gültige Größen.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-335">However, the individual height and width are valid sizes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**dderr-Verzeichnis \_ Breite**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR\_TOOBIGWIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-337">Die von DirectDraw angeforderte Breite ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-337">The width requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**dderr \_ nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-339">Der Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-339">The operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**dderr \_ unsupportedformat**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR\_UNSUPPORTEDFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-341">Das angeforderte Pixel Format wird von DirectDraw nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-341">The pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**dderr \_ unsupportedmask**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR\_UNSUPPORTEDMASK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-343">Die Bitmaske im angeforderten Pixel Format wird von DirectDraw nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-343">The bitmask in the pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**dderr \_ unsupportedmode**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR\_UNSUPPORTEDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-345">Die Anzeige befindet sich zurzeit in einem nicht unterstützten Modus.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-345">The display is currently in an unsupported mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**dderr \_ verticalblankinprogress**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR\_VERTICALBLANKINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-347">Ein vertikaler leerer Vorgang wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-347">A vertical blank is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**dderr \_ videonotactive**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR\_VIDEONOTACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-349">Der Videoport ist nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-349">The video port is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**dderr \_ wasstilldrawing**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR\_WASSTILLDRAWING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-351">Der vorherige BitBLT-Vorgang, der Informationen an diese oder von dieser Oberfläche überträgt, ist unvollständig.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-351">The previous bitblt operation that is transferring information to or from this surface is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**dderr-Fehler \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR\_WRONGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-353">Diese Oberfläche kann nicht wieder hergestellt werden, da Sie in einem anderen Modus erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-353">This surface cannot be restored because it was created in a different mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e1ea6-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**dderr- \_ xalign**</span><span class="sxs-lookup"><span data-stu-id="e1ea6-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR\_XALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e1ea6-355">Das angegebene Rechteck wurde nicht horizontal an einer erforderlichen Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="e1ea6-355">The provided rectangle was not horizontally aligned on a required boundary.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1ea6-356">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1ea6-356">Requirements</span></span>



| <span data-ttu-id="e1ea6-357">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1ea6-357">Requirement</span></span> | <span data-ttu-id="e1ea6-358">Wert</span><span class="sxs-lookup"><span data-stu-id="e1ea6-358">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ea6-359">Header</span><span class="sxs-lookup"><span data-stu-id="e1ea6-359">Header</span></span><br/> | <dl> <span data-ttu-id="e1ea6-360"><dt>Ddraw. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ea6-360"><dt>Ddraw.h</dt></span></span> </dl> |



 

