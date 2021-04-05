---
title: WDS-Transport Anbieter Funktionen
description: Benutzerdefinierte Inhaltsanbieter können dem Multicast Server die folgenden Rückruf Funktionen zur Verfügung stellen.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713854"
---
# <a name="wds-transport-provider-functions"></a><span data-ttu-id="ec0ca-103">WDS-Transport Anbieter Funktionen</span><span class="sxs-lookup"><span data-stu-id="ec0ca-103">WDS Transport Provider Functions</span></span>

<span data-ttu-id="ec0ca-104">Benutzerdefinierte Inhaltsanbieter können dem Multicast Server die folgenden Rückruf Funktionen zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-104">User-defined content providers can expose the following callback functions to the multicast server.</span></span>



| <span data-ttu-id="ec0ca-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="ec0ca-105">Function</span></span>                                                                               | <span data-ttu-id="ec0ca-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec0ca-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec0ca-107">*Wdstransportproviderclosecontent*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-107">*WdsTransportProviderCloseContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | <span data-ttu-id="ec0ca-108">Schließt einen von einem Handle angegebenen Inhaltsdaten Strom.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-108">Closes a content stream specified by a handle.</span></span>                                                                          |
| [<span data-ttu-id="ec0ca-109">*Wdstransportprovidercloseinstance*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-109">*WdsTransportProviderCloseInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | <span data-ttu-id="ec0ca-110">Schließt eine Instanz eines Inhalts Anbieters, der durch ein Handle angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-110">Closes an instance of a content provider specified by a handle.</span></span>                                                         |
| [<span data-ttu-id="ec0ca-111">*Wdstransportprovidercomparecontent*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-111">*WdsTransportProviderCompareContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | <span data-ttu-id="ec0ca-112">Vergleicht einen angegebenen Inhalts Namen und eine Instanz mit einem geöffneten Inhaltsstream, um zu bestimmen, ob diese identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-112">Compares a specified content name and instance to an open content stream to determine if they are the same.</span></span>             |
| [<span data-ttu-id="ec0ca-113">*Wdstransportproviderkreateinstance*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-113">*WdsTransportProviderCreateInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | <span data-ttu-id="ec0ca-114">Öffnet eine neue Instanz eines Inhalts Anbieters.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-114">Opens a new instance of a content provider.</span></span>                                                                             |
| [<span data-ttu-id="ec0ca-115">*Wdstransportproviderdumpstate*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-115">*WdsTransportProviderDumpState*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | <span data-ttu-id="ec0ca-116">Weist den Transportanbieter an, eine Zusammenfassung seines Zustands und alle anderen relevanten Informationen in das Ablauf Verfolgungs Protokoll zu drucken.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-116">Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.</span></span> |
| [<span data-ttu-id="ec0ca-117">*Wdstransportprovidergetcontentmetadata*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-117">*WdsTransportProviderGetContentMetadata*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | <span data-ttu-id="ec0ca-118">Ruft Metadaten für einen geöffneten Inhaltsstream ab.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-118">Retrieves metadata for an open content stream.</span></span>                                                                          |
| [<span data-ttu-id="ec0ca-119">*Wdstransportprovidergetcontentsize*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-119">*WdsTransportProviderGetContentSize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | <span data-ttu-id="ec0ca-120">Ruft die Größe eines geöffneten Inhaltsstreams ab.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-120">Retrieves the size of an open content stream.</span></span>                                                                           |
| [<span data-ttu-id="ec0ca-121">*Wdstransportproviderinitialize*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-121">*WdsTransportProviderInitialize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | <span data-ttu-id="ec0ca-122">Initialisiert einen Inhaltsanbieter.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-122">Initializes a content provider.</span></span>                                                                                         |
| [<span data-ttu-id="ec0ca-123">*Wdstransportprovideropencontent*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-123">*WdsTransportProviderOpenContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | <span data-ttu-id="ec0ca-124">Öffnet eine neue statische Ansicht eines Inhaltsstreams.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-124">Opens a new static view of a content stream.</span></span>                                                                            |
| [<span data-ttu-id="ec0ca-125">*Wdstransportproviderlescontent*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-125">*WdsTransportProviderReadContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | <span data-ttu-id="ec0ca-126">Liest Inhalt aus einem geöffneten Inhaltsstream.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-126">Reads content from an open content stream.</span></span>                                                                              |
| [<span data-ttu-id="ec0ca-127">*Wdstransportprovidererfrischendes-Einstellungen*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-127">*WdsTransportProviderRefreshSettings*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | <span data-ttu-id="ec0ca-128">Weist den Transportanbieter an, alle relevanten Einstellungen erneut zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-128">Instructs the transport provider to reread any relevant settings.</span></span>                                                       |
| [<span data-ttu-id="ec0ca-129">*Wdstransportprovidershutdown*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-129">*WdsTransportProviderShutdown*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | <span data-ttu-id="ec0ca-130">Herunterfahren des Inhalts Anbieters</span><span class="sxs-lookup"><span data-stu-id="ec0ca-130">Shutsdown the content provider.</span></span>                                                                                         |
| [<span data-ttu-id="ec0ca-131">*Wdstransportprovideruseraccesscheck*</span><span class="sxs-lookup"><span data-stu-id="ec0ca-131">*WdsTransportProviderUserAccessCheck*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | <span data-ttu-id="ec0ca-132">Gibt den Zugriff auf einen Inhaltsstream basierend auf dem Token eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-132">Specifies access to a content stream based on a user's token.</span></span>                                                           |



 

 

 




