---
description: Wie andere Instanzanbieter registrieren Sie einen Hochleistungs Anbieter bei Microsoft Windows&\# 160; Verwaltungs Instrumentation (WMI), indem eine Instanz der \_ \_ Win32Provider-Klasse und der \_ \_ instanceproviderregistration-Klasse erstellt wird.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrieren eines High-Performance Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042003"
---
# <a name="registering-a-high-performance-provider"></a><span data-ttu-id="098b6-103">Registrieren eines High-Performance Anbieters</span><span class="sxs-lookup"><span data-stu-id="098b6-103">Registering a High-Performance Provider</span></span>

<span data-ttu-id="098b6-104">Wie andere Instanzanbieter registrieren Sie einen Hochleistungs Anbieter bei Microsoft Windows-Verwaltungsinstrumentation (WMI), indem Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse und der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="098b6-104">Like other instance providers, you register a high-performance provider with Microsoft Windows Management Instrumentation (WMI) by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes.</span></span> <span data-ttu-id="098b6-105">Die **\_ \_ Win32Provider** -Instanz definiert die physische Implementierung des Anbieters, und die **\_ \_ instanceproviderregistration** -Instanz definiert die Funktionsgruppe des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="098b6-105">The **\_\_Win32Provider** instance defines the provider's physical implementation, and the **\_\_InstanceProviderRegistration** instance defines the provider's feature set.</span></span> <span data-ttu-id="098b6-106">Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="098b6-106">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="098b6-107">Im folgenden Verfahren wird beschrieben, wie ein Anbieter für Hochleistungs Instanzen registriert wird.</span><span class="sxs-lookup"><span data-stu-id="098b6-107">The following procedure describes how to register a high-performance instance provider.</span></span>

<span data-ttu-id="098b6-108">**So registrieren Sie einen Anbieter für Hochleistungs Instanzen**</span><span class="sxs-lookup"><span data-stu-id="098b6-108">**To register a high-performance instance provider**</span></span>

1.  <span data-ttu-id="098b6-109">Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.</span><span class="sxs-lookup"><span data-stu-id="098b6-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class describing the provider.</span></span>

    <span data-ttu-id="098b6-110">Stellen Sie sicher, dass Sie der [**\_ \_ Win32Provider**](--win32provider.md) -Instanz eine **clientloadableclsid** -Eigenschaft hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="098b6-110">Be sure to add a **ClientLoadableCLSID** property to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span> <span data-ttu-id="098b6-111">Wenn sich sowohl der Anbieter als auch der Client auf demselben Computer befinden, lädt WMI den Anbieter Prozess in-Process auf den Client, wobei **clientloadableclsid** als Klassen Bezeichner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="098b6-111">If both the provider and client reside on the same computer, WMI loads the provider in-process to the client using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="098b6-112">Wenn sich der Anbieter und der Client auf unterschiedlichen Computern befinden, wird der Anbieter von WMI in-Process in den WMI-Prozess geladen.</span><span class="sxs-lookup"><span data-stu-id="098b6-112">When the provider and client reside on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="098b6-113">WMI verwendet auch **clientloadableclsid** , um Aktualisierungs Vorgänge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="098b6-113">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

2.  <span data-ttu-id="098b6-114">Erstellen Sie eine Instanz der [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.</span><span class="sxs-lookup"><span data-stu-id="098b6-114">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="098b6-115">Stellen Sie sicher, dass Sie die-Klasse mit dem [**dynamischen**](dynamic-qualifier.md) und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren.</span><span class="sxs-lookup"><span data-stu-id="098b6-115">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="098b6-116">Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter zum Abrufen der Klassen Instanzen verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="098b6-116">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="098b6-117">Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="098b6-117">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

    <span data-ttu-id="098b6-118">Ein Hochleistungs Anbieter muss auch die Unterstützung für Vorgänge, Enumerationsvorgänge oder beides angeben.</span><span class="sxs-lookup"><span data-stu-id="098b6-118">A high-performance provider also needs to state support for operations, enumeration operations, or both.</span></span> <span data-ttu-id="098b6-119">Stellen Sie sicher, dass Sie die Eigenschaften " **supportsget** " und " **supportsenumeration** " in der Implementierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="098b6-119">Make sure you use the **SupportsGet** and **SupportsEnumeration** properties in your implementation.</span></span>

<span data-ttu-id="098b6-120">Im folgenden Codebeispiel wird gezeigt, wie Sie die [**\_ \_ Win32Provider**](--win32provider.md) -und [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klassen für einen Hochleistungs Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="098b6-120">The following code example shows you how to implement the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes for a high-performance provider.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a><span data-ttu-id="098b6-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="098b6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="098b6-122">Erstellen eines Instanzanbieters in einen High-Performance-Anbieter</span><span class="sxs-lookup"><span data-stu-id="098b6-122">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



