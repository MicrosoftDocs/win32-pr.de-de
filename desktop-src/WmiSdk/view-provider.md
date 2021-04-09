---
description: Der Ansichts Anbieter ist eine Instanz und ein Methoden Anbieter, die neue Klassen auf der Grundlage von Instanzen von anderen Klassen erstellt.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Ansichtsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866863"
---
# <a name="view-provider"></a><span data-ttu-id="099e2-103">Ansichtsanbieter</span><span class="sxs-lookup"><span data-stu-id="099e2-103">View Provider</span></span>

<span data-ttu-id="099e2-104">Der Ansichts Anbieter ist eine Instanz und ein Methoden Anbieter, die neue Klassen auf der Grundlage von Instanzen von anderen Klassen erstellt.</span><span class="sxs-lookup"><span data-stu-id="099e2-104">The View provider is an instance and method provider that creates new classes based on instances of other classes.</span></span> <span data-ttu-id="099e2-105">Sie können den Ansichts Anbieter verwenden, um Eigenschaften aus verschiedenen Quell Klassen, anderen Namespaces oder anderen Computern zu übernehmen und die Eigenschaften als einzelne Klasse zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="099e2-105">You can use the View provider to take properties from different source classes, different namespaces, or different computers and combine the properties as a single class.</span></span>

<span data-ttu-id="099e2-106">Als Instanzen-und Methoden Anbieter unterstützt der Ansichts Anbieter die standardmäßige [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle und die folgenden [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="099e2-106">As an instance and method provider, the View provider supports the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface and the following [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="099e2-107">**"Kreateingestanceenumasync"**</span><span class="sxs-lookup"><span data-stu-id="099e2-107">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="099e2-108">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="099e2-108">**ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="099e2-109">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="099e2-109">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="099e2-110">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="099e2-110">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="099e2-111">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="099e2-111">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="099e2-112">Weitere Informationen zu den Qualifizierern, mit denen Sie Ansichts Anbieter Klassen definieren, finden [Sie unter Qualifizierer für den Ansichts Anbieter](qualifiers-specific-to-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="099e2-112">For more information about the qualifiers use to define View provider classes, see [Qualifiers Specific to the View Provider](qualifiers-specific-to-the-view-provider.md).</span></span>

<span data-ttu-id="099e2-113">Weitere Informationen zu Ansichten finden Sie unter [Verknüpfen von Klassen](linking-classes-together.md).</span><span class="sxs-lookup"><span data-stu-id="099e2-113">For more information about views, see [Linking Classes Together](linking-classes-together.md).</span></span>

<span data-ttu-id="099e2-114">Zwei Versionen des Ansichts Anbieters sind auf 64-Bit-Plattformen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="099e2-114">Two versions of the View provider are available on 64-bit platforms.</span></span> <span data-ttu-id="099e2-115">Weitere Informationen finden Sie unter " [erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)".</span><span class="sxs-lookup"><span data-stu-id="099e2-115">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="099e2-116">Der Ansichts Anbieter wird in ViewProv.dll implementiert.</span><span class="sxs-lookup"><span data-stu-id="099e2-116">The View provider is implemented in ViewProv.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="099e2-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="099e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="099e2-118">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="099e2-118">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



