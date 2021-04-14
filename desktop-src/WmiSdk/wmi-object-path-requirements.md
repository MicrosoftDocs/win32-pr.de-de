---
description: WMI verwendet Objekt Pfade in den Verweis Eigenschaften von Zuordnungs Klassen, um verknüpfte Objekte zu identifizieren, sowie die Verwendung von Objekt Pfaden in Eingabe-oder Ausgabeparametern für mehrere Methoden.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: WMI-Objekt Pfad Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393569"
---
# <a name="wmi-object-path-requirements"></a><span data-ttu-id="a4371-103">WMI-Objekt Pfad Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4371-103">WMI Object Path Requirements</span></span>

<span data-ttu-id="a4371-104">WMI verwendet Objekt Pfade in den Verweis Eigenschaften von Zuordnungs Klassen, um verknüpfte Objekte zu identifizieren, sowie die Verwendung von Objekt Pfaden in Eingabe-oder Ausgabeparametern für mehrere Methoden.</span><span class="sxs-lookup"><span data-stu-id="a4371-104">WMI uses object paths in the reference properties of association classes to identify related objects, as well as using object paths in input or output parameters for several methods.</span></span> <span data-ttu-id="a4371-105">Da Objekt Pfade als Zeichen folgen für die Suche und den Vergleich behandelt werden, ist der Wert eines Objekt Pfads, wenn er als Verweis Eigenschaft verwendet wird, immer die Zeichenfolge selbst und nicht das Dereferenzierte Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4371-105">Because object paths are treated as strings for the purpose of lookup and comparison, the value of an object path when used as a reference property is always the string itself and not the dereferenced object.</span></span> <span data-ttu-id="a4371-106">Bei Zeichen folgen vergleichen, bei denen Objekt Pfade behandelt werden, wird die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="a4371-106">String comparisons that deal with object paths are always case-insensitive.</span></span>

<span data-ttu-id="a4371-107">Ein Objekt Pfad kann die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="a4371-107">An object path can use the following syntax:</span></span>

-   <span data-ttu-id="a4371-108">In einfache Anführungszeichen enthaltene Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="a4371-108">Strings contained in single quotation marks.</span></span>
-   <span data-ttu-id="a4371-109">Schrägstriche als Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="a4371-109">Forward slashes as separators.</span></span>
-   <span data-ttu-id="a4371-110">Umgekehrte Schrägstriche als Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="a4371-110">Backslashes as separators.</span></span>
-   <span data-ttu-id="a4371-111">Hexadezimale Konstanten für ganze Zahlen.</span><span class="sxs-lookup"><span data-stu-id="a4371-111">Hexadecimal constants for integers.</span></span>
-   <span data-ttu-id="a4371-112">Boolesche Konstanten für Klassen mit Schlüsseln, die boolesche Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="a4371-112">Boolean constants for classes with keys that take Boolean values.</span></span>
-   <span data-ttu-id="a4371-113">URL-Notation zur Darstellung nicht druckbarer Zeichen, z. b. %20 für einen leeren Bereich.</span><span class="sxs-lookup"><span data-stu-id="a4371-113">URL notation to represent nonprinting characters, such as %20 for a blank space.</span></span>

<span data-ttu-id="a4371-114">Außerdem muss eine Objekt Pfad Zeichenfolge die folgenden Einschränkungen einhalten:</span><span class="sxs-lookup"><span data-stu-id="a4371-114">In addition, an object path string must obey the following restrictions:</span></span>

-   <span data-ttu-id="a4371-115">Ein von einem angenommenen lokalen Server mit einem partiellen Namespace Pfad.</span><span class="sxs-lookup"><span data-stu-id="a4371-115">An assumed local server with a partial namespace path.</span></span> <span data-ttu-id="a4371-116">Daher impliziert die Angabe des Stamm-und des Standard Namespace den Stamm-und den Standard Namespace auf dem lokalen Server.</span><span class="sxs-lookup"><span data-stu-id="a4371-116">Thus, specifying the root and default namespace implies the root and default namespace on the local server.</span></span>
-   <span data-ttu-id="a4371-117">Kein Leerraum innerhalb eines Elements oder zwischen Elementen.</span><span class="sxs-lookup"><span data-stu-id="a4371-117">No white space either within an element or between elements.</span></span>
-   <span data-ttu-id="a4371-118">Eingebettete Anführungszeichen in Objekt Pfaden sind zulässig, müssen jedoch das Anführungszeichen mit Escapezeichen begrenzen, wie in einer C-oder C++-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a4371-118">Embedded quotation marks in object paths are allowed but must delimit the quotation mark with escape characters, as in a C or C++ application.</span></span>
-   <span data-ttu-id="a4371-119">Nur Dezimalwerte werden als numerische Teile von Schlüsseln erkannt.</span><span class="sxs-lookup"><span data-stu-id="a4371-119">Only decimal values are recognized as numeric portions of keys.</span></span>

 

 



