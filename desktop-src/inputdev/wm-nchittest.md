---
title: WM_NCHITTEST Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, um zu bestimmen, welcher Teil des Fensters einer bestimmten Bildschirm Koordinate entspricht.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Tastatur-und Maus Eingaben für WM_NCHITTEST Nachricht
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337315"
---
# <a name="wm_nchittest-message"></a><span data-ttu-id="22290-104">WM- \_ nchittest-Nachricht</span><span class="sxs-lookup"><span data-stu-id="22290-104">WM\_NCHITTEST message</span></span>

<span data-ttu-id="22290-105">Wird an ein Fenster gesendet, um zu bestimmen, welcher Teil des Fensters einer bestimmten Bildschirm Koordinate entspricht.</span><span class="sxs-lookup"><span data-stu-id="22290-105">Sent to a window in order to determine what part of the window corresponds to a particular screen coordinate.</span></span> <span data-ttu-id="22290-106">Dies kann z. b. der Fall sein, wenn der Cursor verschoben wird, wenn eine Maustaste gedrückt oder losgelassen wird, oder als Reaktion auf einen Aufrufen einer Funktion, wie z. b. [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span><span class="sxs-lookup"><span data-stu-id="22290-106">This can happen, for example, when the cursor moves, when a mouse button is pressed or released, or in response to a call to a function such as [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span></span> <span data-ttu-id="22290-107">Wenn die Maus nicht erfasst wird, wird die Nachricht an das Fenster unterhalb des Cursors gesendet.</span><span class="sxs-lookup"><span data-stu-id="22290-107">If the mouse is not captured, the message is sent to the window beneath the cursor.</span></span> <span data-ttu-id="22290-108">Andernfalls wird die Nachricht an das Fenster gesendet, das die Maus erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="22290-108">Otherwise, the message is sent to the window that has captured the mouse.</span></span>

<span data-ttu-id="22290-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="22290-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a><span data-ttu-id="22290-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22290-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22290-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22290-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22290-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22290-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22290-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22290-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22290-114">Das nieder wertige Wort gibt die x-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="22290-114">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="22290-115">Die Koordinate ist relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="22290-115">The coordinate is relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="22290-116">Das höchst wertige Wort gibt die y-Koordinate des Cursors an.</span><span class="sxs-lookup"><span data-stu-id="22290-116">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="22290-117">Die Koordinate ist relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="22290-117">The coordinate is relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22290-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22290-118">Return value</span></span>

<span data-ttu-id="22290-119">Der Rückgabewert der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ist einer der folgenden Werte, der die Position des Cursor-Hot-Spot angibt.</span><span class="sxs-lookup"><span data-stu-id="22290-119">The return value of the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function is one of the following values, indicating the position of the cursor hot spot.</span></span>



| <span data-ttu-id="22290-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="22290-120">Return code/value</span></span>                                                                                                                                    | <span data-ttu-id="22290-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22290-121">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22290-122"><dt>**Htborder**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="22290-122"><dt>**HTBORDER**</dt> <dt>18</dt></span></span> </dl>      | <span data-ttu-id="22290-123">Im Rahmen eines Fensters ohne Größen Anpassungsrahmen.</span><span class="sxs-lookup"><span data-stu-id="22290-123">In the border of a window that does not have a sizing border.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="22290-124"><dt>**Htbottom**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="22290-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span></span> </dl>      | <span data-ttu-id="22290-125">Am unteren horizontalen Rand eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters vertikal zu ändern).</span><span class="sxs-lookup"><span data-stu-id="22290-125">In the lower-horizontal border of a resizable window (the user can click the mouse to resize the window vertically).</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="22290-126"><dt>**Htbottomleft**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="22290-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span></span> </dl>  | <span data-ttu-id="22290-127">In der unteren linken Ecke eines Rahmens eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters diagonal zu ändern).</span><span class="sxs-lookup"><span data-stu-id="22290-127">In the lower-left corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="22290-128"><dt>**Htbottomright**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="22290-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span></span> </dl> | <span data-ttu-id="22290-129">In der unteren rechten Ecke eines Rahmens eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters diagonal zu ändern).</span><span class="sxs-lookup"><span data-stu-id="22290-129">In the lower-right corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="22290-130"><dt>**Htcaption**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="22290-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span></span> </dl>      | <span data-ttu-id="22290-131">In einer Titelleiste.</span><span class="sxs-lookup"><span data-stu-id="22290-131">In a title bar.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="22290-132"><dt>**Htclient**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="22290-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="22290-133">In einem Client Bereich.</span><span class="sxs-lookup"><span data-stu-id="22290-133">In a client area.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="22290-134"><dt>**Htclose**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="22290-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span></span> </dl>       | <span data-ttu-id="22290-135">In einer Schaltfläche **Schließen** .</span><span class="sxs-lookup"><span data-stu-id="22290-135">In a **Close** button.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="22290-136"><dt>**HTError**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="22290-136"><dt>**HTERROR**</dt> <dt>-2</dt></span></span> </dl>       | <span data-ttu-id="22290-137">Auf dem Bildschirm Hintergrund oder in einer Trennlinie zwischen Fenstern (identisch mit " **htnirgendwo**", mit der Ausnahme, dass die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ein Systemsignal erzeugt, um einen Fehler anzugeben).</span><span class="sxs-lookup"><span data-stu-id="22290-137">On the screen background or on a dividing line between windows (same as **HTNOWHERE**, except that the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function produces a system beep to indicate an error).</span></span><br/> |
| <dl> <span data-ttu-id="22290-138"><dt>**Htgrowbox**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="22290-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span></span> </dl>      | <span data-ttu-id="22290-139">In einem Größen Feld (identisch mit " **htsize**").</span><span class="sxs-lookup"><span data-stu-id="22290-139">In a size box (same as **HTSIZE**).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="22290-140"><dt>**Hthelp**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="22290-140"><dt>**HTHELP**</dt> <dt>21</dt></span></span> </dl>        | <span data-ttu-id="22290-141">In einer **Hilfe** Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="22290-141">In a **Help** button.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="22290-142"><dt>**Hthscroll**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="22290-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span></span> </dl>      | <span data-ttu-id="22290-143">In einer horizontalen Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="22290-143">In a horizontal scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="22290-144"><dt>**Htleft**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="22290-144"><dt>**HTLEFT**</dt> <dt>10</dt></span></span> </dl>        | <span data-ttu-id="22290-145">Am linken Rand eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters horizontal zu ändern).</span><span class="sxs-lookup"><span data-stu-id="22290-145">In the left border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="22290-146"><dt>**Htmenu**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="22290-146"><dt>**HTMENU**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="22290-147">In einem Menü.</span><span class="sxs-lookup"><span data-stu-id="22290-147">In a menu.</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="22290-148"><dt>**Htmaxbutton**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="22290-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span></span> </dl>    | <span data-ttu-id="22290-149">Auf der Schaltfläche **maximieren** .</span><span class="sxs-lookup"><span data-stu-id="22290-149">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="22290-150"><dt>**Htminbutton**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="22290-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span></span> </dl>    | <span data-ttu-id="22290-151">Auf der Schaltfläche **minimieren** .</span><span class="sxs-lookup"><span data-stu-id="22290-151">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="22290-152"><dt>**Htnirgendwo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="22290-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span></span> </dl>      | <span data-ttu-id="22290-153">Auf dem Bildschirm Hintergrund oder auf einer Trennlinie zwischen Fenstern.</span><span class="sxs-lookup"><span data-stu-id="22290-153">On the screen background or on a dividing line between windows.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="22290-154"><dt>**Htreduce**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="22290-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="22290-155">Auf der Schaltfläche **minimieren** .</span><span class="sxs-lookup"><span data-stu-id="22290-155">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="22290-156"><dt>**Htright**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="22290-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span></span> </dl>       | <span data-ttu-id="22290-157">Am rechten Rand eines Fensters, das in der Größe geändert werden kann (der Benutzer kann auf die Maus klicken, um die Größe des Fensters horizontal zu ändern).</span><span class="sxs-lookup"><span data-stu-id="22290-157">In the right border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="22290-158"><dt>**Htsize**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="22290-158"><dt>**HTSIZE**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="22290-159">In einem Größen Feld (identisch mit " **htgrowbox**").</span><span class="sxs-lookup"><span data-stu-id="22290-159">In a size box (same as **HTGROWBOX**).</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="22290-160">" <dt>**Htsysmenu**</dt> <dt>3</dt> "</span><span class="sxs-lookup"><span data-stu-id="22290-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="22290-161">In einem Fenstermenü oder in der Schaltfläche **Schließen** in einem untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="22290-161">In a window menu or in a **Close** button in a child window.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="22290-162"><dt>**Httop**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="22290-162"><dt>**HTTOP**</dt> <dt>12</dt></span></span> </dl>         | <span data-ttu-id="22290-163">Am oberen horizontalen Rand eines Fensters.</span><span class="sxs-lookup"><span data-stu-id="22290-163">In the upper-horizontal border of a window.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="22290-164"><dt>**Httopleft**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="22290-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span></span> </dl>     | <span data-ttu-id="22290-165">In der oberen linken Ecke eines Fensterrahmens.</span><span class="sxs-lookup"><span data-stu-id="22290-165">In the upper-left corner of a window border.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="22290-166"><dt>**Httopright**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="22290-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="22290-167">In der oberen rechten Ecke eines Fensterrahmens.</span><span class="sxs-lookup"><span data-stu-id="22290-167">In the upper-right corner of a window border.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="22290-168"><dt>**Httransparent**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="22290-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="22290-169">In einem Fenster, das zurzeit von einem anderen Fenster im gleichen Thread abgedeckt wird (die Nachricht wird an die zugrunde liegenden Fenster im gleichen Thread gesendet, bis eine von Ihnen einen Code zurückgibt, der nicht " **httransparent**" ist).</span><span class="sxs-lookup"><span data-stu-id="22290-169">In a window currently covered by another window in the same thread (the message will be sent to underlying windows in the same thread until one of them returns a code that is not **HTTRANSPARENT**).</span></span><br/>  |
| <dl> <span data-ttu-id="22290-170"><dt>**Htvscroll**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="22290-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span></span> </dl>      | <span data-ttu-id="22290-171">Auf der vertikalen Schiebe Leiste.</span><span class="sxs-lookup"><span data-stu-id="22290-171">In the vertical scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="22290-172"><dt>**Htzoom**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="22290-172"><dt>**HTZOOM**</dt> <dt>9</dt></span></span> </dl>         | <span data-ttu-id="22290-173">Auf der Schaltfläche **maximieren** .</span><span class="sxs-lookup"><span data-stu-id="22290-173">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="22290-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22290-174">Remarks</span></span>

<span data-ttu-id="22290-175">Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:</span><span class="sxs-lookup"><span data-stu-id="22290-175">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="22290-176">Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können).</span><span class="sxs-lookup"><span data-stu-id="22290-176">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="22290-177">Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen.</span><span class="sxs-lookup"><span data-stu-id="22290-177">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="22290-178">Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="22290-178">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22290-179">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22290-179">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="22290-180">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="22290-180">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="22290-181">**Windows Vista:** Wenn Sie benutzerdefinierte Frames erstellen, die die Standard Beschriftungs Schaltflächen enthalten, sollte diese Nachricht zuerst an die [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) -Funktion übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="22290-181">**Windows Vista:** When creating custom frames that include the standard caption buttons, this message should first be passed to the [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="22290-182">Dadurch kann der Desktopfenster-Manager (DWM) Treffer Tests für die Beschriftungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="22290-182">This enables the Desktop Window Manager (DWM) to provide hit-testing for the captions buttons.</span></span> <span data-ttu-id="22290-183">Wenn **DwmDefWindowProc** die Nachricht nicht verarbeitet, ist möglicherweise eine weitere Verarbeitung von **WM \_ nchittest** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22290-183">If **DwmDefWindowProc** does not handle the message, further processing of **WM\_NCHITTEST** may be needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="22290-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22290-184">Requirements</span></span>



| <span data-ttu-id="22290-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22290-185">Requirement</span></span> | <span data-ttu-id="22290-186">Wert</span><span class="sxs-lookup"><span data-stu-id="22290-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22290-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22290-187">Minimum supported client</span></span><br/> | <span data-ttu-id="22290-188">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22290-188">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="22290-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22290-189">Minimum supported server</span></span><br/> | <span data-ttu-id="22290-190">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22290-190">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="22290-191">Header</span><span class="sxs-lookup"><span data-stu-id="22290-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="22290-192"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22290-192"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22290-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22290-193">See also</span></span>

<dl> <dt>

<span data-ttu-id="22290-194">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="22290-194">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22290-195">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="22290-195">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="22290-196">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="22290-196">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="22290-197">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="22290-197">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

<span data-ttu-id="22290-198">**Licher**</span><span class="sxs-lookup"><span data-stu-id="22290-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22290-199">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="22290-199">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="22290-200">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="22290-200">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="22290-201">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="22290-201">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="22290-202">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22290-202">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

