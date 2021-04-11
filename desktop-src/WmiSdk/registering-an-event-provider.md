---
description: Zum Erstellen eines WMI-Ereignis Anbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ eventproviderregistration registrieren.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrieren eines Ereignis Anbieters
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131917"
---
# <a name="registering-an-event-provider"></a><span data-ttu-id="c18ef-103">Registrieren eines Ereignis Anbieters</span><span class="sxs-lookup"><span data-stu-id="c18ef-103">Registering an Event Provider</span></span>

<span data-ttu-id="c18ef-104">Zum Erstellen eines WMI- [*Ereignis Anbieters*](gloss-e.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ eventproviderregistration**](--eventproviderregistration.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="c18ef-104">To create a WMI [*event provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventProviderRegistration**](--eventproviderregistration.md).</span></span> <span data-ttu-id="c18ef-105">Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="c18ef-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="c18ef-106">Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c18ef-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="c18ef-107">Im folgenden Verfahren wird beschrieben, wie ein Ereignis Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="c18ef-107">The following procedure describes how to register an event provider.</span></span>

<span data-ttu-id="c18ef-108">**So registrieren Sie einen Ereignis Anbieter**</span><span class="sxs-lookup"><span data-stu-id="c18ef-108">**To register an event provider**</span></span>

1.  <span data-ttu-id="c18ef-109">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c18ef-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="c18ef-110">Erstellen Sie eine Instanz der [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c18ef-110">Create an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="c18ef-111">Die [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="c18ef-111">The [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class.</span></span> <span data-ttu-id="c18ef-112">Die lokalen Eigenschaften der **\_ \_ eventproviderregistration** -Klasse sind der Objekt Pfad zum Anbieter und eine Liste von Abfragen, die die vom Anbieter unterstützten Ereignisse beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c18ef-112">The properties local to the **\_\_EventProviderRegistration** class are the object path to the provider and a list of queries that describe the events that the provider supports.</span></span> <span data-ttu-id="c18ef-113">Weitere Informationen finden Sie unter [WMI-Abfrage](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c18ef-113">For more information, see [Querying WMI](querying-wmi.md).</span></span>

3.  <span data-ttu-id="c18ef-114">Laden Sie die Implementierung der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse und der [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse in das WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="c18ef-114">Load your implementation of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) classes into the WMI repository.</span></span>

    <span data-ttu-id="c18ef-115">WMI verwendet Ihre Klassendefinition, um den Ereignis Anbieter zu registrieren und darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c18ef-115">WMI uses your class definition to register and access your event provider.</span></span> <span data-ttu-id="c18ef-116">Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c18ef-116">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="c18ef-117">Im folgenden Codebeispiel wird eine Implementierung einer [**\_ \_ Win32Provider**](--win32provider.md) -Klasse und einer [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c18ef-117">The following code example describes an implementation of a [**\_\_Win32Provider**](--win32provider.md) class and a [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

<span data-ttu-id="c18ef-118">Die erste Abfrage gibt an, dass der Anbieter alle Ereignis Benachrichtigungen für das faxereignis der System externe-Ereignisklasse generiert.</span><span class="sxs-lookup"><span data-stu-id="c18ef-118">The first query indicates that the provider generates all event notifications for the extrinsic event class FaxEvent.</span></span> <span data-ttu-id="c18ef-119">Da der ISA-Operator verwendet wird, impliziert die zweite Abfrage, dass der Anbieter Benachrichtigungen für alle instanzerstellungsereignisse für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse und alle seine Unterklassen generiert.</span><span class="sxs-lookup"><span data-stu-id="c18ef-119">Because it uses the ISA operator, the second query implies that the provider generates notifications for all instance creation events for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and all of its subclasses.</span></span>

<span data-ttu-id="c18ef-120">Wenn ein Anbieter registriert wird, um ein System internes Ereignis bereitzustellen, muss das Ereignis auf alle Instanzen einer Klasse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c18ef-120">When a provider registers to provide an intrinsic event, the event must apply to all instances of a class.</span></span> <span data-ttu-id="c18ef-121">Anders ausgedrückt: Es kann keine Abfrage geschrieben werden, um instanzerstellungsereignisse nur für einige Laufwerke bereitzustellen, die zur [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse gehören.</span><span class="sxs-lookup"><span data-stu-id="c18ef-121">In other words, a query cannot be written to provide instance creation events for only some of the disk drives that belong to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

 

 
