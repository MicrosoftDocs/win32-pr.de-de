---
description: Die Header Datei "winternl. h" stellt Prototypen interner Windows-APIs zur Verfügung. Es gibt keine zugeordnete Import Bibliothek, sodass Entwickler Lauf Zeit dynamische Verknüpfungen verwenden müssen, um die in dieser Header Datei beschriebenen Funktionen aufzurufen.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Aufrufen interner APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958330"
---
# <a name="calling-internal-apis"></a>Aufrufen interner APIs

Die Header Datei "winternl. h" stellt Prototypen interner Windows-APIs zur Verfügung. Es gibt keine zugeordnete Import Bibliothek, sodass Entwickler Lauf Zeit dynamische Verknüpfungen verwenden müssen, um die in dieser Header Datei beschriebenen Funktionen aufzurufen.

Die Funktionen und Strukturen in "winternl. h" sind für das Betriebssystem intern und können von einer Version von Windows zum nächsten und möglicherweise sogar zwischen Service Packs für die einzelnen Releases geändert werden. Um die Kompatibilität Ihrer Anwendung aufrechtzuerhalten, sollten Sie stattdessen die entsprechenden öffentlichen Funktionen verwenden. Weitere Informationen finden Sie in der Header Datei, winternl. h, und in der Dokumentation zu den einzelnen Funktionen.

Wenn Sie diese Funktionen verwenden, können Sie über die dynamische Lauf Zeit Verknüpfung mithilfe von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)darauf zugreifen. Dadurch erhält Ihr Code die Möglichkeit, ordnungsgemäß zu reagieren, wenn die Funktion geändert oder aus dem Betriebssystem entfernt wurde. Signatur Änderungen sind jedoch möglicherweise nicht erkennbar.

 

 
