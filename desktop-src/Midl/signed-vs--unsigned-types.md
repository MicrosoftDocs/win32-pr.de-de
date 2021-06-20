---
title: Signierte und nicht signierte Typen (MIDL)
description: Erfahren Sie mehr über signierte und nicht signierte Typen in MIDL. Compiler, die unterschiedliche Standardtypen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- -Datentypen MIDL, signed und unsigned
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407383"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="c4d5d-105">Signierte und nicht signierte Typen (MIDL)</span><span class="sxs-lookup"><span data-stu-id="c4d5d-105">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="c4d5d-106">Compiler, die unterschiedliche Standardwerte für signierte und nicht signierte Typen verwenden, können Softwarefehler in Ihrer verteilten Anwendung verursachen.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-106">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="c4d5d-107">Sie können diese Probleme vermeiden, indem Sie Ihre Zeichentypen explizit als signiert oder nicht signiert deklarieren.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-107">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="c4d5d-108">Beachten Sie, dass DCE-IDL-Compiler das Schlüsselwort mit [**Vorzeichen**](signed.md)nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-108">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="c4d5d-109">Daher ist dieses Feature nicht verfügbar, wenn Sie den MIDL-Compiler/osf-Switch verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-109">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="c4d5d-110">MIDL definiert den [**kleinen**](small.md) Typ so, dass er das gleiche Standardzeichen wie der [**char-Typ**](char-idl.md) im C-Zielcompiler verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-110">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="c4d5d-111">Wenn der Compiler davon ausgeht, dass **char** nicht signiert ist, wird **small** auch als unsigned definiert.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-111">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="c4d5d-112">Mit vielen C-Compilern können Sie die Standardeinstellung als Befehlszeilenoption ändern.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-112">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="c4d5d-113">Beispielsweise ändert die Befehlszeilenoption **/J** in der Microsoft Visual C++ Entwicklungsumgebung das Standardzeichen von **char** von signed in unsigned.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-113">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="c4d5d-114">Sie können auch das Vorzeichen von Variablen vom Typ [**char**](char-idl.md) und [**small**](small.md) mit dem MIDL-Compilerbefehlszeilenschalter [**/char**](-char.md)steuern.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-114">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="c4d5d-115">Mit diesem Schalter können Sie das Standardzeichen angeben, das vom Compiler verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-115">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="c4d5d-116">Der MIDL-Compiler deklariert explizit  das Vorzeichen aller char-Typen, die nicht mit ihrem C-Compilerstandardtyp in der generierten Headerdatei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-116">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




