---
description: Das System verwaltet einen Cache von Anzeigegeräte Kontexten, die für gemeinsame, übergeordnete und Fenster Geräte Kontexte verwendet werden.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Gerätekontext Cache anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994086"
---
# <a name="display-device-context-cache"></a><span data-ttu-id="35aee-103">Gerätekontext Cache anzeigen</span><span class="sxs-lookup"><span data-stu-id="35aee-103">Display Device Context Cache</span></span>

<span data-ttu-id="35aee-104">Das System verwaltet einen Cache von Anzeigegeräte Kontexten, die für gemeinsame, übergeordnete und Fenster Geräte Kontexte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35aee-104">The system maintains a cache of display device contexts that it uses for common, parent, and window device contexts.</span></span> <span data-ttu-id="35aee-105">Das System ruft einen Gerätekontext aus dem Cache ab, wenn eine Anwendung die [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) -oder [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) -Funktion aufruft. Das System gibt den DC an den Cache zurück, wenn die Anwendung anschließend die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -oder [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="35aee-105">The system retrieves a device context from the cache whenever an application calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function; the system returns the DC to the cache when the application subsequently calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) or [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) function.</span></span>

<span data-ttu-id="35aee-106">Es gibt keinen vordefinierten Grenzwert für die Anzahl von Geräte Kontexten, die ein Cache enthalten kann. Das System erstellt einen neuen Anzeigegeräte Kontext für den Cache, wenn keiner verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="35aee-106">There is no predetermined limit on the amount of device contexts that a cache can hold; the system creates a new display device context for the cache if none is available.</span></span> <span data-ttu-id="35aee-107">In diesem Zusammenhang kann eine Anwendung mehr als fünf aktive Geräte Kontexte gleichzeitig aus dem Cache haben.</span><span class="sxs-lookup"><span data-stu-id="35aee-107">Given this, an application can have more than five active device contexts from the cache at a time.</span></span> <span data-ttu-id="35aee-108">Die Anwendung muss diese Geräte Kontexte jedoch nach der Verwendung weiterhin freigeben.</span><span class="sxs-lookup"><span data-stu-id="35aee-108">However, the application must continue to release these device contexts after use.</span></span> <span data-ttu-id="35aee-109">Da neue Anzeigegeräte Kontexte für den Cache im Heap Bereich der Anwendung zugeordnet werden, verbraucht die Freigabe der Geräte Kontexte schließlich den gesamten verfügbaren Heap Speicher.</span><span class="sxs-lookup"><span data-stu-id="35aee-109">Because new display device contexts for the cache are allocated in the application's heap space, failing to release the device contexts eventually consumes all available heap space.</span></span> <span data-ttu-id="35aee-110">Das System gibt diesen Fehler an, indem ein Fehler zurückgegeben wird, wenn der Speicherplatz für den neuen Gerätekontext nicht belegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="35aee-110">The system indicates this failure by returning an error when it cannot allocate space for the new device context.</span></span> <span data-ttu-id="35aee-111">Andere Funktionen, die nicht mit dem Cache verknüpft sind, können auch Fehler zurückgeben</span><span class="sxs-lookup"><span data-stu-id="35aee-111">Other functions unrelated to the cache may also return errors.</span></span>

 

 



