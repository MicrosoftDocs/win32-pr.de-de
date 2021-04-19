---
description: Das Telefon Objekt ist die Entität, die das eigentliche Telefongerät und alle seine Steuerelemente darstellt.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Telefon Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359186"
---
# <a name="phone-object-interfaces"></a><span data-ttu-id="b7ce8-103">Telefon Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b7ce8-103">Phone Object Interfaces</span></span>

<span data-ttu-id="b7ce8-104">Das Telefon Objekt ist die Entität, die das eigentliche Telefongerät und alle seine Steuerelemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-104">The Phone object is the entity that represents the actual phone device and all of its controls.</span></span>

<span data-ttu-id="b7ce8-105">Die [**itphoneevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) -und [**ienumphone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) -Schnittstellen werden nicht direkt auf dem Phone-Objekt verfügbar gemacht, sind jedoch eng damit verknüpft und werden hier als praktische Referenz aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-105">The [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) and [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) interfaces are not directly exposed on the Phone object, but are tightly related to it and are listed here for convenience of reference.</span></span>



| <span data-ttu-id="b7ce8-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b7ce8-106">Interface</span></span>                                                  | <span data-ttu-id="b7ce8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7ce8-107">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7ce8-108">**ITPhone**</span><span class="sxs-lookup"><span data-stu-id="b7ce8-108">**ITPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | <span data-ttu-id="b7ce8-109">Ermöglicht den Zugriff auf das Telefongerät auf einer Ebene, die mit der von TAPI 2 verfügbaren vergleichbar ist. *x* -C-API.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-109">Allows access to the phone device at a level comparable to that available with the TAPI 2.*x* C API.</span></span>                                      |
| [<span data-ttu-id="b7ce8-110">**Itautomatedphonecontrol**</span><span class="sxs-lookup"><span data-stu-id="b7ce8-110">**ITAutomatedPhoneControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | <span data-ttu-id="b7ce8-111">Stellt Methoden für die automatisierte Steuerung der Töne und Ringe eines Telefons sowie für die automatisierte Anruf Behandlung auf der Grundlage des Status eines Telefonanschlusses bereit.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-111">Provides methods for automated control of a phone's tones and rings, and for automated call handling based on a phone's hookswitch state.</span></span> |
| [<span data-ttu-id="b7ce8-112">**Itphoneevent**</span><span class="sxs-lookup"><span data-stu-id="b7ce8-112">**ITPhoneEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | <span data-ttu-id="b7ce8-113">Ruft die Beschreibung der Telefon Ereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-113">Retrieves the description of phone events.</span></span>                                                                                                |
| [<span data-ttu-id="b7ce8-114">**Ienumphone**</span><span class="sxs-lookup"><span data-stu-id="b7ce8-114">**IEnumPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | <span data-ttu-id="b7ce8-115">Listet das [**itphone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)auf.</span><span class="sxs-lookup"><span data-stu-id="b7ce8-115">Enumerates [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span></span>                                                                                                    |



 

 

 



