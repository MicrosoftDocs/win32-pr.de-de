---
title: Aufrufen des Mittel l-Compilers
description: Der mittlerer l-Compiler kann Code für verschiedene Plattformen und System Releases generieren. Weitere Informationen zu vorgeschlagenen Switches und zum Generieren von Code, der für eine bestimmte Version optimiert ist, finden Sie unter/Target.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- Mittel l compilermittell, aufrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "106341270"
---
# <a name="invoking-the-midl-compiler"></a><span data-ttu-id="69011-105">Aufrufen des Mittel l-Compilers</span><span class="sxs-lookup"><span data-stu-id="69011-105">Invoking the MIDL Compiler</span></span>

<span data-ttu-id="69011-106">Der mittlerer l-Compiler kann Code für verschiedene Plattformen und System Releases generieren.</span><span class="sxs-lookup"><span data-stu-id="69011-106">The MIDL compiler can generate code for different platforms and system releases.</span></span> <span data-ttu-id="69011-107">Weitere Informationen zu vorgeschlagenen Switches und zum Generieren von Code, der für eine bestimmte Version optimiert ist, finden Sie unter [**/target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="69011-107">Consult the [**/target**](-target.md) switch to learn more about suggested switches and how to generate code optimized for a particular release.</span></span>

<span data-ttu-id="69011-108">Führen Sie den-compilercompiler über die Befehlszeile mit dem folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="69011-108">Run the MIDL compiler from the command line using the following command:</span></span>

<span data-ttu-id="69011-109">**Dateiname. idl** für **mittlere** *< ***Optionen*** >*</span><span class="sxs-lookup"><span data-stu-id="69011-109">**midl** *<***options***>* **filename.idl**</span></span>

<span data-ttu-id="69011-110">Where- *< ***Optionen*** >* stellen die Befehlszeilenoptionen dar, die Sie verwenden möchten, und filename. idl ist der Name der zu kompilierenden Mittell-Datei.</span><span class="sxs-lookup"><span data-stu-id="69011-110">where *<***options***>* represents the command-line options you want to use, and Filename.idl is the name of the MIDL file to compile.</span></span>

<span data-ttu-id="69011-111">Eine vollständige Liste der kompil-Compilerschalter und-Optionen ist verfügbar, wenn Sie den Mittelwert Compiler [**/Help**](-help-.md) und/? verwenden.</span><span class="sxs-lookup"><span data-stu-id="69011-111">A complete listing of MIDL compiler switches and options is available when you use the MIDL compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="69011-112">Mikro.</span><span class="sxs-lookup"><span data-stu-id="69011-112">switches.</span></span> <span data-ttu-id="69011-113">Die Schalter sind nach Kategorien organisiert.</span><span class="sxs-lookup"><span data-stu-id="69011-113">The switches are organized by categories.</span></span> <span data-ttu-id="69011-114">Weitere Informationen finden Sie in der [Referenz zur Mittel l-Command-Line](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="69011-114">For details, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

> [!NOTE]
> <span data-ttu-id="69011-115">Das neue globale Flag **$ (mittlerer l- \_ Optimierung)** ist in Win32. MAK vorhanden.</span><span class="sxs-lookup"><span data-stu-id="69011-115">The new global flag **$(MIDL\_OPTIMIZATION)** exists in win32.mak.</span></span> <span data-ttu-id="69011-116">Wenn eine IDL-Datei mit diesem Flag kompiliert wird, kann der generierte Stub die neuesten auf der angegebenen Plattform verfügbaren RPC-Features nutzen und potenziell die Leistung und Stabilität der Anwendung verbessern.</span><span class="sxs-lookup"><span data-stu-id="69011-116">When an .idl file is compiled using this flag, the generated stub can utilize the latest RPC features available on the specified platform, and potentially improve the application's performance and stability.</span></span> <span data-ttu-id="69011-117">Es wird empfohlen, dass Anwendungen dieses Flag bei der Verwendung von "Mittel l" verwenden.</span><span class="sxs-lookup"><span data-stu-id="69011-117">It's recommended that applications use this flag when using MIDL.</span></span>
>
> <span data-ttu-id="69011-118">**Mittel l** **$ (mittlere \_ Optimierung)** **...**</span><span class="sxs-lookup"><span data-stu-id="69011-118">**midl** **$(MIDL\_OPTIMIZATION)** **...**</span></span>