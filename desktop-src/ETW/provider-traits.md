---
description: Anbieter Merkmale sind eine Methode zum Anfügen von mehr Daten an eine einzelne Anbieter Registrierung.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Anbieter Merkmale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980393"
---
# <a name="provider-traits"></a><span data-ttu-id="895a9-103">Anbieter Merkmale</span><span class="sxs-lookup"><span data-stu-id="895a9-103">Provider Traits</span></span>

<span data-ttu-id="895a9-104">Anbieter Merkmale sind eine Methode zum Anfügen von mehr Daten an eine einzelne Anbieter Registrierung.</span><span class="sxs-lookup"><span data-stu-id="895a9-104">Provider Traits are a method of attaching more data to an individual provider registration.</span></span> <span data-ttu-id="895a9-105">Sie können für Manifestressourcen oder tracelogging-Anbieter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-105">They can be used for manifest-based or TraceLogging providers.</span></span> <span data-ttu-id="895a9-106">Dies umfasst derzeit die Unterstützung für das Hinzufügen eines Anbieter namens und/oder einer Anbieter Gruppe zu einer einzelnen Anbieter Registrierung.</span><span class="sxs-lookup"><span data-stu-id="895a9-106">This currently includes support for adding a Provider Name and/or Provider Group to an individual provider registration.</span></span> <span data-ttu-id="895a9-107">In Zukunft werden wahrscheinlich weitere Merkmals Typen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="895a9-107">More trait types are likely to be added in the future.</span></span> <span data-ttu-id="895a9-108">Diese Informationen werden im Kernel als binäres Blob eines festgelegten Formats gespeichert.</span><span class="sxs-lookup"><span data-stu-id="895a9-108">This information is stored in the kernel as a binary blob of a set format.</span></span>

<span data-ttu-id="895a9-109">Merkmale können nur einmal für eine Registrierung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-109">Traits can only be set once for a registration.</span></span> <span data-ttu-id="895a9-110">Alle weiteren Versuche, die Merkmale dieser Registrierung festzulegen, können nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-110">Any further attempts to set the traits on that registration will fail.</span></span>

<span data-ttu-id="895a9-111">Um Anbieter Merkmale für einen Manifest-basierten Anbieter festzulegen, müssen Sie die [**eventsetinformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) -Funktion mit der eventprovidersettrait-Informations Klasse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="895a9-111">To set Provider Traits on a manifest-based provider, call the [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) function with the EventProviderSetTraits information class.</span></span> <span data-ttu-id="895a9-112">Der eventinformation-Puffer sollte ein binäres Blob im folgenden Format enthalten:</span><span class="sxs-lookup"><span data-stu-id="895a9-112">The EventInformation buffer should contain a binary blob of the following format:</span></span>

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

<span data-ttu-id="895a9-113">Einzelne Merkmale sollten das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="895a9-113">Individual traits should be in the following format:</span></span>

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

<span data-ttu-id="895a9-114">Aus dem einzelnen Merkmal ist der etw- \_ Anbieter \_ Merkmals \_ Typ wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="895a9-114">From the individual trait, ETW\_PROVIDER\_TRAIT\_TYPE is defined as:</span></span>

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

<span data-ttu-id="895a9-115">Die Anbieter Merkmale werden von tracelogging-Anbietern automatisch festgelegt, wenn die [**traceloggingregister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="895a9-115">TraceLogging providers automatically set the Provider Traits when the [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) function is called.</span></span> <span data-ttu-id="895a9-116">Der Name des tracelogging-Anbieters ist immer in seinen Merkmalen enthalten.</span><span class="sxs-lookup"><span data-stu-id="895a9-116">The TraceLogging provider's name will always be included in its traits.</span></span> <span data-ttu-id="895a9-117">Eine Gruppe kann für einen tracelogging-Anbieter mithilfe des [**traceloggingoptiongroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) -Makros in der Anbieter Definition festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-117">A group can be set on a TraceLogging provider using the [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) macro in the provider definition.</span></span>

## <a name="custom-traits"></a><span data-ttu-id="895a9-118">Benutzerdefinierte Merkmale</span><span class="sxs-lookup"><span data-stu-id="895a9-118">Custom Traits</span></span>

<span data-ttu-id="895a9-119">Obwohl die meisten der 255 möglichen Merkmals Typen noch nicht definiert sind, sind Merkmals Typen 1-127 für die Definition durch Microsoft reserviert.</span><span class="sxs-lookup"><span data-stu-id="895a9-119">Although most of the 255 possible trait types are not yet defined, trait types 1-127 are reserved for definition by Microsoft.</span></span> <span data-ttu-id="895a9-120">Die verbleibenden Werte des indizierten Typs können von externen Entwicklern verwendet werden, wenn Sie passen.</span><span class="sxs-lookup"><span data-stu-id="895a9-120">The remaining higher indexed type values can be used by external developers as they see fit.</span></span> <span data-ttu-id="895a9-121">Jeder Benutzer, der seine eigenen benutzerdefinierten Merkmale dem Anbieter hinzufügt, sollte die gesamte Merkmals Größe in den folgenden Gründen unter 256 Bytes behalten:</span><span class="sxs-lookup"><span data-stu-id="895a9-121">Anyone considering adding their own custom traits to their provider should try to keep their total trait size under 256 bytes for the following reasons:</span></span>

-   <span data-ttu-id="895a9-122">Die Merkmale sind in jedem für den Anbieter geschriebenen Ereignis enthalten.</span><span class="sxs-lookup"><span data-stu-id="895a9-122">The traits are included in every event written for the provider.</span></span> <span data-ttu-id="895a9-123">Große Merkmale können zu sehr großen Protokolldateien führen.</span><span class="sxs-lookup"><span data-stu-id="895a9-123">Large traits could lead to very large log files.</span></span>
-   <span data-ttu-id="895a9-124">Die Merkmale werden während der Lebensdauer des Anbieters im nicht ausgelagerten Kernel Pool gespeichert.</span><span class="sxs-lookup"><span data-stu-id="895a9-124">The traits are stored in nonpaged kernel pool for the lifetime of the provider.</span></span>

## <a name="provider-groups"></a><span data-ttu-id="895a9-125">Anbietergruppen</span><span class="sxs-lookup"><span data-stu-id="895a9-125">Provider Groups</span></span>

<span data-ttu-id="895a9-126">Eine Anbieter Gruppe ist eine GUID-definierte, steuerbare Entität, ähnlich wie ein Anbieter selbst.</span><span class="sxs-lookup"><span data-stu-id="895a9-126">A provider group is a GUID-defined controllable entity much like a provider itself.</span></span> <span data-ttu-id="895a9-127">Der Hauptunterschied besteht darin, dass während der Verwendung einer Anbieter-GUID zum Steuern der Registrierungen nur seines Anbieters eine Gruppe alle Registrierungen der Mitglieder steuert.</span><span class="sxs-lookup"><span data-stu-id="895a9-127">The key difference is that while a provider GUID is used to control registrations of just its provider, a group will control all of its member registrations.</span></span> <span data-ttu-id="895a9-128">Wenn Sie z. b. eine Anbieter Gruppe mit einem bestimmten Schlüsselwort und einer Ebene aktivieren, werden alle Gruppenmitglieder Registrierungen mit diesem Schlüsselwort und derselben Ebene aktiviert.</span><span class="sxs-lookup"><span data-stu-id="895a9-128">For example, enabling a provider group with a given keyword and level will enable all of the groups member registrations with that keyword and level.</span></span>

<span data-ttu-id="895a9-129">Die Gruppenmitgliedschaft kann durch Berechtigungen eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-129">Group membership may be restricted by permissions.</span></span> <span data-ttu-id="895a9-130">Wenn der Aufrufer von [**eventsetinformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) nicht über Berechtigungen zum Beitreten zur angegebenen Gruppe verfügt, wird die Mitgliedschaft verweigert.</span><span class="sxs-lookup"><span data-stu-id="895a9-130">If the caller of [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) doesn't have permissions to join the specified group, then membership will be denied.</span></span>

<span data-ttu-id="895a9-131">In einigen Fällen möchte der Ablauf Verfolgungs Sitzungs Controller einige Anbieter von der Aktivierung einer Gruppe ausschließen.</span><span class="sxs-lookup"><span data-stu-id="895a9-131">In some cases the trace session controller may want to exclude a few providers from its enable of a group.</span></span> <span data-ttu-id="895a9-132">Dies kann durch Festlegen einer nicht zulassen-Liste erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-132">This can be done by setting a disallow list.</span></span> <span data-ttu-id="895a9-133">Eine nicht Zulassungsliste ist eine Liste von Anbieter-GUIDs, die auf der Grundlage der Gruppeneinstellungen für eine einzelne Protokollierungs Sitzung nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-133">A disallow list is a list of provider GUIDs that will not be enabled based on the group settings for a single logging session.</span></span> <span data-ttu-id="895a9-134">Die Zulassungs Listen können dynamisch mit [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) und der tracesetdisallowlist-Informations Klasse geändert werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-134">Disallow lists can be changed dynamically with [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) and the TraceSetDisallowList information class.</span></span>

<span data-ttu-id="895a9-135">Die meisten enable-Aktionen können für Anbietergruppen auf ähnliche Weise wie bei einzelnen Anbietern durchgeführt werden. es gibt jedoch einige Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="895a9-135">While most enable actions can be done for Provider Groups in a similar manner to individual providers, there are some exceptions.</span></span> <span data-ttu-id="895a9-136">Zu den Ausnahmen zählen:</span><span class="sxs-lookup"><span data-stu-id="895a9-136">Exceptions include:</span></span>

-   <span data-ttu-id="895a9-137">Anbietergruppen können nicht von privaten Ablauf Verfolgungs Sitzungen gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="895a9-137">Provider Groups cannot be controlled by private trace sessions.</span></span>
-   <span data-ttu-id="895a9-138">Der Ereignis Name, die Ereignis-ID und die Nutz Last Filter sind für Anbietergruppen nicht anwendbar, da Sie bestimmte Informationen eines einzelnen Anbieters annehmen.</span><span class="sxs-lookup"><span data-stu-id="895a9-138">Event Name, Event ID, and Payload filters are not applicable to Provider Groups as they assume specific information of an individual provider.</span></span>

 

 
