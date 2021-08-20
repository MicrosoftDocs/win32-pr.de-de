---
description: Die Klassen RealTimeStylus, GestureRecognizer und DynamicRenderer werden als COM-Wrapper implementiert und sind nur in verwaltetem Code verfügbar.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Implementierungshinweise für die StylusInput-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c106dd0e940cf6fd9e54235af43901d14e511ead5e8908be56b464c483335b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032378"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Implementierungshinweise für die StylusInput-APIs

Die [**Klassen RealTimeStylus,**](realtimestylus-class.md) [GestureRecognizer](/previous-versions/ms575185(v=vs.100))und [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) werden als COM-Wrapper implementiert und sind nur in verwaltetem Code verfügbar.

Wenn [**das RealTimeStylus-,**](realtimestylus-class.md) [GestureRecognizer-](/previous-versions/ms575185(v=vs.100))oder [DynamicRenderer-Objekt](/previous-versions/ms575176(v=vs.100)) als Plug-In zu einem **RealTimeStylus-Objekt** hinzugefügt wird, interagieren die zugrunde liegenden COM-Objekte auf COM-Ebene. Daher wird das direkte Aufrufen der Methoden der [Schnittstellen IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) oder [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) nicht unterstützt. Das Hinzufügen **des RealTimeStylus-,** GestureRecognizer- oder DynamicRenderer-Objekts zum **RealTimeStylus-Objekt** ist die einzige Möglichkeit, auf diese Features zu zugreifen.

 

 
