---
description: Zum Erstellen eines WMI-Methoden Anbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ methodproviderregistration registrieren.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrieren eines Methoden Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216891"
---
# <a name="registering-a-method-provider"></a><span data-ttu-id="0e956-103">Registrieren eines Methoden Anbieters</span><span class="sxs-lookup"><span data-stu-id="0e956-103">Registering a Method Provider</span></span>

<span data-ttu-id="0e956-104">Zum Erstellen eines WMI- [*Methoden Anbieters*](gloss-m.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ methodproviderregistration**](--methodproviderregistration.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="0e956-104">To create a WMI [*method provider*](gloss-m.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_MethodProviderRegistration**](--methodproviderregistration.md).</span></span> <span data-ttu-id="0e956-105">Nachdem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md)erstellt haben, müssen Sie diesen Anbieter bei WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="0e956-105">After creating an instance of [**\_\_Win32Provider**](--win32provider.md), you must register that provider with WMI.</span></span> <span data-ttu-id="0e956-106">Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="0e956-106">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="0e956-107">Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0e956-107">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="0e956-108">Im folgenden Verfahren wird beschrieben, wie ein Methoden Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="0e956-108">The following procedure describes how to register a method provider.</span></span>

<span data-ttu-id="0e956-109">**So registrieren Sie einen Methoden Anbieter**</span><span class="sxs-lookup"><span data-stu-id="0e956-109">**To register a method provider**</span></span>

1.  <span data-ttu-id="0e956-110">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0e956-110">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>

    <span data-ttu-id="0e956-111">Die [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -System Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse. die einzige für einen Methoden Anbieter relevante Eigenschaft ist jedoch der Objekt Pfad zur [**\_ \_ Win32Provider**](--win32provider.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="0e956-111">The [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) system class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, However, the only property relevant for a method provider is the object path to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span>

2.  <span data-ttu-id="0e956-112">Erstellen Sie eine Instanz der [**\_ \_ methodproviderregistration**](--methodproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0e956-112">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="0e956-113">Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](dynamic-qualifier.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren.</span><span class="sxs-lookup"><span data-stu-id="0e956-113">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="0e956-114">Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter zum Abrufen der Klassen Instanzen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="0e956-114">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="0e956-115">Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e956-115">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="0e956-116">Im folgenden Codebeispiel wird beschrieben, wie ein Methoden Anbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="0e956-116">The following code example describes how to register a method provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



