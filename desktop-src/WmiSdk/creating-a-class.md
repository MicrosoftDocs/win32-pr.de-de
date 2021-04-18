---
description: In WMI ist eine Klasse ein Objekt, das einen Aspekt eines Unternehmens beschreibt, z. b. eine besondere Art von Laufwerk.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Erstellen einer WMI-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351505"
---
# <a name="creating-a-wmi-class"></a><span data-ttu-id="60994-103">Erstellen einer WMI-Klasse</span><span class="sxs-lookup"><span data-stu-id="60994-103">Creating a WMI Class</span></span>

<span data-ttu-id="60994-104">In WMI ist eine Klasse ein Objekt, das einen Aspekt eines Unternehmens beschreibt, z. b. eine besondere Art von Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="60994-104">In WMI, a class is an object that describes some aspect of an enterprise, such as a special type of disk drive.</span></span> <span data-ttu-id="60994-105">Nachdem Sie eine Klassendefinition erstellt haben, schreiben Sie die Anbieter-DLL, um Instanzen der Klasse, der Eigenschafts Daten und der Ausführungsmethoden bereitzustellen, die für die Klasse definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="60994-105">After you have created a class definition, write your provider DLL to supply instances of the class, property data, and execute methods defined for the class.</span></span> <span data-ttu-id="60994-106">Skripts und Anwendungen können dann Daten abrufen oder das Gerät steuern.</span><span class="sxs-lookup"><span data-stu-id="60994-106">Scripts and applications can then obtain data or control the device.</span></span> <span data-ttu-id="60994-107">Weitere Informationen finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="60994-107">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="60994-108">Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Anweisungs Präprozessoranweisung in der MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="60994-108">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) statement preprocessor instruction in your MOF file.</span></span>

 

## <a name="base-class"></a><span data-ttu-id="60994-109">Basisklasse</span><span class="sxs-lookup"><span data-stu-id="60994-109">Base Class</span></span>

<span data-ttu-id="60994-110">Eine Basisklasse stellt ein allgemeines Konzept dar.</span><span class="sxs-lookup"><span data-stu-id="60994-110">A base class represents some general concept.</span></span> <span data-ttu-id="60994-111">Die [**CIM- \_ cdromdrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) -Klasse stellt beispielsweise alle Arten von CD-ROM-Laufwerken in WMI dar und enthält allgemeine Eigenschaften, die alle Arten von CD-ROM-Laufwerken beschreiben.</span><span class="sxs-lookup"><span data-stu-id="60994-111">For example, the [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) class represents all types of CD-ROM drives in WMI, and contains general properties that describe all kinds of CD-ROM drives.</span></span> <span data-ttu-id="60994-112">Weitere Informationen finden Sie unter [Erstellen einer Basisklasse](creating-a-base-class.md).</span><span class="sxs-lookup"><span data-stu-id="60994-112">For more information, see [Creating a Base Class](creating-a-base-class.md).</span></span>

<span data-ttu-id="60994-113">Eine abgeleitete Klasse erbt Eigenschaften und Methoden von einer anderen Klasse.</span><span class="sxs-lookup"><span data-stu-id="60994-113">A derived class inherits properties and methods from another class.</span></span> <span data-ttu-id="60994-114">Eine abgeleitete Klasse stellt in der Regel einen bestimmten Fall einer Basisklasse dar.</span><span class="sxs-lookup"><span data-stu-id="60994-114">A derived class usually represents a specific case of a base class.</span></span> <span data-ttu-id="60994-115">Beispielsweise stellt die [**Win32 \_ cdromdrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) -Klasse ein CD-ROM-Laufwerk in einem Windows-System dar.</span><span class="sxs-lookup"><span data-stu-id="60994-115">For example, the [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) class represents a CD-ROM drive on a Windows system.</span></span> <span data-ttu-id="60994-116">Die **Win32 \_ cdromdrive** -Klasse basiert auf und erbt viele Eigenschaften von [**CIM \_ cdromdrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span><span class="sxs-lookup"><span data-stu-id="60994-116">The **Win32\_CDROMDrive** class is based on and inherits many of properties from [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span></span> <span data-ttu-id="60994-117">Allerdings kann **Win32 \_ cdromdrive**, wie andere abgeleitete Klassen, über zusätzliche Eigenschaften verfügen, die die abgeleitete Klasse eindeutig machen.</span><span class="sxs-lookup"><span data-stu-id="60994-117">However, **Win32\_CDROMDrive**, like other derived classes, can have additional properties that make the derived class unique.</span></span> <span data-ttu-id="60994-118">Weitere Informationen finden Sie unter [Erstellen einer abgeleiteten Klasse](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="60994-118">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

## <a name="properties-and-methods"></a><span data-ttu-id="60994-119">Eigenschaften und Methoden</span><span class="sxs-lookup"><span data-stu-id="60994-119">Properties and Methods</span></span>

<span data-ttu-id="60994-120">Das Erstellen einer Klasse bedeutet, dass die Eigenschaften definiert werden, die diese Klasse beschreiben.</span><span class="sxs-lookup"><span data-stu-id="60994-120">Creating a class means defining the properties that describe that class.</span></span> <span data-ttu-id="60994-121">Sie können auch Methoden definieren, die das von der-Klasse dargestellte Objekt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="60994-121">You can also define methods that manipulate the object represented by the class.</span></span>

<span data-ttu-id="60994-122">Im Allgemeinen stellt eine Eigenschaft einen Aspekt des Objekts dar, z. b. eine Seriennummer für ein Gerät oder eine Größe in Byte für einen Prozess, während eine Methode eine Aktion darstellt, die den Zustand oder das Verhalten des Geräts oder der logischen Entität ändert.</span><span class="sxs-lookup"><span data-stu-id="60994-122">Generally, a property represents an aspect of the object, such as a serial number for a device or a size in bytes for a process, while a method represents an action that changes the state or behavior of the device or logical entity.</span></span>

<span data-ttu-id="60994-123">Jede Klasse muss mindestens eine Schlüsseleigenschaft haben.</span><span class="sxs-lookup"><span data-stu-id="60994-123">Each class must have at least one key property.</span></span> <span data-ttu-id="60994-124">Obwohl eine Klasse mehrere Schlüssel haben kann, können Sie keine Instanz einer Klasse mit mehr als 256 Schlüsseln erstellen.</span><span class="sxs-lookup"><span data-stu-id="60994-124">While a class may have multiple keys, you cannot create an instance of a class with more than 256 keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60994-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60994-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60994-126">Entwerfen von Managed Object Format-Klassen (MOF)</span><span class="sxs-lookup"><span data-stu-id="60994-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
