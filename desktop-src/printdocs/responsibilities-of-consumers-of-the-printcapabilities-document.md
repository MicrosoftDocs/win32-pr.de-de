---
description: Benutzer von PrintCapabilities-Dokumenten haben bestimmte Verpflichtungen, die sie erfüllen müssen, bevor sie ein PrintCapabilities-Dokument verwenden können.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Zuständigkeiten der Verbraucher des PrintCapabilities-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec123509515de32b88c7352dcf0fc2c2b54504ff
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404943"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="a6d98-103">Zuständigkeiten der Verbraucher des PrintCapabilities-Dokuments</span><span class="sxs-lookup"><span data-stu-id="a6d98-103">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="a6d98-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="a6d98-104">This topic is not current.</span></span> <span data-ttu-id="a6d98-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="a6d98-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a6d98-106">Benutzer von PrintCapabilities-Dokumenten haben bestimmte Verpflichtungen, die sie erfüllen müssen, bevor sie ein PrintCapabilities-Dokument verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a6d98-106">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="a6d98-107">Die folgenden Anforderungen gelten für Clients eines PrintCapabilities-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="a6d98-107">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="a6d98-108">Sie dürfen keine syntaktisch gültigen PrintCapabilities-Daten ablehnen oder nicht verarbeiten. das heißt, alle PrintCapabilities-Dokumente, die dem PrintCapabilities-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a6d98-108">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="a6d98-109">Sie müssen das unerwartete Vorhandensein oder Fehlen von privat definierten Inhalten abarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a6d98-109">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="a6d98-110">Dies schließt privat definierte Inhalte ein, die in Instanzen von druckschemadefinierten Elementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a6d98-110">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="a6d98-111">Sie müssen in der Lage sein, optionalen Inhalt des Druckschemas zu umarbeiten, der nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a6d98-111">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="a6d98-112">Sie müssen wissen, wann sie ein neues Dokument anfordern müssen.</span><span class="sxs-lookup"><span data-stu-id="a6d98-112">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="a6d98-113">Werte von Property-Instanzen sind konfigurationsabhängig (daher momentaufnahmeabhängig).</span><span class="sxs-lookup"><span data-stu-id="a6d98-113">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="a6d98-114">Sie müssen die Momentaufnahme aktualisieren, wenn Sie auf eine Property-Instanz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a6d98-114">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="a6d98-115">Feature-, Option- und ScoredProperty-Instanzen, die in ein PrintTicket kopiert werden sollen, sind definitionsgemäß statisch.</span><span class="sxs-lookup"><span data-stu-id="a6d98-115">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="a6d98-116">Das heißt, sie sind nicht von der Gerätekonfiguration abhängig (und dürfen nicht sein).</span><span class="sxs-lookup"><span data-stu-id="a6d98-116">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="a6d98-117">Wenn Sie auf Instanzen dieser Typen zugreifen, müssen Sie kein neues PrintCapabilities-Dokument abrufen, wenn sich die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="a6d98-117">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="a6d98-118">Benutzer von PrintCapabilities-Clients, die Benutzeroberflächenclients sind, müssen Informationen in einem PrintCapabilities-Dokument verwenden können, um eine Benutzeroberfläche zu erstellen und ein gültiges PrintTicket aus der Benutzerauswahl zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a6d98-118">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="a6d98-119">Dazu gehört das Wissen, welche ParameterInit-Instanzen angegeben werden müssen, und die Validierung der angegebenen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="a6d98-119">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6d98-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6d98-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d98-121">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="a6d98-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



