---
description: Die Klassen RealTimeStylus, GestureRecognizer und DynamicRenderer werden als COM-Wrapper implementiert und sind nur in verwaltetem Code verfügbar.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Implementierungs Hinweise für die StylusInput-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958765"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a><span data-ttu-id="09304-103">Implementierungs Hinweise für die StylusInput-APIs</span><span class="sxs-lookup"><span data-stu-id="09304-103">Implementation Notes for the StylusInput APIs</span></span>

<span data-ttu-id="09304-104">Die Klassen [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))und [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) werden als COM-Wrapper implementiert und sind nur in verwaltetem Code verfügbar.</span><span class="sxs-lookup"><span data-stu-id="09304-104">The [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), and [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) classes are implemented as COM wrappers and are available only in managed code.</span></span>

<span data-ttu-id="09304-105">Wenn das [**RealTimeStylus**](realtimestylus-class.md)-, [GestureRecognizer](/previous-versions/ms575185(v=vs.100))-oder [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) -Objekt als Plug-in zu einem **RealTimeStylus** -Objekt hinzugefügt wird, interagieren die zugrunde liegenden COM-Objekte auf com-Ebene.</span><span class="sxs-lookup"><span data-stu-id="09304-105">When the [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), or [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object is added as a plug-in to a **RealTimeStylus** object, the underlying COM objects interact on the COM level.</span></span> <span data-ttu-id="09304-106">Daher wird das direkte Aufrufen der Methoden der [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) -Schnittstelle oder der [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) -Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09304-106">Therefore, directly calling the methods of the [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) or [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) interfaces are not supported.</span></span> <span data-ttu-id="09304-107">Das Hinzufügen des **RealTimeStylus**-, GestureRecognizer-oder DynamicRenderer-Objekts zum **RealTimeStylus** -Objekt ist die einzige Möglichkeit, auf diese Funktionen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="09304-107">Adding the **RealTimeStylus**, GestureRecognizer, or DynamicRenderer object to the **RealTimeStylus** object is the only way to access these features.</span></span>

 

 
