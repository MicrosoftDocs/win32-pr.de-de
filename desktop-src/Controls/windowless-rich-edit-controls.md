---
title: Fensterlose Rich Edit-Steuerelemente
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit fensterlosen Bearbeitungs Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036566"
---
# <a name="windowless-rich-edit-controls"></a><span data-ttu-id="c3d25-103">Fensterlose Rich Edit-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c3d25-103">Windowless Rich Edit Controls</span></span>

<span data-ttu-id="c3d25-104">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit fensterlosen Bearbeitungs Steuerelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3d25-104">This section contains information about the programming elements used with windowless rich edit controls.</span></span> <span data-ttu-id="c3d25-105">Der Component Object Model (com) definiert einen Satz von Schnittstellen, um fensterlose Objekte zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c3d25-105">The Component Object Model (COM) defines a set of interfaces to support windowless objects.</span></span> <span data-ttu-id="c3d25-106">Fensterlose Objekte können den direkt aktiven Zustand ohne eigenes Fenster eingeben, sondern das Fenster des Containers verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3d25-106">Windowless objects can enter the in-place active state without having their own window, but rather use the window of their container.</span></span> <span data-ttu-id="c3d25-107">Folglich verwendet ein fensterloses Objekt weniger Systemressourcen und bietet eine bessere Leistung durch schnellere Aktivierung und Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="c3d25-107">Consequently, a windowless object uses fewer system resources and gives better performance through faster activation and deactivation.</span></span> <span data-ttu-id="c3d25-108">Außerdem können fensterlose Objekte nicht rechteckig und transparent sein.</span><span class="sxs-lookup"><span data-stu-id="c3d25-108">In addition, windowless objects can be nonrectangular and transparent.</span></span>

### <a name="overviews"></a><span data-ttu-id="c3d25-109">Übersichten</span><span class="sxs-lookup"><span data-stu-id="c3d25-109">Overviews</span></span>



| <span data-ttu-id="c3d25-110">Thema</span><span class="sxs-lookup"><span data-stu-id="c3d25-110">Topic</span></span>                                                                          | <span data-ttu-id="c3d25-111">Inhalte</span><span class="sxs-lookup"><span data-stu-id="c3d25-111">Contents</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3d25-112">Informationen zu fensterlosen Bearbeitungs Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="c3d25-112">About Windowless Rich Edit Controls</span></span>](about-windowless-rich-edit-controls.md) | <span data-ttu-id="c3d25-113">Ein fensterloses Rich Edit-Steuerelement, das auch als Text Dienste-Objekt bezeichnet wird, ist ein Objekt, das die Funktionalität eines [Rich-Edit-Steuer](rich-edit-controls.md) Elements bereitstellt, ohne das Fenster bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c3d25-113">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="c3d25-114">Functions</span><span class="sxs-lookup"><span data-stu-id="c3d25-114">Functions</span></span>



| <span data-ttu-id="c3d25-115">Thema</span><span class="sxs-lookup"><span data-stu-id="c3d25-115">Topic</span></span>                                            | <span data-ttu-id="c3d25-116">Inhalte</span><span class="sxs-lookup"><span data-stu-id="c3d25-116">Contents</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3d25-117">**"Kreatetextservices"**</span><span class="sxs-lookup"><span data-stu-id="c3d25-117">**CreateTextServices**</span></span>](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | <span data-ttu-id="c3d25-118">Die Funktion " [**kreatetextservices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) " erstellt eine Instanz eines Text Dienst Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3d25-118">The [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function creates an instance of a text services object.</span></span> <span data-ttu-id="c3d25-119">Das Text Services-Objekt unterstützt eine Vielzahl von Schnittstellen, einschließlich [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und dem Textobjekt Modell (Tom).</span><span class="sxs-lookup"><span data-stu-id="c3d25-119">The text services object supports a variety of interfaces, including [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and the Text Object Model (TOM).</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="c3d25-120">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c3d25-120">Interfaces</span></span>



| <span data-ttu-id="c3d25-121">Thema</span><span class="sxs-lookup"><span data-stu-id="c3d25-121">Topic</span></span>                                  | <span data-ttu-id="c3d25-122">Inhalte</span><span class="sxs-lookup"><span data-stu-id="c3d25-122">Contents</span></span>                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3d25-123">**Itexthost**</span><span class="sxs-lookup"><span data-stu-id="c3d25-123">**ITextHost**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | <span data-ttu-id="c3d25-124">Die [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle wird von einem Text Dienst Objekt zum Abrufen von Text Host Diensten verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3d25-124">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface is used by a text services object to obtain text host services.</span></span><br/> |
| [<span data-ttu-id="c3d25-125">**Itextservices**</span><span class="sxs-lookup"><span data-stu-id="c3d25-125">**ITextServices**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itextservices) | <span data-ttu-id="c3d25-126">Erweitert den Tom, um zusätzliche Funktionen für den fensterlosen Betrieb bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c3d25-126">Extends the TOM to provide extra functionality for windowless operation.</span></span><br/>                                     |



 

 

 





