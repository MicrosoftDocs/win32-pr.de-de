---
description: Wenn eine Windows Image Acquisition-Schnittstelle (WIA) in mehreren Threads innerhalb eines einzelnen Prozesses verwendet wird, muss eine Anwendung Marshalling für diese Schnittstelle bereitstellen.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Verwenden mehrerer Threads in einer WIA-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707adbfe6cd24152209e318bed73a0b6d7fee54b6cfa1e8fbcfecac67e272082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208006"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Verwenden mehrerer Threads in einer WIA-Anwendung

Wenn eine Windows Image Acquisition-Schnittstelle (WIA) in mehreren Threads innerhalb eines einzelnen Prozesses verwendet wird, muss eine Anwendung Marshalling für diese Schnittstelle bereitstellen. Wenn ein Thread einen Schnittstellenzeiger erstellt, können Sie diesen Zeiger nicht ohne Marshalling in einem anderen Thread verwenden.

Wenn beispielsweise ein Thread in einer Anwendung einen Zeiger auf die [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) erhält, kann ein separater Thread diesen Schnittstellenzeiger nicht ohne Marshalling verwenden.

Ein gängiges Verfahren für dieses Marshalling ist die Verwendung der globalen Schnittstellentabelle. Die globale Schnittstellentabelle ist eine Tabelle, die über alle Threads innerhalb eines einzelnen Prozesses hinweg verwaltet wird. Alle Threads, die innerhalb des Prozesses ausgeführt werden, können Schnittstellen abrufen, die in der globalen Schnittstellentabelle registriert sind. Diese Technik vermeidet die Notwendigkeit, Streams zum Übergeben von Schnittstellen zwischen Threads zu erstellen.

Informationen zur Verwendung der globalen Schnittstellentabelle finden Sie unter [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Auch wenn Sie nicht beabsichtigen, mehrere Threads in einer WIA-Anwendung zu verwenden, müssen Sie davon ausgehen, dass alle Datenübertragungs- oder Geräteereignisrückruffunktionen in separaten Threads ausgeführt werden.

 

 
