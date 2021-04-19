---
title: Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter
description: Dieser Abschnitt enthält Informationen zum Erstellen von Microsoft Benutzeroberflächenautomatisierungs-Anbietern.
ms.assetid: dd9996ec-f70f-4d5b-a029-ad4102b92a14
keywords:
- Benutzeroberflächen Automatisierung, Erstellen von Anbietern
- Benutzeroberflächen Automatisierung, Anbieter Erstellung
- Erstellen von Anbietern
- Anbieter, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da09b5bcef605dd4979a15433c708e04e49534d
ms.sourcegitcommit: 305298a7727a428310fa138b45a933bcd7ef2532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2020
ms.locfileid: "106338651"
---
# <a name="ui-automation-provider-programmers-guide"></a><span data-ttu-id="36fc0-107">Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="36fc0-107">UI Automation Provider Programmer's Guide</span></span>

<span data-ttu-id="36fc0-108">Dieser Abschnitt enthält Informationen zum Erstellen von Microsoft Benutzeroberflächenautomatisierungs-Anbietern.</span><span class="sxs-lookup"><span data-stu-id="36fc0-108">This section contains information about creating Microsoft UI Automation providers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="36fc0-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="36fc0-109">In this section</span></span>

-   [<span data-ttu-id="36fc0-110">Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="36fc0-110">UI Automation Providers Overview</span></span>](uiauto-providersoverview.md)
-   [<span data-ttu-id="36fc0-111">Implementieren eines Server-Side Benutzeroberflächenautomatisierungs-Anbieters</span><span class="sxs-lookup"><span data-stu-id="36fc0-111">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
-   [<span data-ttu-id="36fc0-112">Implementieren eines Client-Side (Proxy) Benutzeroberflächenautomatisierungs-Anbieters</span><span class="sxs-lookup"><span data-stu-id="36fc0-112">Implementing a Client-Side (Proxy) UI Automation Provider</span></span>](uiauto-clientsideprovider.md)
-   [<span data-ttu-id="36fc0-113">Hinzufügen von Funktionen für die Benutzeroberflächen Automatisierung zu Active Accessibility Servern</span><span class="sxs-lookup"><span data-stu-id="36fc0-113">Adding UI Automation Functionality to Active Accessibility Servers</span></span>](uiauto-usingiaccessibleex.md)
-   [<span data-ttu-id="36fc0-114">Implementieren von Steuerungs Mustern für Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="36fc0-114">Implementing UI Automation Control Patterns</span></span>](uiauto-implementinguiautocontrolpatterns.md)
-   [<span data-ttu-id="36fc0-115">Unterstützen der Benutzeroberflächenautomatisierungs</span><span class="sxs-lookup"><span data-stu-id="36fc0-115">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
-   [<span data-ttu-id="36fc0-116">Gewusst-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="36fc0-116">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)

## <a name="related-topics"></a><span data-ttu-id="36fc0-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36fc0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36fc0-118">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="36fc0-118">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> <dt>

[<span data-ttu-id="36fc0-119">Beispiel für einfache Benutzeroberflächen Automatisierung</span><span class="sxs-lookup"><span data-stu-id="36fc0-119">UI Automation Simple Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20simple%20provider%20sample)
</dt> <dt>

[<span data-ttu-id="36fc0-120">Beispiel für Benutzeroberflächenautomatisierungs-Kern Fenster Anbieter</span><span class="sxs-lookup"><span data-stu-id="36fc0-120">UI Automation Core Window Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20core%20window%20provider%20sample)
</dt> <dt>

[<span data-ttu-id="36fc0-121">Benutzeroberflächenautomatisierungs-Fragmentanbieter</span><span class="sxs-lookup"><span data-stu-id="36fc0-121">UI Automation Fragment Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20fragment%20provider%20sample)
</dt> <dt>

[<span data-ttu-id="36fc0-122">Benutzeroberflächenautomatisierungs-Dokument Inhaltsanbieter-Beispiel</span><span class="sxs-lookup"><span data-stu-id="36fc0-122">UI Automation Document Content Provider Sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/UI%20Automation%20document%20content%20provider%20sample)
</dt> </dl>

 

 




