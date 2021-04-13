---
title: WM_GESTURE Meldung (Winuser. h)
description: Übergibt Informationen über eine Geste.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- Windows-Fingereingabe für WM_GESTURE Meldung
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392052"
---
# <a name="wm_gesture-message"></a>WM- \_ Gesten Meldung

Übergibt Informationen über eine Geste.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Stellt Informationen bereit, mit denen der Gesten Befehl und Gesten spezifische Argument Werte identifiziert werden. Dabei handelt es sich um dieselben Informationen, die im **ullarguments** -Member der [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) -Struktur weitergegeben werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Stellt ein Handle für Informationen bereit, mit denen der Gesten Befehl und Gesten spezifische Argument Werte identifiziert werden. Diese Informationen werden abgerufen, indem [**getgestureinfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

Wenn die Anwendung die Nachricht nicht verarbeitet, muss Sie [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden. Wenn Sie dies nicht tun, wird der Arbeitsspeicher von der Anwendung nicht mehr verwendet, da der Fingereingabe Handle nicht geschlossen und zugeordneter Prozess Speicher nicht freigegeben wird.

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle sind die unterstützten Gesten Befehle aufgeführt.



| Gesten-ID            | Wert (*dwID*) | BESCHREIBUNG                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GID- \_ Anfang**        | 1              | Gibt an, dass eine generische Geste beginnt.                                                                                                                                                                                                                                            |
| **GID- \_ Ende**          | 2              | Gibt eine generische Gesten Ende an.                                                                                                                                                                                                                                                     |
| **GID- \_ Zoom**         | 3              | Gibt den Zoom-, Zoom-oder Zoomvorgang an. Die erste **gid \_ Zoom** -Befehls Meldung beginnt einen Zoom, bewirkt aber keine Vergrößerung. Der zweite **gid- \_ Zoom** Befehl löst einen Zoom in Relation zum Zustand aus, der im ersten **gid- \_ Zoom** enthalten ist.                                    |
| **GID- \_ Pan**          | 4              | Gibt an, dass schwenken oder Schwenken schwenken. Der erste Befehl mit der **gid \_ Pan** gibt an, dass ein Schwenken gestartet wird, führt aber keine schwenken aus. Mit der zweiten **gid \_ Pan** -Befehls Meldung beginnt die Anwendung mit dem schwenken.                                                                            |
| **GID \_ drehen**       | 5              | Gibt den Drehungs-oder Drehungs Start an. Die erste **gid- \_ Rotation** -Befehls Meldung weist auf einen Drehungs-oder Drehungs Start hin, wird jedoch nicht gedreht. Die zweite **gid \_** -Rotation-Befehls Meldung löst einen Rotations Vorgang in Relation zum Zustand aus, der in der ersten **gid- \_ Drehung** enthalten ist. |
| **GID \_ twofingertap** | 6              | Gibt die zwei-Finger-Tap-Bewegung an.                                                                                                                                                                                                                                                    |
| **GID- \_ pressandtap**  | 7              | Gibt die Bewegung zum Drücken und tippen an.                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Um die Legacy Unterstützung zu aktivieren, müssen Nachrichten mit den Befehlen **gid \_ Begin** und **gid \_ End** Geste mithilfe von [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)weitergeleitet werden.

 

In der folgenden Tabelle sind die Gesten Argumente angegeben, die in den *LPARAM* -und *wParam* -Parametern angegeben werden.



| Gesten-ID            | Geste        | *ullargument*                                                                                                                                                                                                                                                                                                                                                                                            | *ptsLocation* in der [**GESTUREINFO**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) -Struktur                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID- \_ Zoom**         | Vergrößern/verkleinern    | Gibt den Abstand zwischen den beiden Punkten an.                                                                                                                                                                                                                                                                                                                                                           | Gibt den Mittelpunkt des Zoom Punkts an.                                                                                 |
| **GID- \_ Pan**          | Schwenken            | Gibt den Abstand zwischen den beiden Punkten an.                                                                                                                                                                                                                                                                                                                                                           | Gibt die aktuelle Position der schwenken an.                                                                        |
| **GID \_ drehen**       | Drehen (Pivot) | Gibt den Drehwinkel an, wenn **das \_ FL** -Startflag festgelegt ist. Andernfalls ist dies die Winkel Änderung, seit die Drehung gestartet wurde. Dies wird signiert, um die Richtung der Drehung anzugeben. Verwenden Sie den gid-Winkel [**\_ Drehung \_ \_ von \_ Argument**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) und [**gid \_ Drehung \_ \_ in \_ Argument**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) Makros, um den Winkelwert zu erhalten und festzulegen. | Dies gibt den Mittelpunkt der Drehung an, bei dem es sich um den stationären Punkt handelt, um den das Zielobjekt gedreht wird. |
| **GID \_ twofingertap** | Zwei-Finger-Tippen | Gibt den Abstand zwischen den beiden Fingern an.                                                                                                                                                                                                                                                                                                                                                          | Gibt die Mitte der beiden Finger an.                                                                          |
| **GID- \_ pressandtap**  | Drücken und tippen  | Gibt das Delta zwischen dem ersten und dem zweiten Finger an. Dieser Wert wird in den unteren 32 Bits von *ullargument* in einer **Punkt** Struktur gespeichert.                                                                                                                                                                                                                                             | Gibt die Position an, an der der erste Finger angezeigt wird.                                                       |



 

> [!Note]  
> Alle Entfernungen und Positionen werden in physischen Bildschirm Koordinaten bereitgestellt.

 

> [!Note]  
> Die Parameter " *dwID* " und " *ullargument* " sollten nur als begleitende gid-Befehle angesehen werden \_ \* und sollten nicht von Anwendungen geändert werden.

 

## <a name="examples"></a>Beispiele

Der folgende Code veranschaulicht das Abrufen von Gesten spezifischen Informationen, die dieser Nachricht zugeordnet sind.

> [!Note]  
> Sie sollten unbehandelte Nachrichten immer an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) weiterleiten und das Eingabe Handle für Eingaben für Nachrichten schließen, die Sie mit einem Rückruf von [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle)verarbeiten. In diesem Beispiel wird das Standardverhalten des Gesten Handlers unterdrückt, da das TOUCHINPUT-Handle in jedem der Gesten Fälle geschlossen wird. Wenn Sie die Fälle im obigen Code für nicht behandelte Nachrichten entfernt haben, verarbeitet der Standard Gesten Handler die Nachrichten, indem er im Standardfall an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca) weitergeleitet wird.

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Benachrichtigungen](notifications.md)
</dt> <dt>

[Programmier Handbuch für Windows-Touchgesten](guide-multi-touch-gestures.md)
</dt> </dl>

 

