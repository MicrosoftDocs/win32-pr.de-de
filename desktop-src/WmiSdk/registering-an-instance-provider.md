---
description: Zum Erstellen eines WMI-Instanzanbieters müssen Sie die \_ \_ Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ instanceproviderregistration registrieren.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrieren eines Instanzanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528502"
---
# <a name="registering-an-instance-provider"></a><span data-ttu-id="1e1b5-103">Registrieren eines Instanzanbieters</span><span class="sxs-lookup"><span data-stu-id="1e1b5-103">Registering an Instance Provider</span></span>

<span data-ttu-id="1e1b5-104">Zum Erstellen eines WMI- [*Instanzanbieters*](gloss-i.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-104">To create a WMI [*instance provider*](gloss-i.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="1e1b5-105">Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="1e1b5-106">Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="1e1b5-107">Im folgenden Verfahren wird beschrieben, wie ein Instanzanbieter registriert wird.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-107">The following procedure describes how to register an instance provider.</span></span>

<span data-ttu-id="1e1b5-108">**So registrieren Sie einen Instanzanbieter**</span><span class="sxs-lookup"><span data-stu-id="1e1b5-108">**To register an instance provider**</span></span>

1.  <span data-ttu-id="1e1b5-109">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="1e1b5-110">Erstellen Sie eine Instanz der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-110">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="1e1b5-111">Die [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse erbt viele Eigenschaften von der übergeordneten [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) -Klasse, die boolesche Werte bereitstellt, die Unterstützung für bestimmte Funktionen und ein Array von Zeichen folgen zur Angabe der Abfrage Unterstützung angeben.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-111">The [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="1e1b5-112">Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](standard-wmi-qualifiers.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-112">Be sure to tag the class with both the [**Dynamic**](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="1e1b5-113">Der Qualifizierer signalisiert, dass WMI einen **dynamischen** Anbieter zum Abrufen der Klassen Instanzen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-113">The qualifier signals that WMI should use a **Dynamic** provider to retrieve the class instances.</span></span> <span data-ttu-id="1e1b5-114">Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="1e1b5-115">Im folgenden Codebeispiel wird beschrieben, wie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Instanz registriert werden.</span><span class="sxs-lookup"><span data-stu-id="1e1b5-115">The following code example describes how to register a [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) instance.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



