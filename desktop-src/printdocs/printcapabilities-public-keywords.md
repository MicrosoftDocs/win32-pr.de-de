---
description: Erfahren Sie mehr über vom Benutzer konfigurierbare Elemente und Parameterdefinitionen, die möglicherweise auf ein PrintCapabilities-Dokument anwendbar sind.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Öffentliche PrintCapabilities-Schlüsselwörter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d836ca13297f031897598bb2ecbfc6588c49753
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407093"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="97795-103">Öffentliche PrintCapabilities-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="97795-103">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="97795-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="97795-104">This topic is not current.</span></span> <span data-ttu-id="97795-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="97795-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="97795-106">Im folgenden Abschnitt werden sowohl vom Benutzer konfigurierbare Elemente als auch Parameterdefinitionen angegeben, die auf ein PrintCapabilities-Dokument anwendbar sein können.</span><span class="sxs-lookup"><span data-stu-id="97795-106">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="97795-107">Benutzerkonfigurierbare Elementverwendung</span><span class="sxs-lookup"><span data-stu-id="97795-107">User Configurable Elements Usage</span></span>

<span data-ttu-id="97795-108">Benutzerkonfigurierbare Elemente stellen öffentliche Schlüsselwörter des Druckschemas dar, die entweder in einem PrintCapabilities-Dokument oder einem PrintTicket-Dokument angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="97795-108">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="97795-109">Sie sollen konfigurierbare Geräteattribute darstellen, die von einem bestimmten Gerät unterstützt werden, oder die Absicht der Druckeinstellung durch eine Anwendung oder einen Benutzer kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="97795-109">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="97795-110">Benutzerkonfigurierbare Elemente verweisen möglicherweise auf Parameterverweiselemente.</span><span class="sxs-lookup"><span data-stu-id="97795-110">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="97795-111">Weitere Informationen finden Sie im Abschnitt [Parameterverweiselemente.](parameter-reference-elements.md)</span><span class="sxs-lookup"><span data-stu-id="97795-111">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="97795-112">Verwendung von Parameterdefinitionen</span><span class="sxs-lookup"><span data-stu-id="97795-112">Parameter Definitions Usage</span></span>

<span data-ttu-id="97795-113">Parameterdefinitionen haben die Form von ParameterDef-Elementtypen in einem Dokument Druckfunktionen.</span><span class="sxs-lookup"><span data-stu-id="97795-113">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="97795-114">ParameterDef-Elementtypen werden in einem PrintTicket mithilfe des ParameterInit-Elementtyps initialisiert.</span><span class="sxs-lookup"><span data-stu-id="97795-114">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="97795-115">Der Wert des Parameters wird mit dem ParameterInit-Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="97795-115">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="97795-116">Ein vom Benutzer konfigurierbares Schlüsselwort kann mithilfe des ParameterRef-Elementtyps auf eine Parameterdefinition verweisen.</span><span class="sxs-lookup"><span data-stu-id="97795-116">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="97795-117">Weitere Informationen finden Sie im Abschnitt [Parameterkonstrukte.](parameter-constructs.md)</span><span class="sxs-lookup"><span data-stu-id="97795-117">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97795-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97795-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97795-119">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="97795-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



