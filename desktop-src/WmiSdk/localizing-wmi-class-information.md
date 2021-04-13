---
description: WMI implementiert eine Technik, die es ermöglicht, dass mehrere lokalisierte Versionen derselben Klasse im Repository gespeichert werden.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Lokalisieren von WMI-Klassen Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348398"
---
# <a name="localizing-wmi-class-information"></a><span data-ttu-id="735a3-103">Lokalisieren von WMI-Klassen Informationen</span><span class="sxs-lookup"><span data-stu-id="735a3-103">Localizing WMI Class Information</span></span>

<span data-ttu-id="735a3-104">WMI implementiert eine Technik, die es ermöglicht, dass mehrere lokalisierte Versionen derselben Klasse im Repository gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="735a3-104">WMI implements a technique that allows multiple localized versions of the same class to be stored in the repository.</span></span>

<span data-ttu-id="735a3-105">Die Klassendefinition ist in die folgenden Versionen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="735a3-105">The class definition is separated into the following versions:</span></span>

-   <span data-ttu-id="735a3-106">Eine sprachneutrale Version, die nur eine einfache Klassendefinition enthält.</span><span class="sxs-lookup"><span data-stu-id="735a3-106">A language-neutral version that contains only a basic class definition.</span></span>
-   <span data-ttu-id="735a3-107">Eine sprachspezifische Version, die lokalisierte Informationen enthält, z. b. Eigenschafts Beschreibungen, die für ein Gebiets Schema spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="735a3-107">A language-specific version that contains localized information, such as property descriptions that are specific to a locale.</span></span>

<span data-ttu-id="735a3-108">Die sprachspezifischen Klassendefinitionen werden in einem untergeordneten Namespace unterhalb des Namespaces gespeichert, der eine sprachneutrale Grundklassen Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="735a3-108">The language-specific class definitions are stored in a child namespace beneath the namespace that contains a language-neutral basic class definition.</span></span>

<span data-ttu-id="735a3-109">Wenn Sie eine lokalisierte Klassendefinition für ein bestimmtes Gebiets Schema anfordern, kombiniert WMI die grundlegende Klassendefinition und die lokalisierten Klassen Informationen, um eine komplette lokalisierte Klasse zu bilden.</span><span class="sxs-lookup"><span data-stu-id="735a3-109">When you request a localized class definition for a specific locale, WMI combines the basic class definition and the localized class information to form a complete localized class.</span></span> <span data-ttu-id="735a3-110">Sie können eine lokalisierte Version einer WMI-Klasse erhalten, indem Sie beim Herstellen einer Verbindung mit WMI ein Gebiets Schema angeben und ein Flag festlegen, das angibt, dass lokalisierte Informationen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="735a3-110">You can get a localized version of a WMI class by specifying a locale when you connect to WMI and setting a flag that indicates that you want localized information.</span></span> <span data-ttu-id="735a3-111">Die Informationen werden dann von WMI aus den sprach neutralen und sprachspezifischen Versionen der Klassendefinition zusammengeführt, um eine lokalisierte Klasse zu bilden.</span><span class="sxs-lookup"><span data-stu-id="735a3-111">WMI then merges the information from the language-neutral and the language-specific versions of the class definition to form a localized class.</span></span>

<span data-ttu-id="735a3-112">WMI-Klassen, die lokalisierte Informationen enthalten, werden mit dem **Zusatz** Qualifizierer gekennzeichnet und als geänderte Klassen bezeichnet. eine Klasse unterstützt lokalisierte Informationen, wenn Sie diesen Qualifizierer aufweist.</span><span class="sxs-lookup"><span data-stu-id="735a3-112">WMI classes that contain localized information are marked with the **Amendment** qualifier and are called amended classes; a class supports localized information if it has this qualifier.</span></span> <span data-ttu-id="735a3-113">Sie können bestimmen, für welches Gebiets Schema die Klasse lokalisiert wurde, indem Sie nach einem anderen Qualifizierer namens [**locale**](swbemobjectpath-locale.md)suchen.</span><span class="sxs-lookup"><span data-stu-id="735a3-113">You can determine which locale the class has been localized for by checking for another qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span> <span data-ttu-id="735a3-114">Der Gebiets Schema Qualifizierer enthält eine Lokalisierungs-ID (Windows LCID), die ein Gebiets Schema identifiziert.</span><span class="sxs-lookup"><span data-stu-id="735a3-114">The locale qualifier contains a localization identifier (Windows LCID) that identifies a locale.</span></span> <span data-ttu-id="735a3-115">Beispielsweise lautet das Gebiets Schema für amerikanisches Englisch 0x409.</span><span class="sxs-lookup"><span data-stu-id="735a3-115">For example, the locale for American English is 0x409.</span></span> <span data-ttu-id="735a3-116">Wenn ein Qualifizierer in einer geänderten Klasse lokalisierte Informationen enthält, enthält er die **geänderte** qualifiziererkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="735a3-116">If a qualifier in an amended class contains localized information, it contains the **amended** qualifier flavor.</span></span>

<span data-ttu-id="735a3-117">Die WMI-Lokalisierung umfasst die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="735a3-117">WMI localization includes the following tasks:</span></span>

-   [<span data-ttu-id="735a3-118">Erstellen von lokalisierten Klassendefinitionen</span><span class="sxs-lookup"><span data-stu-id="735a3-118">Creating localized class definitions</span></span>](creating-localized-class-definitions.md)
-   [<span data-ttu-id="735a3-119">Kompilieren lokalisierter MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="735a3-119">Compiling localized MOF files</span></span>](compiling-localized-mof-files.md)
-   [<span data-ttu-id="735a3-120">Lokalisieren von Eigenschafts Werten</span><span class="sxs-lookup"><span data-stu-id="735a3-120">Localizing property values</span></span>](localizing-property-values.md)
-   [<span data-ttu-id="735a3-121">Abrufen von geänderten Klassen</span><span class="sxs-lookup"><span data-stu-id="735a3-121">Retrieving amended classes</span></span>](retrieving-amended-classes.md)

<span data-ttu-id="735a3-122">Weitere Informationen finden Sie unter [Überlegungen zur geänderten Klasse](amended-class-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="735a3-122">For more information, see [Amended Class Considerations](amended-class-considerations.md).</span></span>

 

 



