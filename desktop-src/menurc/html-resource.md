---
title: HTML-Ressource
description: Definiert eine HTML-Datei.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- HTML-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857495"
---
# <a name="html-resource"></a><span data-ttu-id="f1928-104">HTML-Ressource</span><span class="sxs-lookup"><span data-stu-id="f1928-104">HTML resource</span></span>

<span data-ttu-id="f1928-105">Definiert eine HTML-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1928-105">Defines an HTML file.</span></span>

``` syntax
nameID HTML filename
```

## <a name="parameters"></a><span data-ttu-id="f1928-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1928-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="f1928-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="f1928-108">Eindeutiger Name oder ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f1928-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f1928-109"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="f1928-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="f1928-110">Der Name der HTML-Datei.</span><span class="sxs-lookup"><span data-stu-id="f1928-110">The name of the HTML file.</span></span> <span data-ttu-id="f1928-111">Wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet, muss Sie ein vollständiger oder relativer Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="f1928-111">It must be a full or relative path if the file is not in the current working directory.</span></span> <span data-ttu-id="f1928-112">Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="f1928-112">The path should be a quoted string.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f1928-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1928-113">Examples</span></span>

<span data-ttu-id="f1928-114">Im folgenden Beispiel wird eine HTML-Ressource definiert:</span><span class="sxs-lookup"><span data-stu-id="f1928-114">The following example defines an HTML resource:</span></span>

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




