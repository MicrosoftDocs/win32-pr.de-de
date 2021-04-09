---
title: Konzepte der C++-und OLE-Programmierung
description: Konzepte der C++-und OLE-Programmierung
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856944"
---
# <a name="c-and-ole-programming-concepts"></a><span data-ttu-id="fe40b-103">Konzepte der C++-und OLE-Programmierung</span><span class="sxs-lookup"><span data-stu-id="fe40b-103">C++ and OLE Programming Concepts</span></span>

<span data-ttu-id="fe40b-104">Die in Windows enthaltenen Datei-und Datenstrom Handler verwenden einen objektorientierten Entwurf zum herauf Stufen einer Standardschnittstelle und zum Freigeben von Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fe40b-104">The file and stream handlers included with Windows use an object-oriented design to promote a standard interface and to share functionality.</span></span> <span data-ttu-id="fe40b-105">Diese Handler sind in C++ geschrieben und verwenden die OLE-Component Object Model.</span><span class="sxs-lookup"><span data-stu-id="fe40b-105">These handlers are written in C++ and use the OLE Component Object Model.</span></span>

<span data-ttu-id="fe40b-106">Sie können benutzerdefinierte Handler mithilfe der C-oder C++-Entwicklungssysteme entwickeln; Allerdings wird die Verwendung von C++ dringend empfohlen, da Sie einen einfacheren und einfacheren Ansatz zum Implementieren eines Handlers bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fe40b-106">You can develop custom handlers using the C or C++ development systems; however, using C++ is strongly recommended, because it provides an easier and more straightforward approach to implement a handler.</span></span> <span data-ttu-id="fe40b-107">Mit C++ können Sie Daten explizit als Objekte definieren, und Sie können die Funktionen, die die Daten bearbeiten, mit den Element Funktionen eines Objekts verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="fe40b-107">Using C++, you can explicitly define data as objects, and you can associate the functions that manipulate the data with the member functions of an object.</span></span>

<span data-ttu-id="fe40b-108">Dieser Abschnitt enthält eine kurze Zusammenfassung der wichtigen Konzepte von C++ und der OLE-Component Object Model, die für das Entwerfen und Implementieren von Datei-und streamhandlern gelten.</span><span class="sxs-lookup"><span data-stu-id="fe40b-108">This section identifies and briefly summarizes the important concepts of C++ and the OLE Component Object Model that apply to designing and implementing file and stream handlers.</span></span> <span data-ttu-id="fe40b-109">Es gibt zahlreiche Bücher über C++ Programming, auf die Sie verweisen können, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fe40b-109">There are many books written about C++ programming that you can reference for more information.</span></span> <span data-ttu-id="fe40b-110">Weitere Informationen zu OLE finden Sie in der *OLE-Programmier Referenz*.</span><span class="sxs-lookup"><span data-stu-id="fe40b-110">For more information on OLE, please see the *OLE Programmer's Reference*.</span></span>

 

 




