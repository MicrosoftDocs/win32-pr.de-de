---
title: Strikte Konformität
description: Wenn Sie eine strikte Typüberprüfung aktivieren, kann es vorkommen, dass einige Quellcode, die erfolgreich kompiliert werden, Fehlermeldungen erzeugt.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390580"
---
# <a name="strict-compliance"></a><span data-ttu-id="77e5c-103">Strikte Konformität</span><span class="sxs-lookup"><span data-stu-id="77e5c-103">STRICT Compliance</span></span>

<span data-ttu-id="77e5c-104">Wenn Sie eine **strikte** Typüberprüfung aktivieren, kann es vorkommen, dass einige Quellcode, die erfolgreich kompiliert werden, Fehlermeldungen erzeugt.</span><span class="sxs-lookup"><span data-stu-id="77e5c-104">Some source code that compiles successfully might produce error messages when you enable **STRICT** type checking.</span></span> <span data-ttu-id="77e5c-105">In den folgenden Abschnitten werden die Mindestanforderungen beschrieben, mit denen der Code kompiliert werden kann, wenn **Strict** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="77e5c-105">The following sections describe the minimal requirements for making your code compile when **STRICT** is enabled.</span></span> <span data-ttu-id="77e5c-106">Es werden zusätzliche Schritte empfohlen, insbesondere zum Entwickeln von portablen Code.</span><span class="sxs-lookup"><span data-stu-id="77e5c-106">Additional steps are recommended, especially to produce portable code.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="77e5c-107">Allgemeine Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77e5c-107">General Requirements</span></span>

<span data-ttu-id="77e5c-108">Die Hauptanforderung besteht darin, dass Sie korrekte handle-Typen und Funktionszeiger deklarieren müssen, anstatt sich auf allgemeinere Typen zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="77e5c-108">The principal requirement is that you must declare correct handle types and function pointers instead of relying on more general types.</span></span> <span data-ttu-id="77e5c-109">Sie können einen Handles-Typ nicht verwenden, wenn ein anderer Typ erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="77e5c-109">You cannot use one handle type where another is expected.</span></span> <span data-ttu-id="77e5c-110">Dies bedeutet auch, dass Sie möglicherweise Funktions Deklarationen ändern und weitere Typumwandlungen verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="77e5c-110">This also means that you may have to change function declarations and use more type casts.</span></span>

<span data-ttu-id="77e5c-111">Um optimale Ergebnisse zu erzielen, sollte der generische **Handlertyp** nur bei Bedarf verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77e5c-111">For best results, the generic **HANDLE** type should be used only when necessary.</span></span>

## <a name="declaring-functions-within-your-application"></a><span data-ttu-id="77e5c-112">Deklarieren von Funktionen in der Anwendung</span><span class="sxs-lookup"><span data-stu-id="77e5c-112">Declaring Functions Within Your Application</span></span>

<span data-ttu-id="77e5c-113">Stellen Sie sicher, dass alle Anwendungsfunktionen deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="77e5c-113">Make sure all application functions are declared.</span></span> <span data-ttu-id="77e5c-114">Die Platzierung aller Funktions Deklarationen in einer Includedatei wird empfohlen, da Sie problemlos Ihre Deklarationen Scannen und nach Parametern und Rückgabe Typen suchen können, die geändert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="77e5c-114">Placing all function declarations in an include file is recommended because you can easily scan your declarations and look for parameter and return types that should be changed.</span></span>

<span data-ttu-id="77e5c-115">Wenn Sie die **/ZG** -Compileroption verwenden, um Header Dateien für ihre Funktionen zu erstellen, denken Sie daran, dass Sie unterschiedliche Ergebnisse erhalten, je nachdem, ob Sie die **strikte** Typüberprüfung aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="77e5c-115">If you use the **/Zg** compiler option to create header files for your functions, remember that you will get different results depending on whether you have enabled **STRICT** type checking.</span></span> <span data-ttu-id="77e5c-116">Wenn **Strict** deaktiviert ist, generieren alle handle-Typen denselben Basistyp.</span><span class="sxs-lookup"><span data-stu-id="77e5c-116">With **STRICT** disabled, all handle types generate the same base type.</span></span> <span data-ttu-id="77e5c-117">Wenn **Strict** aktiviert ist, generieren Sie unterschiedliche Basis Typen.</span><span class="sxs-lookup"><span data-stu-id="77e5c-117">With **STRICT** enabled, they generate different base types.</span></span> <span data-ttu-id="77e5c-118">Um Konflikte zu vermeiden, müssen Sie die Header Datei bei jeder Aktivierung oder Deaktivierung von **Strict** neu erstellen oder die Header Datei so bearbeiten, dass die Typen **HWND**, **hdc**, **handle** usw. anstelle der Basis Typen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77e5c-118">To avoid conflict, you need to re-create the header file each time you enable or disable **STRICT**, or edit the header file to use the types **HWND**, **HDC**, **HANDLE**, and so on, instead of the base types.</span></span>

<span data-ttu-id="77e5c-119">Alle Funktions Deklarationen, die Sie aus Windows. h in Ihren Quellcode kopiert haben, haben sich möglicherweise geändert, und Ihre lokale Deklaration ist möglicherweise veraltet.</span><span class="sxs-lookup"><span data-stu-id="77e5c-119">Any function declarations that you copied from Windows.h into your source code may have changed, and your local declaration may be out of date.</span></span> <span data-ttu-id="77e5c-120">Entfernen Sie die lokale Deklaration.</span><span class="sxs-lookup"><span data-stu-id="77e5c-120">Remove your local declaration.</span></span>

## <a name="types-that-require-casts"></a><span data-ttu-id="77e5c-121">Typen, die Umwandlungen erfordern</span><span class="sxs-lookup"><span data-stu-id="77e5c-121">Types that Require Casts</span></span>

<span data-ttu-id="77e5c-122">Einige Funktionen verfügen über generische Rückgabe Typen oder Parameter.</span><span class="sxs-lookup"><span data-stu-id="77e5c-122">Some functions have generic return types or parameters.</span></span> <span data-ttu-id="77e5c-123">Beispielsweise gibt die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion Daten zurück, die je nach Kontext eine beliebige Anzahl von Typen sein können.</span><span class="sxs-lookup"><span data-stu-id="77e5c-123">For example, the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function returns data that may be any number of types, depending on the context.</span></span> <span data-ttu-id="77e5c-124">Wenn eine dieser Funktionen in Ihrem Quellcode angezeigt wird, stellen Sie sicher, dass Sie die richtige Typumwandlung verwenden und so spezifisch wie möglich sind.</span><span class="sxs-lookup"><span data-stu-id="77e5c-124">When you see any of these functions in your source code, make sure that you use the correct type cast and that it is as specific as possible.</span></span> <span data-ttu-id="77e5c-125">Die folgende Liste ist ein Beispiel für diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="77e5c-125">The following list is an example of these functions.</span></span>

-   [<span data-ttu-id="77e5c-126">**Loczuweisung**</span><span class="sxs-lookup"><span data-stu-id="77e5c-126">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [<span data-ttu-id="77e5c-127">**GlobalLock**</span><span class="sxs-lookup"><span data-stu-id="77e5c-127">**GlobalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [<span data-ttu-id="77e5c-128">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="77e5c-128">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [<span data-ttu-id="77e5c-129">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="77e5c-129">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [<span data-ttu-id="77e5c-130">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="77e5c-130">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="77e5c-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="77e5c-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [<span data-ttu-id="77e5c-132">**SendDlgItemMess age**</span><span class="sxs-lookup"><span data-stu-id="77e5c-132">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

<span data-ttu-id="77e5c-133">Wenn Sie [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)oder [**SendDlgItemMess**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)aufzurufen, sollten Sie zuerst das Ergebnis in den Typ **uint \_ ptr** umwandeln.</span><span class="sxs-lookup"><span data-stu-id="77e5c-133">When you call [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), or [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), you should first cast the result to type **UINT\_PTR**.</span></span> <span data-ttu-id="77e5c-134">Sie müssen ähnliche Schritte für jede Funktion ausführen, die einen **LRESULT** -oder **Long \_ ptr** -Wert zurückgibt, bei dem das Ergebnis ein Handle enthält.</span><span class="sxs-lookup"><span data-stu-id="77e5c-134">You need to take similar steps for any function that returns an **LRESULT** or **LONG\_PTR** value, where the result contains a handle.</span></span> <span data-ttu-id="77e5c-135">Dies ist für das Schreiben von portablen Code erforderlich, da die Größe eines Handles abhängig von der Windows-Version variiert.</span><span class="sxs-lookup"><span data-stu-id="77e5c-135">This is necessary for writing portable code because the size of a handle varies, depending on the version of Windows.</span></span> <span data-ttu-id="77e5c-136">Durch die Umwandlung von (**uint \_ ptr**) wird eine ordnungsgemäße Konvertierung sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="77e5c-136">The (**UINT\_PTR**) cast ensures proper conversion.</span></span> <span data-ttu-id="77e5c-137">Der folgende Code zeigt ein Beispiel, in dem **SendMessage** ein Handle für einen Pinsel zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="77e5c-137">The following code shows an example in which **SendMessage** returns a handle to a brush:</span></span>


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



<span data-ttu-id="77e5c-138">Der *Parameter "* **upatewindow** " und " **upatewindowex** " wird manchmal verwendet, um einen ganzzahligen Steuerelement Bezeichner (ID) zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="77e5c-138">The **CreateWindow** and **CreateWindowEx** parameter *hmenu* is sometimes used to pass an integer control identifier (ID).</span></span> <span data-ttu-id="77e5c-139">In diesem Fall müssen Sie die ID in einen **HMENU** -Typ umwandeln:</span><span class="sxs-lookup"><span data-stu-id="77e5c-139">In this case, you must cast the ID to an **HMENU** type:</span></span>


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a><span data-ttu-id="77e5c-140">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="77e5c-140">Additional Considerations</span></span>

<span data-ttu-id="77e5c-141">Um die **strikte** Typüberprüfung optimal zu nutzen, gibt es weitere Richtlinien, die Sie befolgen sollten.</span><span class="sxs-lookup"><span data-stu-id="77e5c-141">To get the most benefit from **STRICT** type checking, there are additional guidelines you should follow.</span></span> <span data-ttu-id="77e5c-142">Der Code wird in zukünftigen Versionen von Windows besser portierbar sein, wenn Sie die folgenden Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="77e5c-142">Your code will be more portable in future versions of Windows if you make the following changes.</span></span>

<span data-ttu-id="77e5c-143">Die Typen **wParam**, **LPARAM**, **LRESULT** und **LPVOID** sind *polymorphe Datentypen*.</span><span class="sxs-lookup"><span data-stu-id="77e5c-143">The types **WPARAM**, **LPARAM**, **LRESULT**, and **LPVOID** are *polymorphic data types*.</span></span> <span data-ttu-id="77e5c-144">Sie speichern verschiedene Arten von Daten zu unterschiedlichen Zeitpunkten, auch wenn die **strikte** Typüberprüfung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="77e5c-144">They hold different kinds of data at different times, even when **STRICT** type checking is enabled.</span></span> <span data-ttu-id="77e5c-145">Um den Vorteil der Typüberprüfung zu erhalten, sollten Sie Werte dieser Typen so bald wie möglich umwandeln.</span><span class="sxs-lookup"><span data-stu-id="77e5c-145">To get the benefit of type checking, you should cast values of these types as soon as possible.</span></span> <span data-ttu-id="77e5c-146">(Beachten Sie, dass nachrichtencracker *wParam* und *LPARAM* automatisch für Sie neu umgestalten.)</span><span class="sxs-lookup"><span data-stu-id="77e5c-146">(Note that message crackers automatically recast *wParam* and *lParam* for you in a portable way.)</span></span>

<span data-ttu-id="77e5c-147">Achten Sie besonders darauf, **HMODULE** -und **HINSTANCE** -Typen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="77e5c-147">Take special care to distinguish **HMODULE** and **HINSTANCE** types.</span></span> <span data-ttu-id="77e5c-148">Auch wenn **Strict** aktiviert ist, werden Sie als derselbe Basistyp definiert.</span><span class="sxs-lookup"><span data-stu-id="77e5c-148">Even with **STRICT** enabled, they are defined as the same base type.</span></span> <span data-ttu-id="77e5c-149">Die meisten Verwaltungsfunktionen für Kernelmodule verwenden **HINSTANCE** -Typen, aber es gibt einige Funktionen, die nur **HMODULE** -Typen zurückgeben oder akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="77e5c-149">Most kernel module management functions use **HINSTANCE** types, but there are a few functions that return or accept only **HMODULE** types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77e5c-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77e5c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77e5c-151">Deaktivieren von Strict</span><span class="sxs-lookup"><span data-stu-id="77e5c-151">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="77e5c-152">Aktivieren von Strict</span><span class="sxs-lookup"><span data-stu-id="77e5c-152">Enabling STRICT</span></span>](enabling-strict.md)
</dt> </dl>

 

 