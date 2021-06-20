---
title: Signierte und nicht signierte Typen (RPC)
description: Erfahren Sie mehr über signierte und nicht signierte Typen in RPC. Compiler, die unterschiedliche Standardtypen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406543"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="be650-104">Signierte und nicht signierte Typen (RPC)</span><span class="sxs-lookup"><span data-stu-id="be650-104">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="be650-105">Compiler, die unterschiedliche Standardwerte für signierte und nicht signierte Typen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.</span><span class="sxs-lookup"><span data-stu-id="be650-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="be650-106">Sie können diese Probleme vermeiden, indem Sie Ihre Zeichentypen explizit als **signiert** oder nicht signiert **deklarieren.**</span><span class="sxs-lookup"><span data-stu-id="be650-106">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="be650-107">MIDL definiert den [**kleinen**](/windows/desktop/Midl/small) Typ so, dass er das gleiche Standardzeichen wie der **char-Typ** im C-Zielcompiler verwendet.</span><span class="sxs-lookup"><span data-stu-id="be650-107">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="be650-108">Wenn der Compiler davon ausgeht, dass **char** nicht signiert ist, wird **small** auch als unsigned definiert.</span><span class="sxs-lookup"><span data-stu-id="be650-108">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="be650-109">Mit vielen C-Compilern können Sie die Standardeinstellung als Befehlszeilenoption ändern.</span><span class="sxs-lookup"><span data-stu-id="be650-109">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="be650-110">Beispielsweise ändert die Befehlszeilenoption des Microsoft C-Compilers **/J** das Standardzeichen von **char** von signed in unsigned.</span><span class="sxs-lookup"><span data-stu-id="be650-110">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="be650-111">Sie können auch das Vorzeichen von Variablen vom Typ **char** und **small** mit dem MIDL-Compilerbefehlszeilenschalter [**/char**](/windows/desktop/Midl/-char)steuern.</span><span class="sxs-lookup"><span data-stu-id="be650-111">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="be650-112">Mit diesem Schalter können Sie das Standardzeichen angeben, das vom Compiler verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be650-112">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="be650-113">Der MIDL-Compiler deklariert explizit  das Vorzeichen aller char-Typen, die nicht mit Ihrem C-Compiler-Standardtyp in der generierten Headerdatei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="be650-113">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
