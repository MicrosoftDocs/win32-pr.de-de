---
description: Alle Eigenschaftsnamen müssen diese Einschränkungen einhalten.
ms.assetid: 4447013a-86c4-48a9-bfe1-5e758c799a2f
title: Einschränkungen für Eigenschaftsnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c137bc4902bdd62b42e4f3888243a11de43399b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217342"
---
# <a name="restrictions-on-property-names"></a><span data-ttu-id="afb32-103">Einschränkungen für Eigenschaftsnamen</span><span class="sxs-lookup"><span data-stu-id="afb32-103">Restrictions on Property Names</span></span>

<span data-ttu-id="afb32-104">Alle Eigenschaftsnamen müssen diese Einschränkungen einhalten.</span><span class="sxs-lookup"><span data-stu-id="afb32-104">All property names must follow these restrictions.</span></span>

-   <span data-ttu-id="afb32-105">Ein Eigenschaften Name ist ein [Bezeichner](identifier.md), bei dem es sich um eine Text Zeichenfolge handelt, die mit einem Buchstaben oder einem Unterstrich beginnen muss.</span><span class="sxs-lookup"><span data-stu-id="afb32-105">A property name is an [Identifier](identifier.md), which is a text string that must begin with either a letter or an underscore.</span></span> <span data-ttu-id="afb32-106">Bezeichner und Eigenschaftsnamen dürfen Buchstaben, Ziffern, Unterstriche oder Punkte enthalten. darf jedoch nicht mit einer Ziffer oder einem bestimmten Zeitraum beginnen.</span><span class="sxs-lookup"><span data-stu-id="afb32-106">Identifiers and property names may contain letters, numerals, underscores, or periods; but cannot begin with a numeral or period.</span></span>
-   <span data-ttu-id="afb32-107">[Öffentliche Eigenschafts](public-properties.md) Namen dürfen keine Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="afb32-107">[Public property](public-properties.md) names cannot contain lowercase letters.</span></span>
-   <span data-ttu-id="afb32-108">[Private Eigenschafts](private-properties.md) Namen müssen Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="afb32-108">[Private property](private-properties.md) names must contain some lowercase letters.</span></span>
-   <span data-ttu-id="afb32-109">Eigenschaftsnamen mit dem Präfix% stellen System-und Benutzer Umgebungsvariablen dar.</span><span class="sxs-lookup"><span data-stu-id="afb32-109">Property names prefixed with % represent system and user environment variables.</span></span> <span data-ttu-id="afb32-110">Diese werden nie in die [Eigenschaften Tabelle](property-table.md)eingegeben.</span><span class="sxs-lookup"><span data-stu-id="afb32-110">These are never entered into the [Property table](property-table.md).</span></span> <span data-ttu-id="afb32-111">Die permanenten Einstellungen von Umgebungsvariablen können nur mithilfe der [Umgebungs Tabelle](environment-table.md)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="afb32-111">The permanent settings of environment variables can only be modified using the [Environment Table](environment-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="afb32-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="afb32-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afb32-113">Verwenden von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="afb32-113">Using Properties</span></span>](using-properties.md)
</dt> </dl>

 

 



