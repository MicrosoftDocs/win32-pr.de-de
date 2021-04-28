---
title: Los geht's Entwickeln der Benutzeroberfläche für Windows-Apps
description: Erste Schritte Entwickeln von Benutzeroberflächen für Windows-Anwendungen
ms.assetid: 29d6f67b-46fa-4f39-a319-306c832eff9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10b7e6bd21b782e31c9285c9840b7247a12e606
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091078"
---
# <a name="getting-started-developing-user-interfaces-for-windows-applications"></a><span data-ttu-id="d15f6-103">Erste Schritte Entwickeln von Benutzeroberflächen für Windows-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d15f6-103">Getting Started Developing User Interfaces for Windows Applications</span></span>

## <a name="purpose"></a><span data-ttu-id="d15f6-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="d15f6-104">Purpose</span></span>

<span data-ttu-id="d15f6-105">Die folgenden Abschnitte bieten entwicklern, die die Benutzeroberfläche einer Windows-Anwendung entwerfen, implementieren und testen, allgemeine Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="d15f6-105">The following sections offer general guidance to developers who are designing, implementing, and testing the user interface of a Windows application.</span></span>

<span data-ttu-id="d15f6-106">Zusätzlich zu den grundlegenden Entwurfsprinzipien der Benutzeroberfläche werden zahlreiche Empfehlungen und Vorschläge bereitgestellt, die Entwicklern dabei helfen, eine benutzerfreundliche, möglichst einfache, effiziente und unkomplizierte Benutzeroberfläche zu bieten.</span><span class="sxs-lookup"><span data-stu-id="d15f6-106">In addition to basic user interface design principles, numerous recommendations and suggestions are provided that will help developers provide a user experience that is as simple, efficient, and enjoyable as possible.</span></span>

> [!Note]  
> <span data-ttu-id="d15f6-107">Diese Richtlinien sind nicht als umfassend gedacht und unterliegen dem spezifischen Umfang und der Funktionalität einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d15f6-107">These guidelines are not intended to be comprehensive and are subject to the specific scope and functionality of an application.</span></span> <span data-ttu-id="d15f6-108">Umfassendere Richtlinien finden Sie unter [Windows User Experience Interaction Guidelines (Richtlinien für die Interaktion mit der Windows-Benutzeroberfläche).](../uxguide/guidelines.md)</span><span class="sxs-lookup"><span data-stu-id="d15f6-108">For more comprehensive guidelines, see the [Windows User Experience Interaction Guidelines](../uxguide/guidelines.md).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="d15f6-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d15f6-109">In this section</span></span>



| <span data-ttu-id="d15f6-110">Thema</span><span class="sxs-lookup"><span data-stu-id="d15f6-110">Topic</span></span>                                                                            | <span data-ttu-id="d15f6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d15f6-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d15f6-112">Übersicht über den Benutzeroberfläche Entwicklungsprozess</span><span class="sxs-lookup"><span data-stu-id="d15f6-112">Overview of the User Interface Development Process</span></span>](the-process.md)<br/> | <span data-ttu-id="d15f6-113">In diesem Abschnitt werden die drei Phasen des Benutzeroberflächenentwurfs beschrieben und die Aufgaben erläutert, die in der Regel den einzelnen Phasen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d15f6-113">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span><br/>                                              |
| [<span data-ttu-id="d15f6-114">Entwerfen eines Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d15f6-114">Designing a User Interface</span></span>](designing-a-user-interface.md)<br/>          | <span data-ttu-id="d15f6-115">In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Entwerfen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d15f6-115">This section describes in detail some of the tasks associated with designing a UI for a Windows application.</span></span><br/>                                                                         |
| [<span data-ttu-id="d15f6-116">Implementieren eines Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d15f6-116">Implementing a User Interface</span></span>](implementing-a-user-interface.md)<br/>    | <span data-ttu-id="d15f6-117">In diesem Abschnitt werden einige der Aufgaben beschrieben, die mit der Implementierung einer Benutzeroberfläche für eine Windows-Anwendung verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="d15f6-117">This section describes some of the tasks associated with implementing a user interface for a Windows application.</span></span><br/>                                                                    |
| [<span data-ttu-id="d15f6-118">Testen eines Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d15f6-118">Testing a User Interface</span></span>](testing-a-user-interface.md)<br/>              | <span data-ttu-id="d15f6-119">In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Testen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d15f6-119">This section describes in detail some of the tasks associated with testing a UI for a Windows application.</span></span><br/>                                                                           |
| [<span data-ttu-id="d15f6-120">Sicherheitsüberlegungen: Windows Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d15f6-120">Security Considerations: Windows User Interface</span></span>](sec-ui.md)<br/>         | <span data-ttu-id="d15f6-121">Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Windows Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="d15f6-121">This topic provides information about security considerations in the Windows User Interface.</span></span><br/>                                                                                         |
| [<span data-ttu-id="d15f6-122">Andere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d15f6-122">Other Resources</span></span>](other-resources.md)<br/>                                | <span data-ttu-id="d15f6-123">Dieser Abschnitt enthält eine Liste der empfohlenen Bücher und Ressourcen im Zusammenhang mit dem Entwurf der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="d15f6-123">This section contains a list of recommended books and resources related to user interface design.</span></span> <span data-ttu-id="d15f6-124">(Diese Bücher und Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="d15f6-124">(These books and resources may not be available in some languages and countries.)</span></span> <br/> |



 

 

