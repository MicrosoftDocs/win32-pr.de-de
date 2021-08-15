---
description: Die Headerdatei "Skinl.h" macht Prototypen interner Windows-APIs verfügbar. Es gibt keine zugeordnete Importbibliothek, sodass Entwickler dynamische Verknüpfungen zur Laufzeit verwenden müssen, um die in dieser Headerdatei beschriebenen Funktionen auf aufruft.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Aufrufen interner APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c613b4f650709eb9764eff133c018be62768c58212b4dc7130149ce8b5173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956129"
---
# <a name="calling-internal-apis"></a>Aufrufen interner APIs

Die Headerdatei "Skinl.h" macht Prototypen interner Windows-APIs verfügbar. Es gibt keine zugeordnete Importbibliothek, sodass Entwickler dynamische Verknüpfungen zur Laufzeit verwenden müssen, um die in dieser Headerdatei beschriebenen Funktionen auf aufruft.

Die Funktionen und Strukturen in "Skinl.h" sind für das Betriebssystem intern und können von einer Version von Windows zur nächsten und möglicherweise sogar zwischen Service Packs für jedes Release geändert werden. Um die Kompatibilität Ihrer Anwendung zu gewährleisten, sollten Sie stattdessen die entsprechenden öffentlichen Funktionen verwenden. Weitere Informationen finden Sie in der Headerdatei "Skinl.h" und in der Dokumentation zu den einzelnen Funktionen.

Wenn Sie diese Funktionen verwenden, können Sie über dynamische Verknüpfungen zur Laufzeit mit [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress darauf zugreifen.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde. Signaturänderungen sind jedoch möglicherweise nicht erkennbar.

 

 
