---
description: Die Schlüssel Formatierungs Typen konfigurierbarer Daten können in Textfeldern verwendet werden, um einen Schlüssel in einer Datenbanktabelle bereitzustellen.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Schlüssel Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348408"
---
# <a name="key-format-types"></a><span data-ttu-id="5c7bd-103">Schlüssel Format Typen</span><span class="sxs-lookup"><span data-stu-id="5c7bd-103">Key Format Types</span></span>

<span data-ttu-id="5c7bd-104">Die Schlüssel Formatierungs Typen konfigurierbarer Daten können in Textfeldern verwendet werden, um einen Schlüssel in einer Datenbanktabelle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-104">The Key Format Types of configurable data may be used in text fields to provide a key into a database table.</span></span> <span data-ttu-id="5c7bd-105">Das msmconfigitemnonable-Attribut ist in diesem Datenformat implizit und muss nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-105">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="5c7bd-106">NULL ist nie ein gültiger Wert für diesen Typ.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-106">Null is never a valid value for this type.</span></span> <span data-ttu-id="5c7bd-107">Antworten auf alle Schlüssel Formatierungs Elemente müssen das [spezielle cmsm-Format](cmsm-special-format.md)aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-107">Responses to all Key format items must be in [CMSM Special Format](cmsm-special-format.md).</span></span>

<span data-ttu-id="5c7bd-108">Die folgenden Schlüssel Format Typen sind vorhanden:</span><span class="sxs-lookup"><span data-stu-id="5c7bd-108">The following Key Format types exist:</span></span>

[<span data-ttu-id="5c7bd-109">Verzeichnistyp</span><span class="sxs-lookup"><span data-stu-id="5c7bd-109">Directory Type</span></span>](directory-type.md)

[<span data-ttu-id="5c7bd-110">Dateityp</span><span class="sxs-lookup"><span data-stu-id="5c7bd-110">File Type</span></span>](file-type.md)

[<span data-ttu-id="5c7bd-111">Eigenschaftentyp</span><span class="sxs-lookup"><span data-stu-id="5c7bd-111">Property Type</span></span>](property-type.md)

[<span data-ttu-id="5c7bd-112">Dialog Feld-Typ</span><span class="sxs-lookup"><span data-stu-id="5c7bd-112">Dialog Type</span></span>](dialog-type.md)

[<span data-ttu-id="5c7bd-113">Binary-Typ</span><span class="sxs-lookup"><span data-stu-id="5c7bd-113">Binary Type</span></span>](binary-type.md)

[<span data-ttu-id="5c7bd-114">Symboltyp</span><span class="sxs-lookup"><span data-stu-id="5c7bd-114">Icon Type</span></span>](icon-type.md)

<span data-ttu-id="5c7bd-115">Konfigurierbare Elemente des Schlüssel Formattyps werden in Textspalten verwendet, um einen Daten Bank Schlüssel bereitzustellen, und können im Allgemeinen durch eine beliebige Text Zeichenfolge ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-115">Configurable items of the Key Format Type are used in text columns to provide a database key and in general could be replaced by any text string.</span></span> <span data-ttu-id="5c7bd-116">Die einzelnen Typen verfügen möglicherweise über zusätzliche syntaktische Einschränkungen, aber diese Einschränkungen werden von Mergemod.dll nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-116">The individual types may have additional syntactic restrictions, but these restrictions are not enforced by Mergemod.dll.</span></span> <span data-ttu-id="5c7bd-117">Bestimmte konfigurierbare Elemente können auch über charakteristische Semantik Einschränkungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-117">Particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="5c7bd-118">Beispielsweise kann ein bestimmtes konfigurierbares Element ein Schlüssel in die [binäre Tabelle](binary-table.md) für eine Zeile sein, die ein Bitmapbild enthält.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-118">For example, a particular configurable item may be required to be a key into the [Binary table](binary-table.md) to a row containing a bitmap image.</span></span> <span data-ttu-id="5c7bd-119">Solche Einschränkungen werden von Mergemod.dll nicht erzwungen. Daher sollten Modul Autoren darauf vorbereitet sein, jede beliebige Zeichenfolge zu verarbeiten, die dem angegebenen Schlüssel Formattyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-119">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Key Format type.</span></span> <span data-ttu-id="5c7bd-120">Sofern nicht anderweitig durch die semantische Bedeutung oder Attribute angegeben, ist NULL eine gültige Antwort.</span><span class="sxs-lookup"><span data-stu-id="5c7bd-120">Unless otherwise specified by semantic meaning or attributes, null is a valid response.</span></span>

 

 



