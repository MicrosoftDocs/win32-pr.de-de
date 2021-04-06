---
title: Benutzerdefiniertes Zeichnen
description: Das benutzerdefinierte Zeichnen ist kein gängiges Steuerelement. Es handelt sich um einen Dienst, den viele gängige Steuerelemente bereitstellen.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947517"
---
# <a name="custom-draw"></a><span data-ttu-id="937b5-103">Benutzerdefiniertes Zeichnen</span><span class="sxs-lookup"><span data-stu-id="937b5-103">Custom Draw</span></span>

<span data-ttu-id="937b5-104">Das benutzerdefinierte Zeichnen ist kein gängiges Steuerelement. Es handelt sich um einen Dienst, den viele gängige Steuerelemente bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="937b5-104">Custom draw is not a common control; it is a service that many common controls provide.</span></span> <span data-ttu-id="937b5-105">Der benutzerdefinierte Draw-Dienst ermöglicht einer Anwendung eine größere Flexibilität beim Anpassen der Darstellung eines Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="937b5-105">The custom draw service allows an application greater flexibility in customizing a control's appearance.</span></span> <span data-ttu-id="937b5-106">Die Anwendung kann benutzerdefinierte Zeichnungs Benachrichtigungen nutzen, um die Schriftart, die zum Anzeigen von Elementen verwendet wird, zu ändern oder ein Element manuell zu zeichnen, ohne dass ein vollständiger Besitzer gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="937b5-106">Your application can harness custom draw notifications to easily change the font used to display items or manually draw an item without having to do a full owner draw.</span></span>

<span data-ttu-id="937b5-107">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit benutzerdefiniertem Zeichnen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="937b5-107">This section contains information about the programming elements used with custom draw.</span></span>

## <a name="overviews"></a><span data-ttu-id="937b5-108">Übersichten</span><span class="sxs-lookup"><span data-stu-id="937b5-108">Overviews</span></span>



| <span data-ttu-id="937b5-109">Thema</span><span class="sxs-lookup"><span data-stu-id="937b5-109">Topic</span></span>                                      | <span data-ttu-id="937b5-110">Inhalte</span><span class="sxs-lookup"><span data-stu-id="937b5-110">Contents</span></span>                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="937b5-111">Informationen zum benutzerdefinierten Zeichnen</span><span class="sxs-lookup"><span data-stu-id="937b5-111">About Custom Draw</span></span>](about-custom-draw.md) | <span data-ttu-id="937b5-112">Dieser Abschnitt enthält allgemeine Informationen über benutzerdefinierte Zeichnungsfunktionen und bietet eine konzeptionelle Übersicht darüber, wie eine Anwendung benutzerdefiniertes Zeichnen unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="937b5-112">This section contains general information about custom draw functionality and provides a conceptual overview of how an application can support custom draw.</span></span><br/> |
| [<span data-ttu-id="937b5-113">Verwenden benutzerdefinierter zeichnen</span><span class="sxs-lookup"><span data-stu-id="937b5-113">Using Custom Draw</span></span>](using-custom-draw.md) | <span data-ttu-id="937b5-114">Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="937b5-114">This section contains examples that demonstrate how to implement custom draw.</span></span> <br/>                                                                              |



 

## <a name="notifications"></a><span data-ttu-id="937b5-115">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="937b5-115">Notifications</span></span>



| <span data-ttu-id="937b5-116">Thema</span><span class="sxs-lookup"><span data-stu-id="937b5-116">Topic</span></span>                               | <span data-ttu-id="937b5-117">Inhalte</span><span class="sxs-lookup"><span data-stu-id="937b5-117">Contents</span></span>                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="937b5-118">NM \_ customdraw</span><span class="sxs-lookup"><span data-stu-id="937b5-118">NM\_CUSTOMDRAW</span></span>](nm-customdraw.md) | <span data-ttu-id="937b5-119">Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="937b5-119">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="937b5-120">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="937b5-120">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

## <a name="structures"></a><span data-ttu-id="937b5-121">Strukturen</span><span class="sxs-lookup"><span data-stu-id="937b5-121">Structures</span></span>



| <span data-ttu-id="937b5-122">Thema</span><span class="sxs-lookup"><span data-stu-id="937b5-122">Topic</span></span>                                | <span data-ttu-id="937b5-123">Inhalte</span><span class="sxs-lookup"><span data-stu-id="937b5-123">Contents</span></span>                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="937b5-124">**Nmcustomdraw**</span><span class="sxs-lookup"><span data-stu-id="937b5-124">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | <span data-ttu-id="937b5-125">Enthält Informationen, die für einen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Code spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="937b5-125">Contains information specific to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span><br/> |



 

 

 





