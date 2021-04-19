---
title: Aktivieren von Strict
description: Wenn Sie das Strict-Symbol definieren, aktivieren Sie Features, die beim Deklarieren und Verwenden von Typen mehr Sorgfalt erfordern.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "106351186"
---
# <a name="enabling-strict"></a><span data-ttu-id="918e6-103">Aktivieren von Strict</span><span class="sxs-lookup"><span data-stu-id="918e6-103">Enabling STRICT</span></span>

<span data-ttu-id="918e6-104">Wenn Sie das **Strict** -Symbol definieren, aktivieren Sie Features, die beim Deklarieren und Verwenden von Typen mehr Sorgfalt erfordern.</span><span class="sxs-lookup"><span data-stu-id="918e6-104">When you define the **STRICT** symbol, you enable features that require more care in declaring and using types.</span></span> <span data-ttu-id="918e6-105">Dies hilft Ihnen beim Schreiben von portablen Code.</span><span class="sxs-lookup"><span data-stu-id="918e6-105">This helps you write more portable code.</span></span> <span data-ttu-id="918e6-106">Dadurch wird auch die Debugzeit reduziert.</span><span class="sxs-lookup"><span data-stu-id="918e6-106">This extra care will also reduce your debugging time.</span></span> <span data-ttu-id="918e6-107">Durch das Aktivieren von **Strict** werden bestimmte Datentypen definiert, sodass der Compiler keine Zuweisung von einem Typ zu einem anderen ohne explizite Umwandlung zulässt.</span><span class="sxs-lookup"><span data-stu-id="918e6-107">Enabling **STRICT** redefines certain data types so that the compiler does not permit assignment from one type to another without an explicit cast.</span></span> <span data-ttu-id="918e6-108">Dies ist insbesondere bei Windows-Code hilfreich.</span><span class="sxs-lookup"><span data-stu-id="918e6-108">This is especially helpful with Windows code.</span></span> <span data-ttu-id="918e6-109">Fehler beim Übergeben von Datentypen werden zur Kompilierzeit gemeldet, anstatt schwerwiegende Fehler zur Laufzeit zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="918e6-109">Errors in passing data types are reported at compile time instead of causing fatal errors at run time.</span></span>

<span data-ttu-id="918e6-110">Bei Visual C++ ist die **strikte** Typüberprüfung standardmäßig definiert.</span><span class="sxs-lookup"><span data-stu-id="918e6-110">With Visual C++, **STRICT** type checking is defined by default.</span></span>

<span data-ttu-id="918e6-111">Um **Strict** für eine Datei zu definieren, fügen Sie eine **\# define** -Anweisung ein, bevor Sie Windows. h einschließen:</span><span class="sxs-lookup"><span data-stu-id="918e6-111">To define **STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define STRICT
#include <windows.h>
```



<span data-ttu-id="918e6-112">Wenn **Strict** definiert ist, ändern sich die [Datentyp](windows-data-types.md) Definitionen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="918e6-112">When **STRICT** is defined, [data type](windows-data-types.md) definitions change as follows:</span></span>

-   <span data-ttu-id="918e6-113">Bestimmte handle-Typen werden so definiert, dass Sie sich gegenseitig ausschließen. Beispielsweise können Sie kein **HWND** übergeben, in dem ein **hdc** -Typargument erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="918e6-113">Specific handle types are defined to be mutually exclusive; for example, you will not be able to pass an **HWND** where an **HDC** type argument is required.</span></span> <span data-ttu-id="918e6-114">Ohne **strikte** werden alle Handles als **handle** definiert, sodass der Compiler nicht verhindert, dass Sie einen Typ von Handle verwenden, wenn ein anderer Typ erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="918e6-114">Without **STRICT**, all handles are defined as **HANDLE**, so the compiler does not prevent you from using one type of handle where another type is expected.</span></span>
-   <span data-ttu-id="918e6-115">Alle Rückruf Funktionstypen (z. b. Dialog Prozeduren, Fenster Prozeduren und Hook-Prozeduren) werden mit vollständigen Prototypen definiert.</span><span class="sxs-lookup"><span data-stu-id="918e6-115">All callback function types (such as dialog procedures, window procedures, and hook procedures) are defined with full prototypes.</span></span> <span data-ttu-id="918e6-116">Dadurch wird verhindert, dass Rückruf Funktionen mit falschen Parameterlisten deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="918e6-116">This prevents you from declaring callback functions with incorrect parameter lists.</span></span>
-   <span data-ttu-id="918e6-117">Parameter-und Rückgabe Werttypen, die einen generischen Zeiger verwenden sollten, werden als **LPVOID** anstelle von **LPSTR** oder einem anderen Zeigertyp deklariert.</span><span class="sxs-lookup"><span data-stu-id="918e6-117">Parameter and return value types that should use a generic pointer are declared correctly as **LPVOID** instead of as **LPSTR** or another pointer type.</span></span>
-   <span data-ttu-id="918e6-118">Die [**comstat**](/windows/desktop/api/winbase/ns-winbase-comstat) -Struktur wird gemäß dem ANSI-Standard deklariert.</span><span class="sxs-lookup"><span data-stu-id="918e6-118">The [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) structure is declared according to the ANSI standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="918e6-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="918e6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="918e6-120">Deaktivieren von Strict</span><span class="sxs-lookup"><span data-stu-id="918e6-120">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="918e6-121">Strikte Konformität</span><span class="sxs-lookup"><span data-stu-id="918e6-121">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 
