---
title: Signierte und unsignierte Typen (Mittel l)
description: Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- Datentypen-Mittel l, signiert und unsigniert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391358"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="2f532-104">Signierte und unsignierte Typen (Mittel l)</span><span class="sxs-lookup"><span data-stu-id="2f532-104">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="2f532-105">Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="2f532-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="2f532-106">Sie können diese Probleme vermeiden, indem Sie die Zeichen Typen explizit als signiert oder unsigniert deklarieren.</span><span class="sxs-lookup"><span data-stu-id="2f532-106">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="2f532-107">Beachten Sie, dass DCE-IDL-Compiler das Schlüsselwort [**Signed**](signed.md)nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="2f532-107">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="2f532-108">Diese Funktion ist daher nicht verfügbar, wenn Sie den Mittelwert Compiler/**eines Zertifikats** -Schalter verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f532-108">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="2f532-109">In der mittleren l-Datei wird der [**kleine**](small.md) Typ so definiert, dass dasselbe Standard Zeichen wie der [**char**](char-idl.md) -Typ im C-Ziel Compiler übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="2f532-109">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="2f532-110">Wenn der Compiler annimmt, dass **char** nicht signiert ist, wird **Small** auch als unsigned definiert.</span><span class="sxs-lookup"><span data-stu-id="2f532-110">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="2f532-111">Viele C-Compiler ermöglichen es Ihnen, den Standardwert als Befehlszeilenoption zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2f532-111">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="2f532-112">Beispielsweise wird in der Microsoft Visual C++ Entwicklungsumgebung die Befehlszeilenoption **/J** das Standard Zeichen von **char** von signed in unsigned geändert.</span><span class="sxs-lookup"><span data-stu-id="2f532-112">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="2f532-113">Sie können auch das Vorzeichen der Variablen vom Typ " [**char**](char-idl.md) " und " [**Small**](small.md) " mithilfe des Befehls Zeilenschalters " [**/char**](-char.md)" für den Mittelpunkt steuern.</span><span class="sxs-lookup"><span data-stu-id="2f532-113">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="2f532-114">Mithilfe dieses Schalters können Sie das von Ihrem Compiler verwendete standardmäßige Vorzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="2f532-114">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="2f532-115">Der mittlerer l-Compiler deklariert explizit das Vorzeichen aller **char** -Typen, die nicht mit dem Standardtyp des C-Compilers in der generierten Header Datei identisch sind.</span><span class="sxs-lookup"><span data-stu-id="2f532-115">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




