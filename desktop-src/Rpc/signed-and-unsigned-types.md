---
title: Typen mit und ohne Vorzeichen (RPC)
description: Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858606"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="51e29-103">Typen mit und ohne Vorzeichen (RPC)</span><span class="sxs-lookup"><span data-stu-id="51e29-103">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="51e29-104">Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="51e29-104">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="51e29-105">Sie können diese Probleme vermeiden, indem Sie die Zeichen Typen explizit als **signiert** oder **unsigniert** deklarieren.</span><span class="sxs-lookup"><span data-stu-id="51e29-105">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="51e29-106">In der mittleren l-Datei wird der [**kleine**](/windows/desktop/Midl/small) Typ so definiert, dass dasselbe Standard Zeichen wie der **char** -Typ im C-Ziel Compiler übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="51e29-106">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="51e29-107">Wenn der Compiler annimmt, dass **char** nicht signiert ist, wird **Small** auch als unsigned definiert.</span><span class="sxs-lookup"><span data-stu-id="51e29-107">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="51e29-108">Viele C-Compiler ermöglichen es Ihnen, den Standardwert als Befehlszeilenoption zu ändern.</span><span class="sxs-lookup"><span data-stu-id="51e29-108">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="51e29-109">Beispielsweise ändert die Befehlszeilenoption Microsoft C Compiler **/J** das Standard Zeichen von **char** von signed in unsigned.</span><span class="sxs-lookup"><span data-stu-id="51e29-109">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="51e29-110">Sie können auch das Vorzeichen der Variablen vom Typ " **char** " und " **Small** " mithilfe des Befehls Zeilenschalters " [**/char**](/windows/desktop/Midl/-char)" für den Mittelpunkt steuern.</span><span class="sxs-lookup"><span data-stu-id="51e29-110">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="51e29-111">Mithilfe dieses Schalters können Sie das von Ihrem Compiler verwendete standardmäßige Vorzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="51e29-111">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="51e29-112">Der mittlerer l-Compiler deklariert explizit das Vorzeichen aller **char** -Typen, die nicht mit dem Standardtyp des C-Compilers in der generierten Header Datei identisch sind.</span><span class="sxs-lookup"><span data-stu-id="51e29-112">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
