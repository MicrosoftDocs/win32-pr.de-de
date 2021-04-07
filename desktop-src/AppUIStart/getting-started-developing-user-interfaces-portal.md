---
title: Einstieg in die Entwicklung von Benutzeroberflächen für Windows-apps
description: .
ms.assetid: 29d6f67b-46fa-4f39-a319-306c832eff9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c3d1a182aef6354901f0fa71f94b39ecdc58f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729112"
---
# <a name="getting-started-developing-user-interfaces-for-windows-applications"></a><span data-ttu-id="c0f11-103">Einstieg in die Entwicklung von Benutzeroberflächen für Windows-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c0f11-103">Getting Started Developing User Interfaces for Windows Applications</span></span>

## <a name="purpose"></a><span data-ttu-id="c0f11-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="c0f11-104">Purpose</span></span>

<span data-ttu-id="c0f11-105">Die folgenden Abschnitte bieten allgemeine Anleitungen für Entwickler, die die Benutzeroberfläche einer Windows-Anwendung entwerfen, implementieren und testen.</span><span class="sxs-lookup"><span data-stu-id="c0f11-105">The following sections offer general guidance to developers who are designing, implementing, and testing the user interface of a Windows application.</span></span>

<span data-ttu-id="c0f11-106">Zusätzlich zu den grundlegenden Entwurfs Prinzipien für die Benutzeroberfläche werden zahlreiche Empfehlungen und Vorschläge bereitgestellt, mit deren Hilfe Entwickler eine Benutzeroberfläche bereitstellen können, die so einfach, effizient und unterhaltsam wie möglich ist.</span><span class="sxs-lookup"><span data-stu-id="c0f11-106">In addition to basic user interface design principles, numerous recommendations and suggestions are provided that will help developers provide a user experience that is as simple, efficient, and enjoyable as possible.</span></span>

> [!Note]  
> <span data-ttu-id="c0f11-107">Diese Richtlinien sind nicht als umfassend gedacht und unterliegen dem spezifischen Bereich und der Funktionalität einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c0f11-107">These guidelines are not intended to be comprehensive and are subject to the specific scope and functionality of an application.</span></span> <span data-ttu-id="c0f11-108">Umfassendere Richtlinien finden Sie in den [Windows-Richtlinien](../uxguide/guidelines.md)für die benutzerfreundliche Interaktion.</span><span class="sxs-lookup"><span data-stu-id="c0f11-108">For more comprehensive guidelines, see the [Windows User Experience Interaction Guidelines](../uxguide/guidelines.md).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="c0f11-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c0f11-109">In this section</span></span>



| <span data-ttu-id="c0f11-110">Thema</span><span class="sxs-lookup"><span data-stu-id="c0f11-110">Topic</span></span>                                                                            | <span data-ttu-id="c0f11-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0f11-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0f11-112">Übersicht über den Entwicklungsprozess der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c0f11-112">Overview of the User Interface Development Process</span></span>](the-process.md)<br/> | <span data-ttu-id="c0f11-113">In diesem Abschnitt werden die drei Phasen des Entwurfs von Benutzeroberflächen beschrieben und die Aufgaben eingeführt, die in der Regel mit den einzelnen Phasen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c0f11-113">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span><br/>                                              |
| [<span data-ttu-id="c0f11-114">Entwerfen einer Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c0f11-114">Designing a User Interface</span></span>](designing-a-user-interface.md)<br/>          | <span data-ttu-id="c0f11-115">In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Entwerfen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0f11-115">This section describes in detail some of the tasks associated with designing a UI for a Windows application.</span></span><br/>                                                                         |
| [<span data-ttu-id="c0f11-116">Implementieren einer Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c0f11-116">Implementing a User Interface</span></span>](implementing-a-user-interface.md)<br/>    | <span data-ttu-id="c0f11-117">In diesem Abschnitt werden einige der Aufgaben beschrieben, die mit der Implementierung einer Benutzeroberfläche für eine Windows-Anwendung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c0f11-117">This section describes some of the tasks associated with implementing a user interface for a Windows application.</span></span><br/>                                                                    |
| [<span data-ttu-id="c0f11-118">Testen einer Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c0f11-118">Testing a User Interface</span></span>](testing-a-user-interface.md)<br/>              | <span data-ttu-id="c0f11-119">In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Testen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c0f11-119">This section describes in detail some of the tasks associated with testing a UI for a Windows application.</span></span><br/>                                                                           |
| [<span data-ttu-id="c0f11-120">Sicherheitsüberlegungen: Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c0f11-120">Security Considerations: Windows User Interface</span></span>](sec-ui.md)<br/>         | <span data-ttu-id="c0f11-121">Dieses Thema enthält Informationen zu Sicherheitsüberlegungen in der Windows-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c0f11-121">This topic provides information about security considerations in the Windows User Interface.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c0f11-122">Andere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c0f11-122">Other Resources</span></span>](other-resources.md)<br/>                                | <span data-ttu-id="c0f11-123">Dieser Abschnitt enthält eine Liste der empfohlenen Bücher und Ressourcen, die sich auf das Design der Benutzeroberfläche beziehen.</span><span class="sxs-lookup"><span data-stu-id="c0f11-123">This section contains a list of recommended books and resources related to user interface design.</span></span> <span data-ttu-id="c0f11-124">(Diese Bücher und Ressourcen sind möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="c0f11-124">(These books and resources may not be available in some languages and countries.)</span></span> <br/> |



 

 

