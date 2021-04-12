---
description: In diesem Thema wird beschrieben, was Sie tun müssen, um Programme zu erstellen, die die Sensor-API verwenden.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Allgemeine Anforderungen für die Anwendungsentwicklung (Sensor-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347648"
---
# <a name="general-requirements-for-application-development-sensor-api"></a><span data-ttu-id="c8eab-103">Allgemeine Anforderungen für die Anwendungsentwicklung (Sensor-API)</span><span class="sxs-lookup"><span data-stu-id="c8eab-103">General Requirements for Application Development (Sensor API)</span></span>

<span data-ttu-id="c8eab-104">In diesem Thema wird beschrieben, was Sie tun müssen, um Programme zu erstellen, die die Sensor-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8eab-104">This topic describes what you must do to start to create programs that use the Sensor API.</span></span>

<span data-ttu-id="c8eab-105">Zum Erstellen einer Sensor-API-Anwendung müssen Sie Windows 7 und das Windows 7 Software Development Kit (SDK) auf dem Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="c8eab-105">To create a Sensor API application, you must install Windows 7 and the Windows 7 Software Development Kit (SDK) on your computer.</span></span> <span data-ttu-id="c8eab-106">In der folgenden Tabelle werden die jeweiligen Dateien beschrieben, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="c8eab-106">The following table describes the specific files that you will need.</span></span>



| <span data-ttu-id="c8eab-107">Dateiname</span><span class="sxs-lookup"><span data-stu-id="c8eab-107">File name</span></span>               | <span data-ttu-id="c8eab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8eab-108">Description</span></span>                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8eab-109">Sensorsapi. h</span><span class="sxs-lookup"><span data-stu-id="c8eab-109">Sensorsapi.h</span></span>            | <span data-ttu-id="c8eab-110">Die Haupt Header Datei für die Sensor-API.</span><span class="sxs-lookup"><span data-stu-id="c8eab-110">The main header file for the Sensor API.</span></span> <span data-ttu-id="c8eab-111">Diese Header Datei enthält die Schnittstellendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c8eab-111">This header file contains the interface definitions.</span></span>               |
| <span data-ttu-id="c8eab-112">Sensoren. h</span><span class="sxs-lookup"><span data-stu-id="c8eab-112">Sensors.h</span></span>               | <span data-ttu-id="c8eab-113">Die Header Datei, die Definitionen von Platt Form definierten Konstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="c8eab-113">The header file that contains definitions of platform-defined constants.</span></span>                                    |
| <span data-ttu-id="c8eab-114">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="c8eab-114">Initguid.h</span></span>              | <span data-ttu-id="c8eab-115">Die Header Datei, die Definitionen zum Steuern der **GUID** -Initialisierung enthält.</span><span class="sxs-lookup"><span data-stu-id="c8eab-115">The header file that contains definitions for controlling **GUID** initialization.</span></span>                          |
| <span data-ttu-id="c8eab-116">Functiondiscoverykeys. h</span><span class="sxs-lookup"><span data-stu-id="c8eab-116">FunctionDiscoveryKeys.h</span></span> | <span data-ttu-id="c8eab-117">Die Header Datei, die die Eigenschaften Schlüssel der Geräte-ID definiert, die erforderlich sind, wenn Sie eine Verbindung mit logischen Sensoren herstellen.</span><span class="sxs-lookup"><span data-stu-id="c8eab-117">The header file that defines device ID property keys that are required when you connect to logical sensors.</span></span> |
| <span data-ttu-id="c8eab-118">Sensorsapi. lib</span><span class="sxs-lookup"><span data-stu-id="c8eab-118">Sensorsapi.lib</span></span>          | <span data-ttu-id="c8eab-119">Eine statische Bibliothek, die **GUID** -Definitionen für die Sensor-API enthält.</span><span class="sxs-lookup"><span data-stu-id="c8eab-119">A static library that contains **GUID** definitions for the Sensor API.</span></span>                                     |
| <span data-ttu-id="c8eab-120">Portabledeviceguids. lib</span><span class="sxs-lookup"><span data-stu-id="c8eab-120">PortableDeviceGuids.lib</span></span> | <span data-ttu-id="c8eab-121">Eine statische Bibliothek, die **GUID** -Definitionen für Objekte von tragbaren Windows-Geräten enthält.</span><span class="sxs-lookup"><span data-stu-id="c8eab-121">A static library that contains **GUID** definitions for Windows Portable Devices objects.</span></span>                   |



 

<span data-ttu-id="c8eab-122">Das Programm erfordert möglicherweise zusätzliche Dateien.</span><span class="sxs-lookup"><span data-stu-id="c8eab-122">Your program may require additional files.</span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="c8eab-123">Unterstützte Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="c8eab-123">Supported Operating Systems</span></span>

<span data-ttu-id="c8eab-124">Sensor-API-Anwendungen können mit Ausnahme von Windows 7 Starter Edition unter allen Editionen von Windows 7 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c8eab-124">Sensor API applications will run on all editions of Windows 7, except for Windows 7 Starter edition.</span></span>

## <a name="windows-portable-devices-interfaces"></a><span data-ttu-id="c8eab-125">Schnittstellen für tragbare Windows-Geräte</span><span class="sxs-lookup"><span data-stu-id="c8eab-125">Windows Portable Devices Interfaces</span></span>

<span data-ttu-id="c8eab-126">Die Sensor-API verwendet bestimmte Windows Portable Devices-Objekte (WPD) zum Kapseln von Eigenschafts Schlüsseln und-Werten.</span><span class="sxs-lookup"><span data-stu-id="c8eab-126">The Sensor API uses certain Windows Portable Devices (WPD) objects to encapsulate property keys and values.</span></span> <span data-ttu-id="c8eab-127">In der folgenden Tabelle werden die Schnittstellen für diese Objekte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8eab-127">The following table describes the interfaces for these objects.</span></span>



| <span data-ttu-id="c8eab-128">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c8eab-128">Interface</span></span>                                                                       | <span data-ttu-id="c8eab-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8eab-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8eab-130">[Iportablede vicevalues](/previous-versions//ms740012(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8eab-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span></span>        | <span data-ttu-id="c8eab-131">Diese Schnittstelle stellt eine bequeme Möglichkeit zum Erstellen eines Eigenschaften Behälters mit Name-Wert-Paaren dar.</span><span class="sxs-lookup"><span data-stu-id="c8eab-131">This interface provides a convenient way to create a property bag of name/value pairs.</span></span> <span data-ttu-id="c8eab-132">Namen werden durch **PropertyKey** s dargestellt, und die Werte werden durch **PROPVARIANT** s dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c8eab-132">Names are represented by **PROPERTYKEY** s and values are represented by **PROPVARIANT** s.</span></span> <br/> <span data-ttu-id="c8eab-133">Die API verwendet diese Schnittstelle zum Festlegen und Abrufen einzelner Werte und Werte Sätze.</span><span class="sxs-lookup"><span data-stu-id="c8eab-133">The API uses this interface for setting and retrieving both single values and sets of values.</span></span> <span data-ttu-id="c8eab-134">Diese Schnittstelle kann durch Aufrufen von **CoCreateInstance** mit CLSID portabledevicevalues aus einer Methode abgerufen werden oder, wenn ein neues Objekt erforderlich ist \_ .</span><span class="sxs-lookup"><span data-stu-id="c8eab-134">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceValues.</span></span><br/> |
| <span data-ttu-id="c8eab-135">[Iportabledevicekeycollection](/previous-versions//ms739549(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8eab-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span></span> | <span data-ttu-id="c8eab-136">Diese Schnittstelle enthält eine Auflistung von **PropertyKey** s.</span><span class="sxs-lookup"><span data-stu-id="c8eab-136">This interface contains a collection of **PROPERTYKEY** s.</span></span> <span data-ttu-id="c8eab-137">Diese Schlüsselstellen Eigenschaftsnamen dar, die von **iportabletovicevalues** gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="c8eab-137">These keys represent property names that can be stored by **IPortableDeviceValues**.</span></span> <span data-ttu-id="c8eab-138">Die API verwendet dieses Sammlungsobjekt zum Festlegen und Abrufen von einzelnen Eigenschaftsnamen und Sätzen von Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="c8eab-138">The API uses this collection object for setting and retrieving both single property names and sets of property names.</span></span><br/> <span data-ttu-id="c8eab-139">Diese Schnittstelle kann aus einer-Methode abgerufen werden, oder, wenn ein neues-Objekt erforderlich ist, durch Aufrufen von **CoCreateInstance** mit der CLSID \_ portabledevicekeycollection.</span><span class="sxs-lookup"><span data-stu-id="c8eab-139">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceKeyCollection.</span></span> <br/>    |



 

 

