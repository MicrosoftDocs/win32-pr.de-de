---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Öffentliche Schlüsselwörter von printfunktionalitäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353640"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="58e06-104">Öffentliche Schlüsselwörter von printfunktionalitäten</span><span class="sxs-lookup"><span data-stu-id="58e06-104">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="58e06-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="58e06-105">This topic is not current.</span></span> <span data-ttu-id="58e06-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="58e06-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="58e06-107">Im folgenden Abschnitt werden sowohl vom benutzerkonfigurierbare Elemente als auch Parameter Definitionen angegeben, die möglicherweise auf ein printfunktionalitäten-Dokument anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="58e06-107">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="58e06-108">Benutzerkonfigurierbare Element Verwendung</span><span class="sxs-lookup"><span data-stu-id="58e06-108">User Configurable Elements Usage</span></span>

<span data-ttu-id="58e06-109">Vom benutzerkonfigurierbare Elemente stellen öffentliche Schlüsselwörter des Druck Schemas dar, die in einem printfunktionen-Dokument oder einem PrintTicket vorkommen können.</span><span class="sxs-lookup"><span data-stu-id="58e06-109">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="58e06-110">Sie sollen konfigurierbare Geräte Attribute darstellen, die von einem bestimmten Gerät unterstützt werden, oder die Absicht der Druckeinstellung durch eine Anwendung oder einen Benutzer zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="58e06-110">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="58e06-111">Vom benutzerkonfigurierbare Elemente können auf Parameter Verweis Elemente verweisen.</span><span class="sxs-lookup"><span data-stu-id="58e06-111">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="58e06-112">Weitere Informationen finden Sie im Abschnitt [Parameter Verweis Elemente](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="58e06-112">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="58e06-113">Verwendung von Parameter Definitionen</span><span class="sxs-lookup"><span data-stu-id="58e06-113">Parameter Definitions Usage</span></span>

<span data-ttu-id="58e06-114">Parameter Definitionen verwenden die Form von ParameterDef-Elementtypen in einem Dokument mit Druckfunktionen.</span><span class="sxs-lookup"><span data-stu-id="58e06-114">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="58e06-115">ParameterDef-Elementtypen werden in einem PrintTicket mit dem parameterinit-Elementtyp initialisiert.</span><span class="sxs-lookup"><span data-stu-id="58e06-115">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="58e06-116">Der Wert des-Parameters wird mit dem parameterinit-Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="58e06-116">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="58e06-117">Ein vom Benutzer konfigurierbares Schlüsselwort kann mit dem ParameterRef-Elementtyp auf eine Parameterdefinition verweisen.</span><span class="sxs-lookup"><span data-stu-id="58e06-117">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="58e06-118">Weitere Informationen finden Sie im Abschnitt [Parameterkonstrukte](parameter-constructs.md) .</span><span class="sxs-lookup"><span data-stu-id="58e06-118">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58e06-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58e06-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58e06-120">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="58e06-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



