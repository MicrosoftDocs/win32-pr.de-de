---
description: Anbieter von freigegebenen Komponenten sollten in Erwägung gezogen werden, Ihre Komponente als parallele Assembly verfügbar zu gestalten, wenn mindestens einer der folgenden Fälle zutrifft.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Sollten Sie eine freigegebene Komponente als parallele Assembly bereitstellen?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867883"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a><span data-ttu-id="bc2a1-103">Sollten Sie eine freigegebene Komponente als parallele Assembly bereitstellen?</span><span class="sxs-lookup"><span data-stu-id="bc2a1-103">Should you provide a shared component as a side-by-side assembly?</span></span>

<span data-ttu-id="bc2a1-104">Anbieter von freigegebenen Komponenten sollten in Erwägung gezogen werden, Ihre Komponente als parallele Assembly verfügbar zu gestalten, wenn mindestens einer der folgenden Punkte zutrifft:</span><span class="sxs-lookup"><span data-stu-id="bc2a1-104">Providers of shared components should consider making their component available as a side-by-side assembly if one or more of the following are true:</span></span>

-   <span data-ttu-id="bc2a1-105">Die Komponente macht eine umfangreiche Anwendungsprogrammierschnittstelle verfügbar, die von vielen Anwendungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-105">The component exposes a rich application programming interface that is used by many applications.</span></span> <span data-ttu-id="bc2a1-106">Beispielsweise eine Komponente wie MSHTML, mit der C-und C++-Anwendungen auf das dynamische HTML-Objektmodell (DHTML) zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-106">For example, a component such as MSHTML, which enables C and C++ applications to access the Dynamic HTML (DHTML) Object Model.</span></span>
-   <span data-ttu-id="bc2a1-107">Die Komponente wird bereits von mehreren Anwendungen gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-107">The component is already being shared by multiple applications.</span></span> <span data-ttu-id="bc2a1-108">Beispielsweise eine Komponente wie ComCtl32, die Anwendungen den Zugriff auf die allgemeinen Steuerelemente ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-108">For example, a component such as COMCTL32, which provides applications access to the common controls.</span></span>
-   <span data-ttu-id="bc2a1-109">Die Komponente ist eine neue Komponente.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-109">The component is a new component.</span></span>
-   <span data-ttu-id="bc2a1-110">Bei der Komponente handelt es sich um eine Benutzermoduskomponente und nicht um einen Gerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-110">The component is a user-mode component and not a device driver.</span></span>

<span data-ttu-id="bc2a1-111">Nicht jede Komponente ist ein geeigneter Kandidat für eine parallele Assembly.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-111">Not every component is a suitable candidate for a side-by-side assembly.</span></span> <span data-ttu-id="bc2a1-112">Eine Komponente ist kein geeigneter Kandidat für eine parallele Assembly, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="bc2a1-112">A component is not a suitable candidate for a side-by-side assembly if any of the following are true:</span></span>

-   <span data-ttu-id="bc2a1-113">Die Komponente verarbeitet die Kommunikation zwischen Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-113">The component handles communication between applications.</span></span> <span data-ttu-id="bc2a1-114">Beispielsweise würden Teile von OLE32 keine gute parallele Assembly machen, da Sie nicht über zwei verschiedene Versionen der Teile verfügen möchten, die die Kommunikation zwischen Anwendungen koordinieren, die auf Ihrem System ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-114">For example, parts of OLE32 would not make a good side-by-side assembly because you would not want to have two different versions of the parts that coordinate communication between applications run on your system.</span></span>
-   <span data-ttu-id="bc2a1-115">Die Komponente verwaltet ein physisches oder virtuelles Gerät für das System.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-115">The component manages a physical or virtual device for the system.</span></span> <span data-ttu-id="bc2a1-116">Beispielsweise ein Gerätetreiber für einen Druck Spooler.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-116">For example a device driver for a print spooler.</span></span>

<span data-ttu-id="bc2a1-117">In einigen Fällen kann es möglich sein, dass der Entwickler der Komponente eine vorhandene Komponente umgestalten muss, damit Sie als parallele Assembly für die Veröffentlichung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-117">In some cases it may be possible for the developer of the component to redesign an existing component in order to make it suitable for publication as a side-by-side assembly.</span></span> <span data-ttu-id="bc2a1-118">Weitere Informationen finden Sie unter [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md)paralleler Assemblys.</span><span class="sxs-lookup"><span data-stu-id="bc2a1-118">For more information see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

 

 



