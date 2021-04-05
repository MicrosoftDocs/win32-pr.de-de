---
description: Zum Erstellen eines WMI- \_ \_ Ereignisconsumeranbieters müssen Sie die Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ eventconsumerproviderregistration registrieren.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrieren eines Ereignisconsumeranbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755048"
---
# <a name="registering-an-event-consumer-provider"></a><span data-ttu-id="b140b-103">Registrieren eines Ereignisconsumeranbieters</span><span class="sxs-lookup"><span data-stu-id="b140b-103">Registering an Event Consumer Provider</span></span>

<span data-ttu-id="b140b-104">Zum Erstellen eines WMI- [*Ereignisconsumeranbieters*](gloss-e.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="b140b-104">To create a WMI [*event consumer provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="b140b-105">Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="b140b-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="b140b-106">Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b140b-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="b140b-107">Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumeranbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="b140b-107">The following procedure describes how to register an event consumer provider.</span></span>

<span data-ttu-id="b140b-108">**So registrieren Sie einen Ereignisconsumeranbieter**</span><span class="sxs-lookup"><span data-stu-id="b140b-108">**To register an event consumer provider**</span></span>

1.  <span data-ttu-id="b140b-109">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b140b-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="b140b-110">Erstellen Sie eine Instanz der [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b140b-110">Create an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="b140b-111">Die Eigenschaften, die von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) definiert werden, enthalten den Objekt Pfad zum Anbieter und die Namen der logischen Consumerklassen, die vom Ereignisconsumeranbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b140b-111">The properties that are defined by [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) include the object path to the provider and the names of the logical consumer classes that the event consumer provider supports.</span></span>

    <span data-ttu-id="b140b-112">Stellen Sie sicher, dass Sie die-Klasse mit dem **dynamischen** und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren.</span><span class="sxs-lookup"><span data-stu-id="b140b-112">Be sure to tag the class with both the **Dynamic** and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="b140b-113">Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter zum Abrufen der Klassen Instanzen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="b140b-113">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="b140b-114">Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b140b-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="b140b-115">Im folgenden Codebeispiel wird gezeigt, wie ein Ereignisconsumeranbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="b140b-115">The following code example shows how to register an event consumer provider.</span></span>

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



