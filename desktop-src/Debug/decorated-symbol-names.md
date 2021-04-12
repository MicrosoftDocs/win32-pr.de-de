---
description: Der ergänzte Symbol Name enthält Zeichen, die unterscheiden, wie ein öffentliches Symbol deklariert wurde.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Ergänzte Symbol Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482731"
---
# <a name="decorated-symbol-names"></a><span data-ttu-id="4f2db-103">Ergänzte Symbol Namen</span><span class="sxs-lookup"><span data-stu-id="4f2db-103">Decorated Symbol Names</span></span>

<span data-ttu-id="4f2db-104">Der ergänzte Symbol Name enthält Zeichen, die unterscheiden, wie ein öffentliches Symbol deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="4f2db-104">A decorated symbol name includes characters that distinguish how a public symbol has been declared.</span></span> <span data-ttu-id="4f2db-105">Für \_ \_ StdCall-Funktionen enthalten Namen das Zeichen "@" und eine Dezimalzahl, die die Anzahl von Bytes in den Funktionsparametern angibt.</span><span class="sxs-lookup"><span data-stu-id="4f2db-105">For \_\_stdcall functions, names include the "@" character and a decimal number that specifies the number of bytes in its function parameters.</span></span> <span data-ttu-id="4f2db-106">Der ergänzte Name der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion lautet z. b LoadLibrary@4 ..</span><span class="sxs-lookup"><span data-stu-id="4f2db-106">For example, the decorated name of the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is LoadLibrary@4.</span></span> <span data-ttu-id="4f2db-107">Für C++-Funktionen ist die namens Ergänzung komplexer und unterscheidet sich von Compiler zu Compiler.</span><span class="sxs-lookup"><span data-stu-id="4f2db-107">For C++ functions the name decoration is more complex and varies from compiler to compiler.</span></span>

<span data-ttu-id="4f2db-108">Um den nicht ergänzten Symbolnamen abzurufen, verwenden Sie die [**undecoratesymbolname**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4f2db-108">To retrieve the undecorated symbol name, use the [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) function.</span></span> <span data-ttu-id="4f2db-109">Sie können auch die [**symabtoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion aufzurufen, um anzufordern, dass der Symbol Handler immer Symbole mit nicht ergänzten Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4f2db-109">Alternatively, you can call the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to request that the symbol handler always present symbols with undecorated names.</span></span> <span data-ttu-id="4f2db-110">Sie müssen diese Option vor dem Laden der Symbole festlegen, da der Symbol Handler die Symbol namens Tabellen zur Ladezeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f2db-110">You must set this option before loading the symbols because the symbol handler creates the symbol name tables at load time.</span></span>

 

 
