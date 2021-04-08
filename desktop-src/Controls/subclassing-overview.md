---
title: Subclassingsteuerelemente
description: Wenn ein Steuerelement fast alles hat, was Sie möchten, aber Sie benötigen noch ein paar weitere Features, können Sie Funktionen zum ursprünglichen Steuerelement ändern oder hinzufügen, indem Sie es Unterklassen.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039706"
---
# <a name="subclassing-controls"></a><span data-ttu-id="c7691-103">Subclassingsteuerelemente</span><span class="sxs-lookup"><span data-stu-id="c7691-103">Subclassing Controls</span></span>

<span data-ttu-id="c7691-104">Wenn ein Steuerelement fast alles hat, was Sie möchten, aber Sie benötigen noch ein paar weitere Features, können Sie Funktionen zum ursprünglichen Steuerelement ändern oder hinzufügen, indem Sie es Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="c7691-104">If a control does almost everything you want, but you need a few more features, you can change or add features to the original control by subclassing it.</span></span> <span data-ttu-id="c7691-105">Eine Unterklasse kann über alle Funktionen einer vorhandenen Klasse sowie über alle zusätzlichen Features verfügen, die Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c7691-105">A subclass can have all the features of an existing class as well as any additional features you want to give it.</span></span>

<span data-ttu-id="c7691-106">In diesem Dokument wird erläutert, wie Unterklassen erstellt werden und wie die folgenden Themen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c7691-106">This document discusses how subclasses are created and includes the following topics.</span></span>

-   [<span data-ttu-id="c7691-107">Unterklassen-Steuerelemente vor ComCtl32.dll Version 6</span><span class="sxs-lookup"><span data-stu-id="c7691-107">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [<span data-ttu-id="c7691-108">Speichern von Benutzerdaten</span><span class="sxs-lookup"><span data-stu-id="c7691-108">Storing User Data</span></span>](#storing-user-data)
    -   [<span data-ttu-id="c7691-109">Nachteile des alten Unterklassen Ansatzes</span><span class="sxs-lookup"><span data-stu-id="c7691-109">Disadvantages of the Old Subclassing Approach</span></span>](#disadvantages-of-the-old-subclassing-approach)
-   [<span data-ttu-id="c7691-110">Unterklassen-Steuerelemente mit ComCtl32.dll Version 6</span><span class="sxs-lookup"><span data-stu-id="c7691-110">Subclassing Controls Using ComCtl32.dll version 6</span></span>](#subclassing-controls-using-comctl32dll-version-6)
    -   [<span data-ttu-id="c7691-111">Setwindowsubclass</span><span class="sxs-lookup"><span data-stu-id="c7691-111">SetWindowSubclass</span></span>](#setwindowsubclass)
    -   [<span data-ttu-id="c7691-112">Getwindowsubclass</span><span class="sxs-lookup"><span data-stu-id="c7691-112">GetWindowSubclass</span></span>](#getwindowsubclass)
    -   [<span data-ttu-id="c7691-113">Removewindowsubclass</span><span class="sxs-lookup"><span data-stu-id="c7691-113">RemoveWindowSubclass</span></span>](#removewindowsubclass)
    -   [<span data-ttu-id="c7691-114">Defsubclassproc</span><span class="sxs-lookup"><span data-stu-id="c7691-114">DefSubclassProc</span></span>](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a><span data-ttu-id="c7691-115">Unterklassen-Steuerelemente vor ComCtl32.dll Version 6</span><span class="sxs-lookup"><span data-stu-id="c7691-115">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>

<span data-ttu-id="c7691-116">Sie können ein-Steuerelement in einer Unterklasse platzieren und Benutzerdaten in einem-Steuerelement speichern.</span><span class="sxs-lookup"><span data-stu-id="c7691-116">You can put a control in a subclass and store user data within a control.</span></span> <span data-ttu-id="c7691-117">Dies geschieht, wenn Sie Versionen von ComCtl32.dll vor Version 6 verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7691-117">You do this when you use versions of ComCtl32.dll prior to version 6.</span></span> <span data-ttu-id="c7691-118">Es gibt einige Nachteile beim Erstellen von Unterklassen mit früheren Versionen von ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="c7691-118">There are some disadvantages in creating subclasses with earlier versions of ComCtl32.dll.</span></span>

<span data-ttu-id="c7691-119">Um ein neues Steuerelement zu erstellen, ist es am besten, mit einem der allgemeinen Windows-Steuerelemente zu beginnen und es an einen bestimmten Bedarf anzupassen.</span><span class="sxs-lookup"><span data-stu-id="c7691-119">To make a new control, it is best to start with one of the Windows common controls and extend it to fit a particular need.</span></span> <span data-ttu-id="c7691-120">Um ein Steuerelement zu erweitern, erstellen Sie ein-Steuerelement, und ersetzen Sie dessen vorhandene Fenster Prozedur durch eine neue.</span><span class="sxs-lookup"><span data-stu-id="c7691-120">To extend a control, create a control and replace its existing window procedure with a new one.</span></span> <span data-ttu-id="c7691-121">Die neue Prozedur fängt die Meldungen des Steuer Elements ab und führt Sie entweder aus oder übergibt sie zur Standard Verarbeitung an die ursprüngliche Prozedur.</span><span class="sxs-lookup"><span data-stu-id="c7691-121">The new procedure intercepts the control's messages and either acts on them or passes them to the original procedure for default processing.</span></span> <span data-ttu-id="c7691-122">Verwenden Sie die Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) " oder " [**setwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) ", um das WndProc-Element des Steuer Elements zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c7691-122">Use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function to replace the WNDPROC of the control.</span></span> <span data-ttu-id="c7691-123">Im folgenden Codebeispiel wird gezeigt, wie ein WndProc ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c7691-123">The following code sample shows how to replace a WNDPROC.</span></span>


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a><span data-ttu-id="c7691-124">Speichern von Benutzerdaten</span><span class="sxs-lookup"><span data-stu-id="c7691-124">Storing User Data</span></span>

<span data-ttu-id="c7691-125">Möglicherweise möchten Sie Benutzerdaten mit einem einzelnen Fenster speichern.</span><span class="sxs-lookup"><span data-stu-id="c7691-125">You might want to store user data with an individual window.</span></span> <span data-ttu-id="c7691-126">Diese Daten können von der neuen Fenster Prozedur verwendet werden, um zu bestimmen, wie das Steuerelement gezeichnet werden soll oder wohin bestimmte Nachrichten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7691-126">This data can be used by the new window procedure to determine how to draw the control or where to send certain messages.</span></span> <span data-ttu-id="c7691-127">Beispielsweise können Sie Daten zum Speichern eines C++-Klassen Zeigers auf die Klasse verwenden, die das Steuerelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7691-127">For example, you might use data to store a C++ class pointer to the class that represents the control.</span></span> <span data-ttu-id="c7691-128">Im folgenden Codebeispiel wird gezeigt, wie [**setprop**](/windows/desktop/api/winuser/nf-winuser-setpropa) zum Speichern von Daten mit einem-Fenster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7691-128">The following code sample shows how to use [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) to store data with a window.</span></span>


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a><span data-ttu-id="c7691-129">Nachteile des alten Unterklassen Ansatzes</span><span class="sxs-lookup"><span data-stu-id="c7691-129">Disadvantages of the Old Subclassing Approach</span></span>

<span data-ttu-id="c7691-130">In der folgenden Liste werden einige Nachteile der Verwendung des zuvor beschriebenen Ansatzes zum Unterklassen eines-Steuer Elements aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7691-130">The following list points out some of the disadvantages of using the previously described approach to subclassing a control.</span></span>

-   <span data-ttu-id="c7691-131">Die Fenster Prozedur kann nur einmal ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c7691-131">The window procedure can only be replaced once.</span></span>
-   <span data-ttu-id="c7691-132">Es ist schwierig, eine Unterklasse zu entfernen, nachdem Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c7691-132">It is difficult to remove a subclass after it is created.</span></span>
-   <span data-ttu-id="c7691-133">Das Zuordnen privater Daten zu einem Fenster ist ineffizient.</span><span class="sxs-lookup"><span data-stu-id="c7691-133">Associating private data with a window is inefficient.</span></span>
-   <span data-ttu-id="c7691-134">Um die nächste Prozedur in einer Unterklassen Kette aufzurufen, können Sie die alte Fenster Prozedur nicht umwandeln und aufrufen, sondern Sie müssen Sie mithilfe der [**callwindowproc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c7691-134">To call the next procedure in a subclass chain, you cannot cast the old window procedure and call it, you must call it by using the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function.</span></span>

## <a name="subclassing-controls-using-comctl32dll-version-6"></a><span data-ttu-id="c7691-135">Unterklassen-Steuerelemente mit ComCtl32.dll Version 6</span><span class="sxs-lookup"><span data-stu-id="c7691-135">Subclassing Controls Using ComCtl32.dll version 6</span></span>

> [!Note]  
> <span data-ttu-id="c7691-136">ComCtl32.dll Version 6 ist nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7691-136">ComCtl32.dll version 6 is Unicode only.</span></span> <span data-ttu-id="c7691-137">Die von ComCtl32.dll Version 6 unterstützten allgemeinen Steuerelemente dürfen nicht mit ANSI-Fenster Prozeduren untergeordnet (oder übergeordnet) werden.</span><span class="sxs-lookup"><span data-stu-id="c7691-137">The common controls supported by ComCtl32.dll version 6 should not be subclassed (or superclassed) with ANSI window procedures.</span></span>

 

<span data-ttu-id="c7691-138">ComCtl32.dll Version 6 enthält vier Funktionen, die das Erstellen von Unterklassen vereinfachen und die zuvor erörterten Nachteile vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c7691-138">ComCtl32.dll version 6 contains four functions that make creating subclasses easier and eliminate the disadvantages previously discussed.</span></span> <span data-ttu-id="c7691-139">Die neuen Funktionen kapseln die Verwaltung, die mit mehreren Sätzen von Verweis Daten verbunden ist. Daher kann sich der Entwickler auf die Programmierfunktionen konzentrieren, nicht auf die Verwaltung von Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="c7691-139">The new functions encapsulate the management involved with multiple sets of reference data, therefore the developer can focus on programming features and not on managing subclasses.</span></span> <span data-ttu-id="c7691-140">Die Unterklassen Funktionen sind:</span><span class="sxs-lookup"><span data-stu-id="c7691-140">The subclassing functions are:</span></span>

-   [<span data-ttu-id="c7691-141">**Setwindowsubclass**</span><span class="sxs-lookup"><span data-stu-id="c7691-141">**SetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [<span data-ttu-id="c7691-142">**Getwindowsubclass**</span><span class="sxs-lookup"><span data-stu-id="c7691-142">**GetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [<span data-ttu-id="c7691-143">**Removewindowsubclass**</span><span class="sxs-lookup"><span data-stu-id="c7691-143">**RemoveWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [<span data-ttu-id="c7691-144">**Defsubclassproc**</span><span class="sxs-lookup"><span data-stu-id="c7691-144">**DefSubclassProc**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a><span data-ttu-id="c7691-145">Setwindowsubclass</span><span class="sxs-lookup"><span data-stu-id="c7691-145">SetWindowSubclass</span></span>

<span data-ttu-id="c7691-146">Diese Funktion wird verwendet, um anfänglich ein Fenster zu Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="c7691-146">This function is used to initially subclass a window.</span></span> <span data-ttu-id="c7691-147">Jede Unterklasse wird durch die Adresse der *pfnsubclass* und ihrer *uidsubclass* eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c7691-147">Each subclass is uniquely identified by the address of the *pfnSubclass* and its *uIdSubclass*.</span></span> <span data-ttu-id="c7691-148">Beide sind Parameter der Funktion [**setwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) .</span><span class="sxs-lookup"><span data-stu-id="c7691-148">Both of these are parameters of the [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) function.</span></span> <span data-ttu-id="c7691-149">Mehrere Unterklassen können dieselbe Unterklassen Prozedur gemeinsam verwenden, und die ID kann jeden-Rückruf identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c7691-149">Several subclasses can share the same subclass procedure and the ID can identify each call.</span></span> <span data-ttu-id="c7691-150">Um Verweis Daten zu ändern, können Sie nachfolgende Aufrufe an **setwindowsubclass** durchführen.</span><span class="sxs-lookup"><span data-stu-id="c7691-150">To change reference data you can make subsequent calls to **SetWindowSubclass**.</span></span> <span data-ttu-id="c7691-151">Der wichtige Vorteil besteht darin, dass jede Unterklassen Instanz über eigene Verweis Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="c7691-151">The important advantage is that each subclass instance has its own reference data.</span></span>

<span data-ttu-id="c7691-152">Die Deklaration einer Unterklassen Prozedur unterscheidet sich geringfügig von einer regulären Fenster Prozedur, da Sie über zwei zusätzliche Datenelemente verfügt: die Unterklassen-ID und die Verweis Daten.</span><span class="sxs-lookup"><span data-stu-id="c7691-152">The declaration of a subclass procedure is slightly different from a regular window procedure because it has two additional pieces of data: the subclass ID and the reference data.</span></span> <span data-ttu-id="c7691-153">Dies wird in den letzten beiden Parametern der folgenden Funktionsdeklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c7691-153">The last two parameters of the following function declaration show this.</span></span>


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



<span data-ttu-id="c7691-154">Jedes Mal, wenn eine Nachricht von der neuen Fenster Prozedur empfangen wird, sind eine Unterklassen-ID und Verweis Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7691-154">Every time a message is received by the new window procedure, a subclass ID and reference data are included.</span></span>

> [!Note]  
> <span data-ttu-id="c7691-155">Alle an die Prozedur weiter gegebenen Zeichen folgen sind Unicode-Zeichen folgen, auch wenn Unicode nicht als Präprozessordefinition angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c7691-155">All strings passed to the procedure are Unicode strings even if Unicode is not specified as a preprocessor definition.</span></span>

 

<span data-ttu-id="c7691-156">Das folgende Beispiel zeigt eine Skeleton-Implementierung einer Fenster Prozedur für ein untergeordnetes Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c7691-156">The following example shows a skeleton implementation of a window procedure for a subclassed control.</span></span>


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="c7691-157">Die Fenster Prozedur kann an das-Steuerelement im " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Handler der Dialogfeld Prozedur angefügt werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7691-157">The window procedure can be attached to the control in the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) handler of the dialog procedure, as shown in the following example.</span></span>


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a><span data-ttu-id="c7691-158">Getwindowsubclass</span><span class="sxs-lookup"><span data-stu-id="c7691-158">GetWindowSubclass</span></span>

<span data-ttu-id="c7691-159">Diese Funktion Ruft Informationen zu einer Unterklasse ab.</span><span class="sxs-lookup"><span data-stu-id="c7691-159">This function retrieves information about a subclass.</span></span> <span data-ttu-id="c7691-160">Beispielsweise können Sie [**getwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) verwenden, um auf die Verweis Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c7691-160">For example, you can use [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) to access the reference data.</span></span>

### <a name="removewindowsubclass"></a><span data-ttu-id="c7691-161">Removewindowsubclass</span><span class="sxs-lookup"><span data-stu-id="c7691-161">RemoveWindowSubclass</span></span>

<span data-ttu-id="c7691-162">Diese Funktion entfernt Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="c7691-162">This function removes subclasses.</span></span> <span data-ttu-id="c7691-163">[**Removewindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in Kombination mit [**setwindowsubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) ermöglicht das dynamische Hinzufügen und Entfernen von Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="c7691-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combination with [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) allows you to dynamically add and remove subclasses.</span></span>

### <a name="defsubclassproc"></a><span data-ttu-id="c7691-164">Defsubclassproc</span><span class="sxs-lookup"><span data-stu-id="c7691-164">DefSubclassProc</span></span>

<span data-ttu-id="c7691-165">Die [**defsubclassproc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) -Funktion Ruft den nächsten Handler in der Unterklassen Kette auf.</span><span class="sxs-lookup"><span data-stu-id="c7691-165">The [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) function calls the next handler in the subclass chain.</span></span> <span data-ttu-id="c7691-166">Die-Funktion ruft auch die richtige ID und Verweis Daten ab und übergibt die Informationen an die nächste Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="c7691-166">The function also retrieves the proper ID and reference data and passes the information to the next window procedure.</span></span>

 

 