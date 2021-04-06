---
title: Compilerfehler und-Warnungen
description: Bei Verwendung des compl-Compilers können Fehler und Warnungen durch eine nicht ordnungsgemäße Verwendung der Befehls Zeilenschalter oder durch den Inhalt der IDL-und ACF-Dateien verursacht werden.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language-Mittell, Referenz
- Mittel l compilermittell, Fehler
- compilermittell, Fehler
- Fehler-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855192"
---
# <a name="midl-compiler-errors-and-warnings"></a><span data-ttu-id="d78aa-107">Compilerfehler und-Warnungen</span><span class="sxs-lookup"><span data-stu-id="d78aa-107">MIDL Compiler Errors and Warnings</span></span>

<span data-ttu-id="d78aa-108">Bei Verwendung des compl-Compilers können Fehler und Warnungen durch eine nicht ordnungsgemäße Verwendung der Befehls Zeilenschalter oder durch den Inhalt der IDL-und ACF-Dateien verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="d78aa-108">When using the MIDL compiler, errors and warnings can be caused by improper use of the command-line switches or by the content of the IDL and ACF files.</span></span> <span data-ttu-id="d78aa-109">Wenn der Fehler darauf zurückzuführen ist, dass die Befehls Zeilenschalter nicht ordnungsgemäß eingegeben werden, kann in einer Fehler-oder Warnmeldung der Name eines oder mehrerer Mittell-compilermodusschalter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d78aa-109">If the error is due to improperly entering the command-line switches, an error or warning message may specify the name of one or more MIDL compiler mode switches.</span></span> <span data-ttu-id="d78aa-110">Beispielsweise können Sie bestimmte ACF-Attribute in eine IDL-Datei einschließen, wenn Sie den Schalter/**App \_ config** verwenden. diese IDL-Datei generiert jedoch einen Fehler, wenn Sie ohne den Schalter/**App- \_ Konfiguration** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d78aa-110">For example, you can include certain ACF attributes in an IDL file when you use the /**app\_config** switch, but that IDL file will generate an error if you compile without using the /**app\_config** switch.</span></span>

<span data-ttu-id="d78aa-111">Fehler in den IDL-und ACF-Dateien werden in zwei Kategorien unterteilt: Fehler, die vom Präprozessor abgefangen wurden, und Fehler, die vom Compiler erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="d78aa-111">Errors in the IDL and ACF files fall into two categories: errors caught by the preprocessor and errors recognized by the compiler.</span></span> <span data-ttu-id="d78aa-112">In diesem Abschnitt werden die-präprozessorfehlermeldungen und-Compilerfehlermeldungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d78aa-112">This section lists the MIDL preprocessor and compiler error messages.</span></span> <span data-ttu-id="d78aa-113">Außerdem werden ihre Formate und Gründe beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d78aa-113">It also describes their formats and causes.</span></span>

-   [<span data-ttu-id="d78aa-114">Formate für Fehler-und Warnmeldungen</span><span class="sxs-lookup"><span data-stu-id="d78aa-114">Error and Warning Message Formats</span></span>](error-and-warning-message-formats.md)
-   [<span data-ttu-id="d78aa-115">Präprozessorfehler</span><span class="sxs-lookup"><span data-stu-id="d78aa-115">Preprocessor Errors</span></span>](preprocessor-errors.md)
-   [<span data-ttu-id="d78aa-116">Compilerfehler</span><span class="sxs-lookup"><span data-stu-id="d78aa-116">Compiler Errors</span></span>](compiler-errors.md)

 

 




