---
description: Die erweiterten Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Referenz zu erweiterten Telefoniediensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359845"
---
# <a name="extended-telephony-services-reference"></a><span data-ttu-id="85099-103">Referenz zu erweiterten Telefoniediensten</span><span class="sxs-lookup"><span data-stu-id="85099-103">Extended Telephony Services Reference</span></span>

<span data-ttu-id="85099-104">Die erweiterten Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="85099-104">The Extended Telephony functions are listed by category in the following tables.</span></span>

## <a name="extended-telephony-functions-for-line-devices"></a><span data-ttu-id="85099-105">Erweiterte Telefoniefunktionen für Linien Geräte</span><span class="sxs-lookup"><span data-stu-id="85099-105">Extended Telephony Functions for Line Devices</span></span>



| <span data-ttu-id="85099-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="85099-106">Function</span></span>                                                   | <span data-ttu-id="85099-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85099-107">Description</span></span>                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85099-108">**linenegotiateextversion**</span><span class="sxs-lookup"><span data-stu-id="85099-108">**lineNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | <span data-ttu-id="85099-109">Ermöglicht einer Anwendung das Aushandeln einer Erweiterungs Version, die mit dem angegebenen Zeilen Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85099-109">Allows an application to negotiate an extension version to use with the specified line device.</span></span> <span data-ttu-id="85099-110">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="85099-110">Asynchronous.</span></span> |
| [<span data-ttu-id="85099-111">**linedevspecific**</span><span class="sxs-lookup"><span data-stu-id="85099-111">**lineDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | <span data-ttu-id="85099-112">Bietet Dienstanbietern Zugriff auf gerätespezifische Funktionen, die nicht von anderen TAPI-Funktionen angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="85099-112">Gives service providers access to device-specific features not offered by other TAPI functions.</span></span> <span data-ttu-id="85099-113">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="85099-113">Synchronous.</span></span> |
| [<span data-ttu-id="85099-114">**linedevspecificfeature**</span><span class="sxs-lookup"><span data-stu-id="85099-114">**lineDevSpecificFeature**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | <span data-ttu-id="85099-115">Sendet gerätespezifische Switchfeatures an den Schalter.</span><span class="sxs-lookup"><span data-stu-id="85099-115">Sends device-specific switch features to the switch.</span></span> <span data-ttu-id="85099-116">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="85099-116">Asynchronous.</span></span>                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a><span data-ttu-id="85099-117">Erweiterte Telefoniefunktionen für Telefongeräte</span><span class="sxs-lookup"><span data-stu-id="85099-117">Extended Telephony Functions for Phone Devices</span></span>



| <span data-ttu-id="85099-118">Funktion</span><span class="sxs-lookup"><span data-stu-id="85099-118">Function</span></span>                                                     | <span data-ttu-id="85099-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85099-119">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85099-120">**phonedevspecific**</span><span class="sxs-lookup"><span data-stu-id="85099-120">**phoneDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | <span data-ttu-id="85099-121">Gerätespezifische escapefunktion, um Hersteller abhängige Erweiterungen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="85099-121">Device-specific escape function to allow vendor-dependent extensions.</span></span> <span data-ttu-id="85099-122">Asynchron.</span><span class="sxs-lookup"><span data-stu-id="85099-122">Asynchronous.</span></span>                          |
| [<span data-ttu-id="85099-123">**Phonenegotiateextversion**</span><span class="sxs-lookup"><span data-stu-id="85099-123">**PhoneNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | <span data-ttu-id="85099-124">Ermöglicht einer Anwendung das Aushandeln einer Erweiterungs Version, die mit dem angegebenen Telefongerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85099-124">Allows an application to negotiate an extension version to use with the specified phone device.</span></span> <span data-ttu-id="85099-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="85099-125">Synchronous.</span></span> |



 

 

 



