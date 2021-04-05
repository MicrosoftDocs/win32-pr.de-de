---
title: Schriftart Ressource
description: Definiert eine Datei, die eine Schriftart enthält.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Schriftart Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718738"
---
# <a name="font-resource"></a><span data-ttu-id="3afd1-104">Schriftart Ressource</span><span class="sxs-lookup"><span data-stu-id="3afd1-104">FONT resource</span></span>

<span data-ttu-id="3afd1-105">Definiert eine Datei, die eine Schriftart enthält.</span><span class="sxs-lookup"><span data-stu-id="3afd1-105">Defines a file that contains a font.</span></span>

``` syntax
nameID FONT filename
```

## <a name="parameters"></a><span data-ttu-id="3afd1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3afd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3afd1-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="3afd1-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="3afd1-108">Eindeutiger ganzzahliger 16-Bit-Wert ohne Vorzeichen, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3afd1-108">Unique 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3afd1-109"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="3afd1-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="3afd1-110">Der Name der Datei, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3afd1-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="3afd1-111">Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="3afd1-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="3afd1-112">Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="3afd1-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="3afd1-113">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3afd1-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3afd1-114">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="3afd1-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3afd1-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3afd1-115">Examples</span></span>

<span data-ttu-id="3afd1-116">Im folgenden Beispiel wird eine einzelne Schriftart Ressource definiert:</span><span class="sxs-lookup"><span data-stu-id="3afd1-116">The following example defines a single font resource:</span></span>

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




