---
description: Entwickler können die WMI-Infrastruktur durch die Entwicklung von WMI-Anbietern erweitern.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Erstellen von WMI-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050593"
---
# <a name="creating-wmi-providers"></a><span data-ttu-id="58ef5-103">Erstellen von WMI-Anbietern</span><span class="sxs-lookup"><span data-stu-id="58ef5-103">Creating WMI Providers</span></span>

<span data-ttu-id="58ef5-104">Entwickler können die WMI-Infrastruktur durch die Entwicklung von WMI-Anbietern erweitern.</span><span class="sxs-lookup"><span data-stu-id="58ef5-104">Developers can extend the WMI infrastructure by developing WMI providers.</span></span> <span data-ttu-id="58ef5-105">WMI-Anbieter sind COM-Objekte, die einen angegebenen Satz von Schnittstellen implementieren und bis vor kurzem in C++ immer implementiert wurden.</span><span class="sxs-lookup"><span data-stu-id="58ef5-105">WMI providers are COM objects that implement a specified set of interfaces and, until recently, were always implemented in C++.</span></span> <span data-ttu-id="58ef5-106">Sie können jetzt verwaltete Sprachen wie c# verwenden, um WMI-Anbieter zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="58ef5-106">You can now use managed languages like C# to implement WMI providers.</span></span> <span data-ttu-id="58ef5-107">In Version 3,5 von .NET Framework wurde das Framework für WMI-Anbieter Erweiterungen eingeführt, das Dies ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="58ef5-107">Version 3.5 of the .NET framework introduced the WMI Provider Extensions framework that makes this possible.</span></span> <span data-ttu-id="58ef5-108">Weitere Informationen zum Erstellen von WMI-Anbietern mithilfe dieses Frameworks finden Sie im Artikel [Schreiben von gekoppelten WMI-Anbietern mithilfe der WMI.NET-Anbieter Erweiterung 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="58ef5-108">To learn more about creating WMI providers by using that framework, read the article, [Writing coupled WMI providers using WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="58ef5-109">Sie können auch einen Anbieter mithilfe der Windows-Verwaltungsinfrastruktur (Mi) erstellen, der WMI-Version der nächsten Generation.</span><span class="sxs-lookup"><span data-stu-id="58ef5-109">You can also create a provider using Windows Management Infrastructure (MI), the next-generation version of WMI.</span></span> <span data-ttu-id="58ef5-110">Weitere Informationen finden Sie unter [Implementieren eines Mi-Anbieters](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="58ef5-110">For more information, see [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span></span>

 

<span data-ttu-id="58ef5-111">In der folgenden Tabelle werden die Inhalte dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58ef5-111">The following table describes the contents in this section.</span></span>



| <span data-ttu-id="58ef5-112">Thema</span><span class="sxs-lookup"><span data-stu-id="58ef5-112">Topic</span></span>                                                      | <span data-ttu-id="58ef5-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58ef5-113">Description</span></span>                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="58ef5-114">Bereitstellen von Daten für WMI</span><span class="sxs-lookup"><span data-stu-id="58ef5-114">Providing Data to WMI</span></span>](providing-data-to-wmi.md)         | <span data-ttu-id="58ef5-115">Bietet einen Überblick über die Schritte zum Erstellen eines WMI-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="58ef5-115">Provides an overview of the steps involved in creating a WMI provider.</span></span>         |
| [<span data-ttu-id="58ef5-116">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="58ef5-116">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md) | <span data-ttu-id="58ef5-117">Beschreibt Aufgaben, die Sie beim Erstellen verschiedener Typen von WMI-Anbietern ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="58ef5-117">Describes tasks you must perform when creating various types of WMI providers.</span></span> |



 

 

 
