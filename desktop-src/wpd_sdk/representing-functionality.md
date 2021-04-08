---
description: Darstellen von Funktionen
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Darstellen von Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866504"
---
# <a name="representing-functionality"></a><span data-ttu-id="70f0d-103">Darstellen von Funktionen</span><span class="sxs-lookup"><span data-stu-id="70f0d-103">Representing Functionality</span></span>

<span data-ttu-id="70f0d-104">Funktionale Objekte sind vorhanden, um Funktions Funktionen eines Geräts zu identifizieren oder logisch zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="70f0d-104">Functional objects exist to identify or logically group feature capabilities of a device.</span></span> <span data-ttu-id="70f0d-105">Beispielsweise kann eine Anwendung sehen, dass ein Gerät SMS unterstützt, indem er nach dem SMS-Funktions Objekt sucht.</span><span class="sxs-lookup"><span data-stu-id="70f0d-105">For example, an application can see that a device supports SMS by looking for the SMS functional object.</span></span> <span data-ttu-id="70f0d-106">Ebenso kann die Anwendung sehen, dass ein Gerät über Kamerafunktionen verfügt, indem es nach dem noch funktionalen Objekt der Bild Erfassung sucht.</span><span class="sxs-lookup"><span data-stu-id="70f0d-106">Similarly, the application can see that a device has camera capabilities by looking for the Still Image Capture functional object.</span></span>

<span data-ttu-id="70f0d-107">Diese flexible Objektdarstellung ermöglicht die einfache Unterstützung von Geräten mit Funktionen mit mehreren Funktionen.</span><span class="sxs-lookup"><span data-stu-id="70f0d-107">This flexible object representation helps enable easy support for devices with multi-function capabilities.</span></span> <span data-ttu-id="70f0d-108">Treiber können einfach alle funktionalen Objekte verfügbar machen, die Ihr Gerät darstellen, was präziser als die Verwendung herkömmlicher Geräteklassen ist.</span><span class="sxs-lookup"><span data-stu-id="70f0d-108">Drivers can simply expose whatever functional objects represent their device, which is more granular than using traditional device classes.</span></span> <span data-ttu-id="70f0d-109">Die Objektdarstellung hilft auch dabei, überlappende funktionale Teile zu isolieren. einige Telefone können z. b. über zwei Kameras oder vier Storages verfügen.</span><span class="sxs-lookup"><span data-stu-id="70f0d-109">The object representation also helps isolate overlapping functional pieces; for example, some phones may have two cameras or four storages.</span></span>

<span data-ttu-id="70f0d-110">Im Betriebssystem Windows 7 erweitern Dienste funktionale Objekte durch die Bereitstellung umfangreicher Abfragen von Funktionen und eine abstrakte Gruppierung von Inhalten.</span><span class="sxs-lookup"><span data-stu-id="70f0d-110">In the Windows 7 operating system, services extend functional objects by providing rich queries of capabilities and an abstract grouping of content.</span></span> <span data-ttu-id="70f0d-111">Anwendungen können-Dienste verwenden, um Gerätefunktionen zu ermitteln und effizienter mit Inhalten zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="70f0d-111">Applications can use services to discover device capabilities and to interact with content more efficiently.</span></span> <span data-ttu-id="70f0d-112">Beispielsweise kann eine Anwendung sehen, dass ein Gerät die Funktionen zum Synchronisieren von Kontakten unterstützt, indem es nach einem Contact Service-Objekt sucht und alle Kontakte als untergeordnete Objekte des Dienst Objekts findet, ohne dass die Speicher Hierarchie rekursiv durchsucht werden muss.</span><span class="sxs-lookup"><span data-stu-id="70f0d-112">For example, an application can see that a device supports the contacts-synchronization capabilities by looking for a Contacts service object, and can find all contacts as child objects of the service object, without having to recursively search the storage hierarchy.</span></span>

<span data-ttu-id="70f0d-113">Dienste ermöglichen Anwendungen auch das ermitteln und Aufrufen von benutzerdefiniertem Verhalten auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="70f0d-113">Services also allow applications to discover and invoke custom behavior on a device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70f0d-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70f0d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70f0d-115">**Anwendungs Übersicht**</span><span class="sxs-lookup"><span data-stu-id="70f0d-115">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



