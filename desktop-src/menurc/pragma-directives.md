---
title: Pragma-Direktiven
description: RC unterstützt die vom C/C++-Compiler unterstützten pragma-Direktiven nicht.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038967"
---
# <a name="pragma-directives"></a><span data-ttu-id="72498-103">Pragma-Direktiven</span><span class="sxs-lookup"><span data-stu-id="72498-103">Pragma Directives</span></span>

<span data-ttu-id="72498-104">RC unterstützt die vom C/C++-Compiler unterstützten pragma-Direktiven nicht.</span><span class="sxs-lookup"><span data-stu-id="72498-104">RC does not support the pragma directives supported by the C/C++ compiler.</span></span> <span data-ttu-id="72498-105">RC unterstützt jedoch die folgende pragma-Direktive zum Ändern der Codepage:</span><span class="sxs-lookup"><span data-stu-id="72498-105">However, RC does support the following pragma directive for changing the code page:</span></span>

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

<span data-ttu-id="72498-106">Dieses Pragma wird in einer enthaltenen Ressourcen Datei (. RC) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72498-106">This pragma is not supported in an included resource file (.rc).</span></span> <span data-ttu-id="72498-107">Wenn Sie also über eine übergeordnete RC-Datei verfügen und RC-Dateien für mehrere Sprachen enthalten, verwenden Sie dieses Pragma vor dem Einschließen einer anderen RC-Datei, anstatt Sie in der enthaltenen RC-Datei selbst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="72498-107">Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself.</span></span> <span data-ttu-id="72498-108">Dies wird im folgenden Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="72498-108">This is demonstrated in the following example.</span></span>

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

<span data-ttu-id="72498-109">Eine Liste der Werte für codepagenum finden Sie unter [Code Page Identifier](../intl/code-page-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="72498-109">For a list of values for CodePageNum, see [Code Page Identifiers](../intl/code-page-identifiers.md).</span></span>

 

 