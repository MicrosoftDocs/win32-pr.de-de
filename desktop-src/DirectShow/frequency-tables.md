---
description: Häufigkeits Tabellen
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Häufigkeits Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123560"
---
# <a name="frequency-tables"></a><span data-ttu-id="329c9-103">Häufigkeits Tabellen</span><span class="sxs-lookup"><span data-stu-id="329c9-103">Frequency Tables</span></span>

<span data-ttu-id="329c9-104">Der TV-Tuner-Filter (kstvtune.ax) verfügt über eine interne Liste der Häufigkeits Tabellen.</span><span class="sxs-lookup"><span data-stu-id="329c9-104">The TV Tuner filter (kstvtune.ax) has an internal list of frequency tables.</span></span> <span data-ttu-id="329c9-105">Jede Häufigkeits Tabelle enthält eine Liste von Frequenzen und entspricht den Übertragungs-oder Kabel Frequenzen für ein bestimmtes Land bzw. eine bestimmte Region.</span><span class="sxs-lookup"><span data-stu-id="329c9-105">Each frequency table contains a list of frequencies, and corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="329c9-106">Eine Anwendung optimiert auf eine bestimmte Häufigkeit, indem Sie die Methode [**iamtuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) mit dem Index der gewünschten Häufigkeit aufruft.</span><span class="sxs-lookup"><span data-stu-id="329c9-106">An application tunes to a particular frequency by calling the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method with the index of the desired frequency.</span></span>

<span data-ttu-id="329c9-107">Für einige Länder/Regionen werden die Indexnummern der Häufigkeits Tabellen direkt den Kanalnummern zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="329c9-107">For some countries/regions, the index numbers of the frequency tables map directly to channel numbers.</span></span> <span data-ttu-id="329c9-108">Die Anzahl fester channelnummern eignet sich jedoch nicht für alle Märkte.</span><span class="sxs-lookup"><span data-stu-id="329c9-108">Fixed channel numbers are not appropriate for all markets, however.</span></span> <span data-ttu-id="329c9-109">Beispielsweise werden die europäischen channelnummern von Consumern nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="329c9-109">For instance, the European channel numbers are not actually used by consumers.</span></span> <span data-ttu-id="329c9-110">Stattdessen erwarten Consumer, dass Sie Ihre eigenen channelnummern für die Frequenzen auswählen und zuweisen, die von den Broadcast-oder Kabel Operatoren in Ihrem Bereich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="329c9-110">Instead, consumers expect to choose and assign their own channel numbers for the frequencies that are used by the broadcast or cable operators in their area.</span></span> <span data-ttu-id="329c9-111">Für diese Länder/Regionen sollten Anwendungen die Indexnummern nicht direkt für den Benutzer verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="329c9-111">For these countries/regions, applications should not expose the index numbers directly to the user.</span></span> <span data-ttu-id="329c9-112">Instread: die Anwendung sollte eine interne Zuordnung zwischen den channelnummern (die dem Benutzer präsentiert werden) und Häufigkeits Indizes (für die Optimierung) beibehalten.</span><span class="sxs-lookup"><span data-stu-id="329c9-112">Instread, the application should keep an internal mapping between channel numbers (presented to the user) and frequency indexes (for tuning).</span></span>

<span data-ttu-id="329c9-113">Die meisten nicht-US-Kabel Operatoren können in Häufigkeits Häufigkeit übertragen werden, wobei häufig Häufigkeiten aus verschiedenen Standards in dieselbe channelauflistung gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="329c9-113">Most non-US cable operators are free to broadcast on frequencies of their choosing, often mixing frequencies from different standards into the same channel lineup.</span></span> <span data-ttu-id="329c9-114">Daher wird für jedes Land bzw. jede Region eine "Unicable"-Häufigkeits Tabelle verwendet, die über keine standardmäßige Kabelkanal-Standard Autorität verfügt.</span><span class="sxs-lookup"><span data-stu-id="329c9-114">Therefore, a "Unicable" frequency table is used for any country/region that lacks a standard cable channel standards authority.</span></span> <span data-ttu-id="329c9-115">Außerdem wird ein Mechanismus bereitgestellt, um einzelne Frequenzen in den Häufigkeits Tabellen zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="329c9-115">Also, a mechanism is provided to override individual frequencies in the frequency tables.</span></span> <span data-ttu-id="329c9-116">Dieser Mechanismus wird im folgenden Abschnitt, [Häufigkeits Überschreitungen](frequency-overrides.md), beschrieben.</span><span class="sxs-lookup"><span data-stu-id="329c9-116">This mechanism is described in the following section, [Frequency Overrides](frequency-overrides.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="329c9-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="329c9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="329c9-118">Internationale Analog-TV-Optimierung</span><span class="sxs-lookup"><span data-stu-id="329c9-118">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



