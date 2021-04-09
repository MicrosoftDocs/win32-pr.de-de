---
title: Dynamic-Annotation-API
description: Die API für die dynamische Anmerkung ist eine Erweiterung von Microsoft Active Accessibility, mit der Entwickler die vorhandene IAccessible-Unterstützung anpassen können, ohne fehleranfällige Unterklassen-oder Wrapping Techniken verwenden zu müssen.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948090"
---
# <a name="dynamic-annotation-api"></a><span data-ttu-id="77101-103">Dynamic-Annotation-API</span><span class="sxs-lookup"><span data-stu-id="77101-103">Dynamic Annotation API</span></span>

<span data-ttu-id="77101-104">Die API für die dynamische Anmerkung ist eine Erweiterung von Microsoft Active Accessibility, mit der Entwickler die vorhandene [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Unterstützung anpassen können, ohne fehleranfällige Unterklassen-oder Wrapping Techniken verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="77101-104">The Dynamic Annotation API is an extension to Microsoft Active Accessibility that allows developers to customize existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support without having to use error-prone subclassing or wrapping techniques.</span></span> <span data-ttu-id="77101-105">Dieser Mechanismus ermöglicht es Entwicklern auch, Hinweise oder andere nützliche Informationen an die Oleacc.dll Proxys zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="77101-105">This mechanism also allows developers to pass hints or other useful information to the Oleacc.dll proxies.</span></span>

<span data-ttu-id="77101-106">Dynamische Anmerkung wird normalerweise verwendet, um eine ungenaue Instanz eines [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekts zu korrigieren oder zu ändern, das von einem vorhandenen Oleacc.dll Proxy verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="77101-106">Dynamic Annotation is typically used to correct or amend an inaccurate instance of an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object exposed by an existing Oleacc.dll proxy.</span></span> <span data-ttu-id="77101-107">So können Sie beispielsweise den [**Namen**](name-property.md) und die [**Rollen**](role-property.md) Eigenschaften des Standard Proxys überschreiben und [**Beschreibungen**](description-property.md) und [**Hilfe**](help-property.md) Eigenschaften angeben (die möglicherweise nicht vom Standard Proxy bereitgestellt werden).</span><span class="sxs-lookup"><span data-stu-id="77101-107">For example, you can use it to override the [**Name**](name-property.md) and [**Role**](role-property.md) properties provided by the default proxy, and to supply [**Description**](description-property.md) and [**Help**](help-property.md) properties (which may not be provided by the default proxy).</span></span>

<span data-ttu-id="77101-108">Mit Windows 7 können Entwickler die API für dynamische Annotation verwenden, um Eigenschaften der Microsoft-Benutzeroberflächen Automatisierung und Microsoft Active Accessibility Eigenschaften der Proxy Objekte, die Oleacc.dll für Windows-Standard Steuerelemente erstellt, mit Anmerkungen versehen.</span><span class="sxs-lookup"><span data-stu-id="77101-108">With Windows 7, developers can use the Dynamic Annotation API to annotate Microsoft UI Automation properties as well as Microsoft Active Accessibility properties of the proxy objects that Oleacc.dll creates for standard Windows controls.</span></span> <span data-ttu-id="77101-109">Die Oleacc.dll Proxy Objekte fungieren sowohl für Microsoft Active Accessibility als auch für Benutzeroberflächenautomatisierungs-Clients.</span><span class="sxs-lookup"><span data-stu-id="77101-109">The Oleacc.dll proxy objects serve both Microsoft Active Accessibility and UI Automation clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="77101-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="77101-110">In this section</span></span>

-   [<span data-ttu-id="77101-111">Hintergrundinformationen</span><span class="sxs-lookup"><span data-stu-id="77101-111">Background Information</span></span>](background-information.md)
-   [<span data-ttu-id="77101-112">Alternativen zu dynamischer Anmerkung</span><span class="sxs-lookup"><span data-stu-id="77101-112">Alternatives to Dynamic Annotation</span></span>](alternatives-to-dynamic-annotation.md)
-   [<span data-ttu-id="77101-113">Typen von dynamischer Anmerkung</span><span class="sxs-lookup"><span data-stu-id="77101-113">Types of Dynamic Annotation</span></span>](types-of-dynamic-annotation.md)
-   [<span data-ttu-id="77101-114">Direkte Anmerkung</span><span class="sxs-lookup"><span data-stu-id="77101-114">Direct Annotation</span></span>](direct-annotation.md)
-   [<span data-ttu-id="77101-115">Werte Zuordnungs Anmerkung</span><span class="sxs-lookup"><span data-stu-id="77101-115">Value Map Annotation</span></span>](value-map-annotation.md)
-   [<span data-ttu-id="77101-116">Server Anmerkung</span><span class="sxs-lookup"><span data-stu-id="77101-116">Server Annotation</span></span>](server-annotation.md)
-   [<span data-ttu-id="77101-117">Probleme und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="77101-117">Issues and Limitations</span></span>](issues-and-limitations.md)

 

 




