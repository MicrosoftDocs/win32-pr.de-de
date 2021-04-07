---
title: Abfragen von zusätzlichen Audiogeräten
description: Abfragen von zusätzlichen Audiogeräten
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- Wellenform-Audiodaten, Abfragen von hilfaudiogeräten
- zusätzliches Audiomaterial, Abfragen von Geräten
- hilfsaudioschnittstelle
- hilfaudiogeräte, Abfragen
- Abfragen von zusätzlichen Audiogeräten
- zusätzliches Audiomaterial, Schnittstelle
- zusätzliches Audiogerät, Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d7de949c304cdd6941be87277f2eef1711ada24
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038871"
---
# <a name="querying-auxiliary-audio-devices"></a><span data-ttu-id="78534-110">Abfragen von zusätzlichen Audiogeräten</span><span class="sxs-lookup"><span data-stu-id="78534-110">Querying Auxiliary Audio Devices</span></span>

<span data-ttu-id="78534-111">Nicht alle Multimediasysteme verfügen über zusätzliche Audiounterstützung.</span><span class="sxs-lookup"><span data-stu-id="78534-111">Not all multimedia systems have auxiliary audio support.</span></span> <span data-ttu-id="78534-112">Mit der Funktion "-Funktion" können [**Sie die Anzahl**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) der in einem System vorhandenen steuerbaren Hilfssysteme ermitteln.</span><span class="sxs-lookup"><span data-stu-id="78534-112">You can use the [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) function to determine the number of controllable auxiliary devices present in a system.</span></span>

<span data-ttu-id="78534-113">Verwenden [**Sie die Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) "-Funktion", um Informationen zu einem bestimmten zusätzlichen Audiogerät zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="78534-113">To get information about a particular auxiliary audio device, use the [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) function.</span></span> <span data-ttu-id="78534-114">Diese Funktion füllt eine " [**auxcaps**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) "-Struktur mit Informationen zu den Funktionen eines bestimmten Geräts.</span><span class="sxs-lookup"><span data-stu-id="78534-114">This function fills an [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="78534-115">Diese Informationen umfassen die Hersteller-und Produkt-IDs, einen Produktnamen für das Gerät und die Gerätetreiber-Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="78534-115">This information includes the manufacturer and product identifiers, a product name for the device, and the device-driver version number.</span></span>

 

 