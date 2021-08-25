---
title: DirectComposition-Fehlercodes (Dcomp.h)
description: In diesem Abschnitt werden die Fehlercodes beschrieben, die spezifisch für DirectComposition sind.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d86ab61574af84e0b4b51223c69b181697dc0ebbdd7995c1bff112e286cc3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891980"
---
# <a name="directcomposition-error-codes"></a>DirectComposition-Fehlercodes

Wenn ein Fehler auftritt, gibt Microsoft DirectComposition einen Code als **HRESULT-Wert** zurück. In diesem Abschnitt werden die Fehlercodes beschrieben, die spezifisch für DirectComposition sind. Eine Liste der allgemeinen Component Object Model (COM)-Fehlercodes finden Sie unter [COM-Fehlercodes.](/windows/desktop/com/com-error-codes)

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION \_ ERROR \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>


</dt> <dt>



Das Fensterhandle, das in einem Aufruf der [**IDCompositionDevice::CreateTargetForHwnd-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) angegeben wurde, gehört zu einem anderen Prozess als der Prozess, der das Geräteobjekt erstellt hat.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_GERENDERTE DCOMPOSITION-FEHLEROBERFLÄCHE \_ \_ \_**
</dt> <dd> <dl> <dt>


</dt> <dt>



Die Oberfläche wurde bereits gerendert, als die Anwendung die [**IDCompositionSurface::BeginDraw-,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) [**IDCompositionSurface::SuspendDraw-**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)oder [**IDCompositionSurface::ResumeDraw-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) aufgerufen hat. Weitere Informationen finden Sie in den Hinweisen.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_DCOMPOSITION-FEHLEROBERFLÄCHE \_ WIRD NICHT \_ \_ \_ GERENDERT**
</dt> <dd> <dl> <dt>


</dt> <dt>



Die Anwendung hat die [**IDCompositionSurface::SuspendDraw-,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) [**IDCompositionSurface::ResumeDraw-**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)oder [**IDCompositionSurface::EndDraw-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) für eine Oberfläche aufgerufen, die nicht gerendert wird. Weitere Informationen finden Sie in den Hinweisen.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**FEHLERFENSTER "DCOMPOSITION" \_ \_ BEREITS \_ \_ ZUSAMMENGESETZT**
</dt> <dd> <dl> <dt>


</dt> <dt>



Die [**IDCompositionDevice::CreateTargetForHwnd-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) wurde mit *hwnd* und *den obersten* Parametern aufgerufen, für die bereits eine visuelle Struktur vorhanden ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn ein Aufruf von [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) die letzte Aktion war:



| Aufrufen dieser Methode:                                    | Gibt diesen Wert zurück:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_GERENDERTE DCOMPOSITION-FEHLEROBERFLÄCHE \_ \_ \_** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_GERENDERTE DCOMPOSITION-FEHLEROBERFLÄCHE \_ \_ \_** |



 

Wenn ein Aufruf von [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) die letzte Aktion war:



| Aufrufen dieser Methode:                                    | Gibt diesen Wert zurück:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_GERENDERTE DCOMPOSITION-FEHLEROBERFLÄCHE \_ \_ \_** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_GERENDERTE DCOMPOSITION-FEHLEROBERFLÄCHE \_ \_ \_** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ OK                                             |



 

Wenn ein Aufruf von [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) die letzte Aktion war:



| Aufrufen dieser Methode:                                    | Gibt diesen Wert zurück:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_GERENDERTE DCOMPOSITION-FEHLEROBERFLÄCHE \_ \_ \_**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_DCOMPOSITION-FEHLEROBERFLÄCHE, \_ \_ DIE \_ GERENDERT WIRD.** |



 

Wenn ein Aufruf von [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) die letzte Aktion war:



| Aufrufen dieser Methode:                                    | Gibt diesen Wert zurück:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ OK                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **\_DCOMPOSITION-FEHLEROBERFLÄCHE \_ WIRD NICHT \_ \_ \_ GERENDERT.** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_DCOMPOSITION-FEHLEROBERFLÄCHE \_ WIRD NICHT \_ \_ \_ GERENDERT.** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_DCOMPOSITION-FEHLEROBERFLÄCHE \_ WIRD NICHT \_ \_ \_ GERENDERT.** |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Dcomp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectComposition-Referenz](reference.md)
</dt> </dl>

 

