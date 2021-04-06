---
title: Erste Schritte mit Win32 und C++
description: Das Ziel dieser Reihe von ersten Schritten besteht darin, Ihnen zu zeigen, wie Sie ein Desktop Programm in C++ mithilfe von Win32-und com-APIs schreiben.
ms.assetid: a9470cb9-a1e7-4d6d-a4be-61b81d209ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b1ad80530877e9502d158a16295013e3f4a05e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714147"
---
# <a name="get-started-with-win32-and-c"></a><span data-ttu-id="f2bfe-103">Erste Schritte mit Win32 und C++</span><span class="sxs-lookup"><span data-stu-id="f2bfe-103">Get Started with Win32 and C++</span></span>

<span data-ttu-id="f2bfe-104">Das Ziel dieser Reihe von ersten Schritten besteht darin, Ihnen zu zeigen, wie Sie ein Desktop Programm in C++ mithilfe von Win32-und com-APIs schreiben.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-104">The aim of this Get Started series is to teach you how to write a desktop program in C++ using Win32 and COM APIs.</span></span>

<span data-ttu-id="f2bfe-105">Im ersten Modul erfahren Sie Schritt für Schritt, wie Sie ein Fenster erstellen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-105">In the first module, you'll learn step-by-step how to create and show a window.</span></span> <span data-ttu-id="f2bfe-106">Spätere Module stellen die Component Object Model (com), Grafiken und Text sowie Benutzereingaben vor.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-106">Later modules will introduce the Component Object Model (COM), graphics and text, and user input.</span></span>

<span data-ttu-id="f2bfe-107">Bei dieser Serie wird davon ausgegangen, dass Sie über ein gutes Wissen in der C++-Programmierung verfügen.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-107">For this series, it is assumed that you have a good working knowledge of C++ programming.</span></span> <span data-ttu-id="f2bfe-108">Es wird nicht mit der Windows-Programmierung begonnen.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-108">No previous experience with Windows programming is assumed.</span></span> <span data-ttu-id="f2bfe-109">Wenn Sie noch nicht mit C++ vertraut sind, finden Sie im [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx)Lernmaterial.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-109">If you are new to C++, you can find learning material at the [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx).</span></span> <span data-ttu-id="f2bfe-110">(Diese Ressource ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="f2bfe-110">(This resource may not be available in some languages and countries.)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f2bfe-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f2bfe-111">In this section</span></span>



| <span data-ttu-id="f2bfe-112">Thema</span><span class="sxs-lookup"><span data-stu-id="f2bfe-112">Topic</span></span>                                                                                                     | <span data-ttu-id="f2bfe-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2bfe-113">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2bfe-114">Einführung in die Windows-Programmierung in C++</span><span class="sxs-lookup"><span data-stu-id="f2bfe-114">Introduction to Windows Programming in C++</span></span>](introduction-to-windows-programming-in-c--.md)<br/>   | <span data-ttu-id="f2bfe-115">In diesem Abschnitt werden einige grundlegende Terminologie und Codierungs Konventionen beschrieben, die bei der Windows-Programmierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-115">This section describes some of the basic terminology and coding conventions used in Windows programming.</span></span><br/>  |
| [<span data-ttu-id="f2bfe-116">Modul 1. Ihr erstes Windows-Programm</span><span class="sxs-lookup"><span data-stu-id="f2bfe-116">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)<br/>                         | <span data-ttu-id="f2bfe-117">In diesem Modul erstellen Sie ein einfaches Windows-Programm, das ein leeres Fenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-117">In this module, you will create a simple Windows program that shows a blank window.</span></span><br/>                       |
| [<span data-ttu-id="f2bfe-118">Modul 2. Verwenden von com in Ihrem Windows-Programm</span><span class="sxs-lookup"><span data-stu-id="f2bfe-118">Module 2. Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)<br/> | <span data-ttu-id="f2bfe-119">Dieses Modul führt den Component Object Model (com) ein, der vielen modernen Windows-APIs zugrunde liegt.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-119">This module introduces the Component Object Model (COM), which underlies many of the modern Windows APIs.</span></span><br/> |
| [<span data-ttu-id="f2bfe-120">Modul 3. Windows-Grafiken</span><span class="sxs-lookup"><span data-stu-id="f2bfe-120">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)<br/>                                  | <span data-ttu-id="f2bfe-121">Mit diesem Modul wird die Windows-Grafik Architektur eingeführt, wobei der Schwerpunkt auf Direct2D liegt.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-121">This module introduces the Windows graphics architecture, with a focus on Direct2D.</span></span><br/>                       |
| [<span data-ttu-id="f2bfe-122">Modul 4. Benutzereingabe</span><span class="sxs-lookup"><span data-stu-id="f2bfe-122">Module 4. User Input</span></span>](module-4--user-input.md)<br/>                                               | <span data-ttu-id="f2bfe-123">Dieses Modul beschreibt die Maus-und Tastatureingaben.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-123">This module describes mouse and keyboard input.</span></span><br/>                                                           |
| [<span data-ttu-id="f2bfe-124">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="f2bfe-124">Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)<br/>                                   | <span data-ttu-id="f2bfe-125">Enthält Links zum Herunterladen des Beispielcodes für diese Reihe.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-125">Contains links to download the sample code for this series.</span></span><br/>                                               |



 

 

 





