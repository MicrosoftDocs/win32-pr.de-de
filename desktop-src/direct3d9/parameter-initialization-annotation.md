---
description: Verwenden Sie diese Anmerkung, um den Inhalt einer externen Datei als Initialisierungs Wert für einen Effektparameter zu definieren.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Initialisierungs Anmerkung für Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213840"
---
# <a name="parameter-initialization-annotation"></a><span data-ttu-id="ca0ec-103">Initialisierungs Anmerkung für Parameter</span><span class="sxs-lookup"><span data-stu-id="ca0ec-103">Parameter Initialization Annotation</span></span>

<span data-ttu-id="ca0ec-104">Verwenden Sie diese Anmerkung, um den Inhalt einer externen Datei als Initialisierungs Wert für einen Effektparameter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ca0ec-104">Use this annotation to define the contents of an external file as the initialization value for an effect parameter.</span></span> <span data-ttu-id="ca0ec-105">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ca0ec-105">For example:</span></span>


```
string SasResourceAddress = "Value";
```



<span data-ttu-id="ca0ec-106">Dabei ist value eine ASCII-Text Zeichenfolge, die einen absoluten oder relativen Pfad enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="ca0ec-106">where Value is an ASCII text string that may contain an absolute or relative path.</span></span> <span data-ttu-id="ca0ec-107">Ein relativer Pfad bezieht sich auf das Verzeichnis, das die Effekt Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="ca0ec-107">A relative path is relative to the directory that contains the effect file.</span></span>

<span data-ttu-id="ca0ec-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ca0ec-108">Here is an example:</span></span>


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



<span data-ttu-id="ca0ec-109">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ca0ec-109">The default value is an empty string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca0ec-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca0ec-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca0ec-111">DirectX-Standard Anmerkungen und Semantik Referenz</span><span class="sxs-lookup"><span data-stu-id="ca0ec-111">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



