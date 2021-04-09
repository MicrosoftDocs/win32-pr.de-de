---
description: Eine Verwaltungs Anwendung, die den System Registrierungs Anbieter verwendet, kann Klassen mit Eigenschaften definieren, die Registrierungsdaten für bestimmte Schlüssel darstellen. Anschließend werden die Klassen im WMI-Repository gespeichert.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definieren von Klassen für den System Registrierungs Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960302"
---
# <a name="defining-classes-for-the-system-registry-provider"></a><span data-ttu-id="6022d-103">Definieren von Klassen für den System Registrierungs Anbieter</span><span class="sxs-lookup"><span data-stu-id="6022d-103">Defining Classes for the System Registry Provider</span></span>

<span data-ttu-id="6022d-104">Eine Verwaltungs Anwendung, die den System Registrierungs Anbieter verwendet, kann Klassen mit Eigenschaften definieren, die Registrierungsdaten für bestimmte Schlüssel darstellen. Anschließend werden die Klassen im WMI-Repository gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6022d-104">A management application using the System Registry provider can define classes with properties that represent registry data for particular keys and then stores the classes in the WMI repository.</span></span> <span data-ttu-id="6022d-105">Die meisten Prozesse zum Definieren einer Klasse für die Systemregistrierung sind identisch mit der Definition einer anderen Klasse.</span><span class="sxs-lookup"><span data-stu-id="6022d-105">Most of the processes for defining a class for the system registry is identical to defining any other class.</span></span> <span data-ttu-id="6022d-106">Der System Registrierungs Anbieter erfordert jedoch, dass Sie bestimmte Datentypen und Qualifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="6022d-106">However, the System Registry provider requires that you use specific data types and qualifiers.</span></span>

<span data-ttu-id="6022d-107">Im folgenden Verfahren wird beschrieben, wie Sie eine Klasse für den System Registrierungs Anbieter definieren.</span><span class="sxs-lookup"><span data-stu-id="6022d-107">The following procedure describes how to define a class for the System Registry provider.</span></span>

<span data-ttu-id="6022d-108">**So definieren Sie eine Klasse für den System Registrierungs Anbieter**</span><span class="sxs-lookup"><span data-stu-id="6022d-108">**To define a class for the System Registry provider**</span></span>

1.  <span data-ttu-id="6022d-109">Erstellen Sie die Klasse wie jede andere Klasse.</span><span class="sxs-lookup"><span data-stu-id="6022d-109">Create the class as you would any other class.</span></span>

    <span data-ttu-id="6022d-110">Weitere Informationen finden Sie unter [Creating a Class](creating-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="6022d-110">For more information, see [Creating a Class](creating-a-class.md).</span></span>

2.  <span data-ttu-id="6022d-111">Ordnen Sie die entsprechenden Registrierungs Datentypen den entsprechenden WMI-Typen zu.</span><span class="sxs-lookup"><span data-stu-id="6022d-111">Map the appropriate registry data types to the appropriate WMI types.</span></span>

    <span data-ttu-id="6022d-112">Der System Registrierungs Anbieter ordnet die Registrierungs Datentypen bestimmten WMI-Datentypen zu.</span><span class="sxs-lookup"><span data-stu-id="6022d-112">The System Registry provider maps the registry data types to specific WMI data types.</span></span> <span data-ttu-id="6022d-113">Weitere Informationen finden Sie unter [Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="6022d-113">For more information, see [Mapping a Registry Data Type to a WMI Data Type](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span></span>

3.  <span data-ttu-id="6022d-114">Verwenden Sie die erforderlichen Qualifizierer, um den Speicherort des Registrierungs Anbieters und den Speicherort des entsprechenden Registrierungsschlüssels zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6022d-114">Use the required qualifiers to define the location of the Registry provider and the location of the appropriate registry key.</span></span>

    <span data-ttu-id="6022d-115">Der System Registrierungs Anbieter verwendet drei Qualifizierer, um den Speicherort verschiedener Klassen, Anbieter und Registrierungseinträge zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6022d-115">The System Registry provider uses three qualifiers to define the location of various classes, providers, and registry entries.</span></span> <span data-ttu-id="6022d-116">Weitere Informationen finden Sie unter [Definieren einer Registrierungs Klasse mit Qualifizierern](defining-a-registry-class-with-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="6022d-116">For more information, see [Defining a Registry Class With Qualifiers](defining-a-registry-class-with-qualifiers.md).</span></span>

 

 



