---
description: Einige Objekte unterstützen jeweils nur ein handle.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Einschränkungen behandeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217983"
---
# <a name="handle-limitations"></a><span data-ttu-id="0fe56-103">Einschränkungen behandeln</span><span class="sxs-lookup"><span data-stu-id="0fe56-103">Handle Limitations</span></span>

<span data-ttu-id="0fe56-104">Einige Objekte unterstützen jeweils nur ein handle.</span><span class="sxs-lookup"><span data-stu-id="0fe56-104">Some objects support only one handle at a time.</span></span> <span data-ttu-id="0fe56-105">Das System stellt das Handle bereit, wenn eine Anwendung das Objekt erstellt, und macht das Handle ungültig, wenn die Anwendung das Objekt zerstört.</span><span class="sxs-lookup"><span data-stu-id="0fe56-105">The system provides the handle when an application creates the object and invalidates the handle when the application destroys the object.</span></span> <span data-ttu-id="0fe56-106">Andere Objekte unterstützen mehrere Handles für ein einzelnes Objekt.</span><span class="sxs-lookup"><span data-stu-id="0fe56-106">Other objects support multiple handles to a single object.</span></span> <span data-ttu-id="0fe56-107">Das Betriebssystem entfernt das-Objekt automatisch aus dem Arbeitsspeicher, nachdem das letzte Handle für das-Objekt geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0fe56-107">The operating system automatically removes the object from memory after the last handle to the object is closed.</span></span>

<span data-ttu-id="0fe56-108">Die Gesamtanzahl der geöffneten Handles im System wird nur durch die verfügbare Menge an Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0fe56-108">The total number of open handles in the system is limited only by the amount of memory available.</span></span> <span data-ttu-id="0fe56-109">Einige Objekttypen unterstützen eine begrenzte Anzahl von Handles pro Sitzung oder pro Prozess.</span><span class="sxs-lookup"><span data-stu-id="0fe56-109">Some object types support a limited number of handles per session or per process.</span></span>

 

 



