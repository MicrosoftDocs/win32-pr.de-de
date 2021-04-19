---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Zuständigkeiten von Kunden des Printworks-Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366381"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="9c577-104">Zuständigkeiten von Kunden des Printworks-Dokuments</span><span class="sxs-lookup"><span data-stu-id="9c577-104">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="9c577-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9c577-105">This topic is not current.</span></span> <span data-ttu-id="9c577-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9c577-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9c577-107">Consumer von printfähigkeiten-Dokumenten haben bestimmte Verpflichtungen, die Sie einhalten müssen, bevor Sie ein Printworks-Dokument verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9c577-107">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="9c577-108">Die folgenden Anforderungen gelten für Clients eines Printworks-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="9c577-108">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="9c577-109">Sie dürfen keine syntaktisch gültigen Print-Funktionen ablehnen oder nicht verarbeiten. Das heißt, alle printfunktionalitäten-Dokumente, die dem printfunktionalitäten-Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9c577-109">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="9c577-110">Sie müssen in der Lage sein, das unerwartete vorhanden sein oder Fehlen von Privat definierten Inhalten zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="9c577-110">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="9c577-111">Dies schließt privat definierte Inhalte ein, die in Instanzen von Schema definierten Elementen vom Druck Schema angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9c577-111">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="9c577-112">Sie müssen den optionalen Inhalt des Druck Schemas umgehen können, der nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9c577-112">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="9c577-113">Sie müssen wissen, wann ein neues Dokument angefordert werden muss.</span><span class="sxs-lookup"><span data-stu-id="9c577-113">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="9c577-114">Werte von Eigenschaften Instanzen sind Konfigurations abhängig (daher von der Momentaufnahme abhängig).</span><span class="sxs-lookup"><span data-stu-id="9c577-114">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="9c577-115">Sie müssen die Momentaufnahme aktualisieren, wenn Sie auf eine Eigenschaften Instanz zugreifen.</span><span class="sxs-lookup"><span data-stu-id="9c577-115">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="9c577-116">Feature-, Option-und ScoredProperty-Instanzen, die in ein Print Ticket kopiert werden sollen, sind definitionsgemäß statisch.</span><span class="sxs-lookup"><span data-stu-id="9c577-116">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="9c577-117">Das heißt, Sie sind nicht (und dürfen nicht sein), abhängig von der Gerätekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9c577-117">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="9c577-118">Wenn Sie auf Instanzen dieser Art zugreifen, ist es nicht erforderlich, dass Sie ein neues printfunktionalitäten-Dokument erhalten, wenn sich die Konfiguration ändert.</span><span class="sxs-lookup"><span data-stu-id="9c577-118">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="9c577-119">Consumer von Print-Funktionen, die Benutzeroberflächen Clients sind, müssen in der Lage sein, Informationen in einem printfunktionalitäten-Dokument zu verwenden, um eine Benutzeroberfläche zu erstellen und ein gültiges PrintTicket aus der Benutzer Auswahl zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9c577-119">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="9c577-120">Dazu gehört das wissen, welche parameterinit-Instanzen angegeben werden müssen, und die Überprüfung der angegebenen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="9c577-120">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c577-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c577-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c577-122">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="9c577-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



