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
# <a name="wm_tablet_querysystemgesturestatus-message"></a><span data-ttu-id="96f1c-103">WM- \_ Tablet \_ querysystemgesturestatus-Meldung</span><span class="sxs-lookup"><span data-stu-id="96f1c-103">WM\_TABLET\_QUERYSYSTEMGESTURESTATUS message</span></span>

<span data-ttu-id="96f1c-104">Wird gesendet, wenn das System ein Fenster anfordert, welche System Gesten Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="96f1c-104">Sent when the system asks a window which system gestures it would like to receive.</span></span>


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a><span data-ttu-id="96f1c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="96f1c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96f1c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96f1c-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96f1c-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="96f1c-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="96f1c-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96f1c-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96f1c-109">Ein-Punktwert, der die Bildschirm Koordinaten darstellt.</span><span class="sxs-lookup"><span data-stu-id="96f1c-109">A point value that represents the screen coordinates.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96f1c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96f1c-110">Remarks</span></span>

<span data-ttu-id="96f1c-111">Wenn Sie diese Meldung verarbeiten, können Sie schnelle Stift Bewegungen für Fensterbereiche dynamisch deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="96f1c-111">By handling this message, you can dynamically disable flicks for regions of a window.</span></span>

> [!Note]  
> <span data-ttu-id="96f1c-112">Der *LPARAM* -Parameter kann mit den Makros und in x-Koordinaten und y-Koordinaten konvertiert werden `GET_X_LPARAM` `GET_Y_LPARAM` .</span><span class="sxs-lookup"><span data-stu-id="96f1c-112">The *lParam* can be converted to x-coordinates and y-coordinates by using the `GET_X_LPARAM` and `GET_Y_LPARAM` macros.</span></span>

 

<span data-ttu-id="96f1c-113">Standardmäßig empfängt das Fenster alle systemgesten-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="96f1c-113">By default, your window will receive all system gesture events.</span></span> <span data-ttu-id="96f1c-114">Sie können auswählen, welche Ereignisse das Fenster empfangen soll und welche Ereignisse Sie deaktivieren möchten, indem Sie in der **WndProc** auf die " **WM \_ Tablet \_ querysystemgesturestatus** "-Meldung Antworten.</span><span class="sxs-lookup"><span data-stu-id="96f1c-114">You can choose which events you would like your window to receive and which events you would like disabled by responding to the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message in your **WndProc**.</span></span> <span data-ttu-id="96f1c-115">Die " **WM \_ Tablet \_ querysystemgesturestatus** "-Meldung wird in "tpcshrd. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="96f1c-115">The **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message is defined in tpcshrd.h.</span></span> <span data-ttu-id="96f1c-116">Die Werte zum Aktivieren und Deaktivieren von System-Tablet System Gesten werden auch in tpcshrd. h wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="96f1c-116">The values to enable and disable system tablet system gestures are also defined in tpcshrd.h as follows:</span></span>

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
> <span data-ttu-id="96f1c-117">Durch die Deaktivierung von Press und Hold wird die Reaktionsfähigkeit für Mausklicks verbessert, da diese Funktion eine Wartezeit zur Unterscheidung zwischen den beiden Vorgängen erzeugt.</span><span class="sxs-lookup"><span data-stu-id="96f1c-117">Disabling press and hold will improve responsiveness for mouse clicks because this functionality creates a wait time to distinguish between the two operations.</span></span>

 

<span data-ttu-id="96f1c-118">Gehen Sie vorsichtig vor, wenn Sie die **WM- \_ Tablet- \_ querysystemgesturestatus** -Meldung verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="96f1c-118">Use caution when handling the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message.</span></span> <span data-ttu-id="96f1c-119">**WM \_ Das Tablet \_ querysystemgesturestatus** wird mithilfe der [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="96f1c-119">**WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** is passed using the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="96f1c-120">Wenn Sie Methoden für eine COM-Schnittstelle aufzurufen, muss sich dieses Objekt innerhalb desselben Prozesses befinden.</span><span class="sxs-lookup"><span data-stu-id="96f1c-120">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="96f1c-121">Andernfalls löst com eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="96f1c-121">If not, COM throws an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="96f1c-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96f1c-122">Examples</span></span>

<span data-ttu-id="96f1c-123">Im folgenden Beispiel wird gezeigt, wie Sie schnelle Stift Bewegungen für einen Bereich mithilfe von WM \_ Tablet \_ querysystemgesturestatus deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="96f1c-123">The following example shows how to disable flicks for a region using WM\_TABLET\_QUERYSYSTEMGESTURESTATUS.</span></span>


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



<span data-ttu-id="96f1c-124">Im folgenden Beispiel wird gezeigt, wie verschiedene schnelle Stift Bewegungen-Funktionen für ein gesamtes Fenster deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="96f1c-124">The following example shows how to disable various flicks features for an entire window.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="96f1c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96f1c-125">Requirements</span></span>



| <span data-ttu-id="96f1c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96f1c-126">Requirement</span></span> | <span data-ttu-id="96f1c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="96f1c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96f1c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96f1c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="96f1c-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96f1c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="96f1c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96f1c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="96f1c-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96f1c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="96f1c-132">Header</span><span class="sxs-lookup"><span data-stu-id="96f1c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f1c-133"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f1c-133"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
