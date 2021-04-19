---
description: Bei den Textformat Typen von konfigurierbaren Daten kann es sich um Text Zeichenfolgen beliebiger Länge handeln. Eingebettete Nullen sind nicht zulässig.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Text Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363801"
---
# <a name="text-format-types"></a><span data-ttu-id="99b49-104">Text Format Typen</span><span class="sxs-lookup"><span data-stu-id="99b49-104">Text Format Types</span></span>

<span data-ttu-id="99b49-105">Bei den Textformat Typen von konfigurierbaren Daten kann es sich um Text Zeichenfolgen beliebiger Länge handeln.</span><span class="sxs-lookup"><span data-stu-id="99b49-105">The text format types of configurable data may be text strings of any length.</span></span> <span data-ttu-id="99b49-106">Eingebettete Nullen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="99b49-106">Embedded nulls are not allowed.</span></span>

<span data-ttu-id="99b49-107">Die folgenden Text Format Typen sind vorhanden:</span><span class="sxs-lookup"><span data-stu-id="99b49-107">The following Text Format types exist:</span></span>

[<span data-ttu-id="99b49-108">Beliebiger Text</span><span class="sxs-lookup"><span data-stu-id="99b49-108">Arbitrary Text</span></span>](arbitrary-text-type.md)

[<span data-ttu-id="99b49-109">RTF</span><span class="sxs-lookup"><span data-stu-id="99b49-109">RTF</span></span>](rtf-type.md)

[<span data-ttu-id="99b49-110">Großformatige</span><span class="sxs-lookup"><span data-stu-id="99b49-110">Formatted</span></span>](formatted-type.md)

[<span data-ttu-id="99b49-111">Enum</span><span class="sxs-lookup"><span data-stu-id="99b49-111">Enum</span></span>](enum-type.md)

[<span data-ttu-id="99b49-112">Bezeichnertyp</span><span class="sxs-lookup"><span data-stu-id="99b49-112">Identifier Type</span></span>](identifier-type.md)

<span data-ttu-id="99b49-113">Konfigurierbare Elemente des Text Format Typs werden in nicht binären Datenbankfeldern verwendet und können im Allgemeinen durch eine beliebige Zeichenfolge beliebiger Länge ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="99b49-113">Configurable items of the Text Format Type are used in non-binary database fields and in general could be replaced by any string of any length.</span></span> <span data-ttu-id="99b49-114">Bestimmte konfigurierbare Elemente haben jedoch auch semantische Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="99b49-114">However, particular configurable items also have semantic restrictions.</span></span> <span data-ttu-id="99b49-115">Beispielsweise weist ein konfigurierbares Element, das als Fremdschlüssel für eine bestimmte Tabelle erforderlich ist, zusätzliche Semantik Einschränkungen auf.</span><span class="sxs-lookup"><span data-stu-id="99b49-115">For example, a configurable item that is required to be a foreign key into a specific table has additional semantic restrictions.</span></span> <span data-ttu-id="99b49-116">Solche semantischen Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modul Autoren darauf vorbereitet sein, jede beliebige Zeichenfolge zu verarbeiten, die dem angegebenen Text Formattyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="99b49-116">Such semantic restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Text Format type.</span></span>

 

 



