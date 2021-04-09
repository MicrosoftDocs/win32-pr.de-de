---
description: Wenn eine Windows-Abbild Erfassungs Schnittstelle (WIA) in mehr als einem Thread innerhalb eines einzelnen Prozesses verwendet wird, muss eine Anwendung Marshalling für diese Schnittstelle bereitstellen.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Verwenden mehrerer Threads in einer WIA-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129389"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Verwenden mehrerer Threads in einer WIA-Anwendung

Wenn eine Windows-Abbild Erfassungs Schnittstelle (WIA) in mehr als einem Thread innerhalb eines einzelnen Prozesses verwendet wird, muss eine Anwendung Marshalling für diese Schnittstelle bereitstellen. Wenn ein Thread einen Schnittstellen Zeiger erstellt, können Sie diesen Zeiger nicht in einem anderen Thread verwenden, ohne Marshalling zu müssen.

Wenn ein Thread in einer Anwendung z. b. einen Zeiger auf die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle erhält, kann ein separater Thread diesen Schnittstellen Zeiger nicht ohne Marshalling verwenden.

Ein gängiges Verfahren, mit dem dieses Marshalling erreicht wird, ist die Verwendung der globalen Schnittstellen Tabelle. Die globale Schnittstellen Tabelle ist eine Tabelle, die in einem einzelnen Prozess über alle Threads hinweg verwaltet wird. Alle Threads, die innerhalb des Prozesses ausgeführt werden, können Schnittstellen abrufen, die für die globale Schnittstellen Tabelle registriert sind. Diese Methode vermeidet das Erstellen von Streams zum Übergeben von Schnittstellen zwischen Threads.

Informationen zur Verwendung der globalen Schnittstellen Tabelle finden Sie unter [iglobalinterfaketable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Auch wenn Sie nicht beabsichtigen, mehrere Threads in einer WIA-Anwendung zu verwenden, müssen Sie davon ausgehen, dass alle Datenübertragungs-oder Geräte Ereignis Rückruf Funktionen in separaten Threads ausgeführt werden.

 

 
