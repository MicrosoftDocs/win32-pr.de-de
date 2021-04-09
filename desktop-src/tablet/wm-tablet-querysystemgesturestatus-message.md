---
description: Wird gesendet, wenn das System ein Fenster anfordert, welche System Gesten Sie erhalten möchten.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: WM_TABLET_QUERYSYSTEMGESTURESTATUS Meldung (tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862484"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>WM- \_ Tablet \_ querysystemgesturestatus-Meldung

Wird gesendet, wenn das System ein Fenster anfordert, welche System Gesten Sie erhalten möchten.


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein-Punktwert, der die Bildschirm Koordinaten darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Meldung verarbeiten, können Sie schnelle Stift Bewegungen für Fensterbereiche dynamisch deaktivieren.

> [!Note]  
> Der *LPARAM* -Parameter kann mit den Makros und in x-Koordinaten und y-Koordinaten konvertiert werden `GET_X_LPARAM` `GET_Y_LPARAM` .

 

Standardmäßig empfängt das Fenster alle systemgesten-Ereignisse. Sie können auswählen, welche Ereignisse das Fenster empfangen soll und welche Ereignisse Sie deaktivieren möchten, indem Sie in der **WndProc** auf die " **WM \_ Tablet \_ querysystemgesturestatus** "-Meldung Antworten. Die " **WM \_ Tablet \_ querysystemgesturestatus** "-Meldung wird in "tpcshrd. h" definiert. Die Werte zum Aktivieren und Deaktivieren von System-Tablet System Gesten werden auch in tpcshrd. h wie folgt definiert:

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> Durch die Deaktivierung von Press und Hold wird die Reaktionsfähigkeit für Mausklicks verbessert, da diese Funktion eine Wartezeit zur Unterscheidung zwischen den beiden Vorgängen erzeugt.

 

Gehen Sie vorsichtig vor, wenn Sie die **WM- \_ Tablet- \_ querysystemgesturestatus** -Meldung verarbeiten. **WM \_ Das Tablet \_ querysystemgesturestatus** wird mithilfe der [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion übergeben. Wenn Sie Methoden für eine COM-Schnittstelle aufzurufen, muss sich dieses Objekt innerhalb desselben Prozesses befinden. Andernfalls löst com eine Ausnahme aus.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie schnelle Stift Bewegungen für einen Bereich mithilfe von WM \_ Tablet \_ querysystemgesturestatus deaktivieren.


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



Im folgenden Beispiel wird gezeigt, wie verschiedene schnelle Stift Bewegungen-Funktionen für ein gesamtes Fenster deaktiviert werden.


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
