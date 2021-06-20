---
description: Neben PrintCapabilities ermöglicht das PrintTicket, dass clients zusätzliche Informationen in Form von Property-Elementen hinzugefügt werden.
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: Konfigurationsinformationen, die nicht im Zusammenhang mit PrintCapabilities stehen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e4ac332d6e9b106ab9d68c29d03366761c01d5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409653"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="ee7da-103">Konfigurationsinformationen, die nicht im Zusammenhang mit PrintCapabilities stehen</span><span class="sxs-lookup"><span data-stu-id="ee7da-103">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="ee7da-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ee7da-104">This topic is not current.</span></span> <span data-ttu-id="ee7da-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="ee7da-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee7da-106">Zusätzlich zur Auswahl der in PrintCapabilities definierten Geräteattribute ermöglicht PrintTicket, dass clients zusätzliche Informationen in Form von Property-Elementen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ee7da-106">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="ee7da-107">Das Druckschema definiert eine Reihe von Standard-Eigenschafteninstanzen, und der Schnittstellenanbieter kann auch private Property-Instanzen einführen.</span><span class="sxs-lookup"><span data-stu-id="ee7da-107">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="ee7da-108">Wenn Mitglieder einer Organisation beispielsweise die meisten Druckaufträge an eine zentrale Batcheinrichtung senden, können sie für jeden Auftrag eine private Property-Instanz angeben, die eine Rückgabeadresse enthält.</span><span class="sxs-lookup"><span data-stu-id="ee7da-108">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="ee7da-109">Diese Eigenschaft kann die Bereitstellung des abgeschlossenen Auftrags vereinfachen, der an den Erursacher übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee7da-109">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee7da-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee7da-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee7da-111">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="ee7da-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



