---
title: Directcomposition-Fehlercodes (Dcomp. h)
description: In diesem Abschnitt werden die Fehlercodes beschrieben, die für directcomposition spezifisch sind.
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
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104894"
---
# <a name="directcomposition-error-codes"></a>Directcomposition-Fehlercodes

Wenn ein Fehler auftritt, gibt Microsoft directcomposition einen Code als **HRESULT** -Wert zurück. In diesem Abschnitt werden die Fehlercodes beschrieben, die für directcomposition spezifisch sind. Eine Liste der allgemeinen Component Object Model (com)-Fehlercodes finden Sie unter [com-Fehlercodes](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**dcomposition- \_ Fehler \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>


</dt> <dt>



Das Fenster Handle, das in einem Aufrufen der [**idcompositiondevice:: foratetargetforhwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) -Methode angegeben wurde, gehört zu einem anderen Prozess als dem, der das Geräte Objekt erstellt hat.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**
</dt> <dd> <dl> <dt>


</dt> <dt>



Die Oberfläche wurde bereits gerendert, als die Anwendung die Methode [**idcompositionsurface:: beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**idcompositionsurface:: suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)oder [**idcompositionsurface:: resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) aufgerufen hat. Weitere Informationen finden Sie in den Hinweisen.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.**
</dt> <dd> <dl> <dt>


</dt> <dt>



Die Anwendung hat die Methode [**idcompositionsurface:: suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**idcompositionsurface:: resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)oder [**idcompositionsurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) für eine Oberfläche aufgerufen, die nicht gerendert wird. Weitere Informationen finden Sie in den Hinweisen.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**Das dcomposition- \_ Fehler \_ Fenster wurde \_ bereits \_ erstellt.**
</dt> <dd> <dl> <dt>


</dt> <dt>



Die [**idcompositiondevice:: foratetargetforhwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) -Methode wurde mit *HWND* und den *obersten* Parametern aufgerufen, für die bereits eine visuelle Struktur vorhanden ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn ein Aufrufen von [**idcompositionsurface:: beginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) die letzte Aktion war:



| Aufrufen dieser Methode:                                    | Gibt folgenden Wert zurück:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert** |
| [**"EndDraw"**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**Suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                             |
| [**Resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert** |



 

Bei einem Aufrufen von " [**idcompositionsurface:: suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) " handelt es sich um die letzte Aktion:



| Aufrufen dieser Methode:                                    | Gibt folgenden Wert zurück:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert** |
| [**"EndDraw"**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**Suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert** |
| [**Resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ OK                                             |



 

Wenn ein Aufrufen von [**idcompositionsurface:: resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) die letzte Aktion war:



| Aufrufen dieser Methode:                                    | Gibt folgenden Wert zurück:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **dcomposition- \_ Fehler \_ Oberfläche \_ wird \_ gerendert**  |
| [**"EndDraw"**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                              |
| [**Suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                              |
| [**Resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **dcomposition- \_ Fehler \_ Oberfläche, die \_ \_ gerendert wird.** |



 

Wenn ein Aufrufen von [**idcompositionsurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) die letzte Aktion war:



| Aufrufen dieser Methode:                                    | Gibt folgenden Wert zurück:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ OK                                                   |
| [**"EndDraw"**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.** |
| [**Suspenddraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.** |
| [**Resumedraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **dcomposition \_ - \_ Fehler \_ Oberfläche \_ wird nicht \_ gerendert.** |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Dcomp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Directcomposition-Referenz](reference.md)
</dt> </dl>

 

