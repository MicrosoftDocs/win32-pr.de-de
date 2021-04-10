---
description: Zum Erstellen eines WMI-Eigenschaften Anbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ propertyproviderregistration registrieren.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrieren eines Eigenschaften Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215341"
---
# <a name="registering-a-property-provider"></a><span data-ttu-id="e0ac2-103">Registrieren eines Eigenschaften Anbieters</span><span class="sxs-lookup"><span data-stu-id="e0ac2-103">Registering a Property Provider</span></span>

<span data-ttu-id="e0ac2-104">Zum Erstellen eines WMI- [*Eigenschaften Anbieters*](gloss-p.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-104">To create a WMI [*property provider*](gloss-p.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span> <span data-ttu-id="e0ac2-105">Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="e0ac2-106">Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="e0ac2-107">Im folgenden Verfahren wird beschrieben, wie ein Eigenschaften Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-107">The following procedure describes how to register a property provider.</span></span>

<span data-ttu-id="e0ac2-108">**So registrieren Sie einen Eigenschaften Anbieter**</span><span class="sxs-lookup"><span data-stu-id="e0ac2-108">**To register a property provider**</span></span>

1.  <span data-ttu-id="e0ac2-109">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Eigenschaften Anbieter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the property provider.</span></span>

    <span data-ttu-id="e0ac2-110">Die [**\_ \_ Win32Provider**](--win32provider.md) -Klasse akzeptiert die Standardwerte für andere Eigenschaften, z. b. den **true** -Wert für die **Pure** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-110">The [**\_\_Win32Provider**](--win32provider.md) class accepts the default values for other properties, such as the **TRUE** value for the **Pure** property.</span></span> <span data-ttu-id="e0ac2-111">Weitere Informationen finden Sie unter [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="e0ac2-111">For more information, see [**\_\_Win32Provider**](--win32provider.md).</span></span>

2.  <span data-ttu-id="e0ac2-112">Erstellen Sie eine Instanz der [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-112">Create an instance of the [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="e0ac2-113">Die [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md) -Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse, die boolesche Werte bereitstellt, die Unterstützung für bestimmte Funktionen und ein Array von Zeichen folgen zur Angabe der Abfrage Unterstützung angeben.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-113">The [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="e0ac2-114">Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](dynamic-qualifier.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-114">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="e0ac2-115">Der **dynamische** Qualifizierer signalisiert, dass WMI einen dynamischen Anbieter verwenden sollte, um die Klassen Instanzen abzurufen, die die unterstützten Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-115">The **Dynamic** qualifier signals that WMI should use a dynamic provider to retrieve the class instances that contain the supported properties.</span></span> <span data-ttu-id="e0ac2-116">Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-116">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="e0ac2-117">WMI ruft NewQuery für einen Ereignis Anbieter auf, wenn ein Client Consumer eine Ereignis Filter Abfrage registriert, die Verweise auf Ereignisse enthält, die von diesem Ereignis Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-117">WMI calls NewQuery on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="e0ac2-118">Daher kann der Ereignis Anbieter, der für Instanzen Änderungs Ereignisse für die emailclass-Klasse verantwortlich ist, so eingerichtet werden, dass nur Benachrichtigungen für den Absender generiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-118">So the event provider responsible for instance modification events for the EmailClass class can be set up to generate notifications only for sender.</span></span> <span data-ttu-id="e0ac2-119">Wenn der Anbieter eine Abfrage empfängt, die eine Benachrichtigung über Änderungen an der Eigenschaft "Subject" anfordert, kann der Anbieter damit beginnen, diese Benachrichtigungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-119">When the provider receives a query requesting notification of changes to the subject property, the provider can start generating those notifications.</span></span> <span data-ttu-id="e0ac2-120">In diesem Szenario ist es nicht erforderlich, dass WMI die Benachrichtigungen verwerfen, die nur vom Empfänger des Empfängers geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-120">In this scenario, WMI is not required to discard the notifications that report recipient changes only.</span></span>

<span data-ttu-id="e0ac2-121">Im folgenden MOF-Codebeispiel werden-Instanzen beschrieben, die verwendet werden können, um einen Eigenschaften Anbieter zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-121">The following MOF code example describes instances that can be used to register a property provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> <span data-ttu-id="e0ac2-122">Nur Administratoren können einen Eigenschaften Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ propertyproviderregistration**](--propertyproviderregistration.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0ac2-122">Only administrators can register or delete a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span>

 

 

 



