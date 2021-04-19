---
description: Der System Event Notification Service (Sens) definiert die Sens-Co-Klasse als Teil der Sens-Typbibliothek.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Sens-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356971"
---
# <a name="sens-object"></a><span data-ttu-id="e6467-103">Sens-Objekt</span><span class="sxs-lookup"><span data-stu-id="e6467-103">SENS Object</span></span>

<span data-ttu-id="e6467-104">Der System Event Notification Service (Sens) definiert die Sens-Co-Klasse als Teil der Sens-Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="e6467-104">The System Event Notification Service (SENS) defines the SENS coclass as part of the SENS type library.</span></span>

## <a name="implementation"></a><span data-ttu-id="e6467-105">Implementierung</span><span class="sxs-lookup"><span data-stu-id="e6467-105">Implementation</span></span>

<span data-ttu-id="e6467-106">Die Sens-Objekt Implementierung wird vom Betriebssystem bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e6467-106">The SENS object implementation is provided by the operating system.</span></span>

## <a name="creationaccess-functions"></a><span data-ttu-id="e6467-107">Erstellungs-/Zugriffs Funktionen</span><span class="sxs-lookup"><span data-stu-id="e6467-107">Creation/Access Functions</span></span>



| <span data-ttu-id="e6467-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="e6467-108">Function</span></span>                                      | <span data-ttu-id="e6467-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6467-109">Description</span></span>                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="e6467-110">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="e6467-110">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | <span data-ttu-id="e6467-111">Erstellt eine Instanz des Sens-Objekts unter Verwendung der zugehörigen CLSID.</span><span class="sxs-lookup"><span data-stu-id="e6467-111">Creates an instance of the SENS object using its CLSID.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="e6467-112">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e6467-112">Interfaces</span></span>



| <span data-ttu-id="e6467-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e6467-113">Interface</span></span>                            | <span data-ttu-id="e6467-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6467-114">Description</span></span>                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6467-115">**Isensnetwork**</span><span class="sxs-lookup"><span data-stu-id="e6467-115">**IsensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | <span data-ttu-id="e6467-116">Standard.</span><span class="sxs-lookup"><span data-stu-id="e6467-116">Default.</span></span> <span data-ttu-id="e6467-117">Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert</span><span class="sxs-lookup"><span data-stu-id="e6467-117">Outgoing interface implemented by sink object in subscriber application.</span></span>                   |
| [<span data-ttu-id="e6467-118">**Isennow**</span><span class="sxs-lookup"><span data-stu-id="e6467-118">**IsensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | <span data-ttu-id="e6467-119">Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert</span><span class="sxs-lookup"><span data-stu-id="e6467-119">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="e6467-120">**Isenslogon**</span><span class="sxs-lookup"><span data-stu-id="e6467-120">**IsensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | <span data-ttu-id="e6467-121">Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert</span><span class="sxs-lookup"><span data-stu-id="e6467-121">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="e6467-122">**IsensLogon2**</span><span class="sxs-lookup"><span data-stu-id="e6467-122">**IsensLogon2**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | <span data-ttu-id="e6467-123">Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert</span><span class="sxs-lookup"><span data-stu-id="e6467-123">Outgoing interface implemented by sink object in subscriber application.</span></span> <span data-ttu-id="e6467-124">Verfügbar in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e6467-124">Available with Windows XP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e6467-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6467-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6467-126">**Isenslogon**</span><span class="sxs-lookup"><span data-stu-id="e6467-126">**ISensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[<span data-ttu-id="e6467-127">**Isensnetwork**</span><span class="sxs-lookup"><span data-stu-id="e6467-127">**ISensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[<span data-ttu-id="e6467-128">**Isennow**</span><span class="sxs-lookup"><span data-stu-id="e6467-128">**ISensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[<span data-ttu-id="e6467-129">Informationen zum System Ereignis Benachrichtigungsdienst</span><span class="sxs-lookup"><span data-stu-id="e6467-129">About System Event Notification Service</span></span>](about-system-event-notification-service.md)
</dt> </dl>

 

 
