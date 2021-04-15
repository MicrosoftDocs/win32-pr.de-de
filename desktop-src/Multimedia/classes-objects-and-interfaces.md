---
title: Klassen, Objekte und Schnittstellen
description: Klassen, Objekte und Schnittstellen
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474614"
---
# <a name="classes-objects-and-interfaces"></a><span data-ttu-id="7c53c-103">Klassen, Objekte und Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7c53c-103">Classes, Objects, and Interfaces</span></span>

<span data-ttu-id="7c53c-104">In der Programmiersprache C++ besteht eine- *Klasse* aus *Eigenschaften* (oder Elementdaten) und *Methoden* (oder Element Funktionen).</span><span class="sxs-lookup"><span data-stu-id="7c53c-104">In the C++ programming language, a *class* consists of *properties* (or member data) and *methods* (or member functions).</span></span> <span data-ttu-id="7c53c-105">Die Eigenschaften sind Datenelemente, die in einer Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7c53c-105">The properties are data elements, such as those contained in a structure.</span></span> <span data-ttu-id="7c53c-106">Die Methoden werden für eine Vielzahl von Zwecken verwendet, wie z. b. Initialisierung, Zuweisung, Vorgänge und Datenzugriff.</span><span class="sxs-lookup"><span data-stu-id="7c53c-106">The methods are used for a variety of purposes, such as initialization, assignment, operations, and data access.</span></span> <span data-ttu-id="7c53c-107">Eine Klassen Deklaration wird auf die gleiche Weise wie eine Struktur Deklaration verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c53c-107">You use a class declaration in the same way that you use a structure declaration.</span></span> <span data-ttu-id="7c53c-108">Arbeitsspeicher wird für eine Klasse zugewiesen, wenn Sie ein Klassen *Objekt* definieren.</span><span class="sxs-lookup"><span data-stu-id="7c53c-108">Memory is allocated for a class when you define a class *object*.</span></span> <span data-ttu-id="7c53c-109">Jedes Klassenobjekt verfügt über einen Datenbereich für seine Eigenschaften und eine Tabelle mit Zeigern auf die unterstützten Methoden.</span><span class="sxs-lookup"><span data-stu-id="7c53c-109">Each class object has a data area for its properties and a table of pointers to the methods it supports.</span></span>

<span data-ttu-id="7c53c-110">In OLE besteht ein Objekt aus Daten und Methoden, wie es in C++ der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="7c53c-110">In OLE, an object consists of data and methods, as it does in C++.</span></span> <span data-ttu-id="7c53c-111">Ein OLE-Objekt befolgt jedoch strengere Regeln.</span><span class="sxs-lookup"><span data-stu-id="7c53c-111">However, an OLE object adheres to stricter rules.</span></span> <span data-ttu-id="7c53c-112">Die Daten sind streng intern.</span><span class="sxs-lookup"><span data-stu-id="7c53c-112">The data is strictly internal.</span></span> <span data-ttu-id="7c53c-113">Ein-Objekt macht nur Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7c53c-113">An object only exposes interfaces.</span></span> <span data-ttu-id="7c53c-114">Eine *Schnittstelle* ist ein Satz verwandter Methoden für ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="7c53c-114">An *interface* is a set of related methods for an object.</span></span> <span data-ttu-id="7c53c-115">Jedes-Objekt kann mehrere Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7c53c-115">Each object can support multiple interfaces.</span></span> <span data-ttu-id="7c53c-116">Alle OLE-Schnittstellen unterstützen die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7c53c-116">All OLE interfaces support the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

 

 




