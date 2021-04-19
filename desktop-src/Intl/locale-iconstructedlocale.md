---
description: Gebiets Schema- \_ iconstructedlocale-Konstante Beschreibung
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "106374062"
---
# <a name="locale_iconstructedlocale"></a><span data-ttu-id="f7626-103">Gebiets Schema \_ iconstructedlocale</span><span class="sxs-lookup"><span data-stu-id="f7626-103">LOCALE\_ICONSTRUCTEDLOCALE</span></span>

<span data-ttu-id="f7626-104">Bezeichner für die Anforderung, wenn das Gebiets Schema ein "konstruiertes" Gebiets Schema ist.</span><span class="sxs-lookup"><span data-stu-id="f7626-104">Identifier to request if the locale is a "constructed" locale.</span></span> <span data-ttu-id="f7626-105">Die Verwendung dieses LCTYPE ist nicht empfehlenswert.</span><span class="sxs-lookup"><span data-stu-id="f7626-105">Use of this LCTYPE is discouraged.</span></span>

<span data-ttu-id="f7626-106">Dadurch wird ein Gebiets Schema identifiziert, für das Windows viele nicht über umfassende Informationen verfügt und zur Laufzeit Informationen erstellen muss.</span><span class="sxs-lookup"><span data-stu-id="f7626-106">This identifies a locale for which Windows many not have complete information and has to "construct" information at runtime.</span></span> <span data-ttu-id="f7626-107">In der Regel sind die von LOCALE_ICONSTRUCTEDLOCALE bereitgestellten Informationen eingeschränkt, da Windows so viele Daten bereitstellt, wie es für jedes Gebiets Schema verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f7626-107">Typically the information provided by LOCALE_ICONSTRUCTEDLOCALE is of limited use as Windows will provide as much data as is available for every locale.</span></span> <span data-ttu-id="f7626-108">Daher wird von der Verwendung dieses LCTYPE abgeraten.</span><span class="sxs-lookup"><span data-stu-id="f7626-108">Therefore, use of this LCTYPE is discouraged.</span></span>


| <span data-ttu-id="f7626-109">Wert</span><span class="sxs-lookup"><span data-stu-id="f7626-109">Value</span></span> | <span data-ttu-id="f7626-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f7626-110">Meaning</span></span>                 |
|-------|-------------------------|
| <span data-ttu-id="f7626-111">0</span><span class="sxs-lookup"><span data-stu-id="f7626-111">0</span></span>     | <span data-ttu-id="f7626-112">Nicht erstellt</span><span class="sxs-lookup"><span data-stu-id="f7626-112">Not constructed</span></span>         |
| <span data-ttu-id="f7626-113">1</span><span class="sxs-lookup"><span data-stu-id="f7626-113">1</span></span>     | <span data-ttu-id="f7626-114">Ist ein konstruiertes Gebiets Schema</span><span class="sxs-lookup"><span data-stu-id="f7626-114">Is a constructed locale</span></span> |


<span data-ttu-id="f7626-115">Ein Beispiel wäre eine Anforderung für "de-US" oder Deutsch im USA.</span><span class="sxs-lookup"><span data-stu-id="f7626-115">An example would be a request for "de-US", or German in the United States.</span></span> <span data-ttu-id="f7626-116">NLS verwendet die deutschen Sprach Daten, die gefunden werden können, und die USA Regions Daten, die gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="f7626-116">NLS will use the German language data that it can find and the United States region data that it can find.</span></span> 

<span data-ttu-id="f7626-117">Dies ist möglicherweise nicht perfekt, da das System wahrscheinlich keine Informationen über den Namen USA in Deutsch hat.</span><span class="sxs-lookup"><span data-stu-id="f7626-117">This may not be perfect as, for example, the system will likely not have information about the name of United States in German.</span></span> <span data-ttu-id="f7626-118">Wenn die Anwendung oder der Benutzer jedoch einen "de-US"-Kontext wünscht, sind die zurückgegebenen Daten die beste Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="f7626-118">However, if the application or user desires a "de-US" context, then the returned data is the best available.</span></span> 

<span data-ttu-id="f7626-119">Apps, die LOCALE_ICONSTRUCTEDLOCALE zum ablehnen von Gebiets Schemas verwenden und auf ein anderes Gebiets Schema zurückgreifen, haben in der Regel eine schlechtere Darstellung, wie z. b. die Landung von de-de oder en-US in diesem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f7626-119">Apps that use LOCALE_ICONSTRUCTEDLOCALE to reject locales and fall back to a different locale typically end up with a worse experience, such as landing on de-DE or en-US in this example.</span></span> <span data-ttu-id="f7626-120">Keines der beiden Bereiche entspricht der ursprünglichen Anforderung für deutschsprachige Sprache mit einer USA Region.</span><span class="sxs-lookup"><span data-stu-id="f7626-120">Neither of those are close to the original request for German language with a United States region.</span></span>

