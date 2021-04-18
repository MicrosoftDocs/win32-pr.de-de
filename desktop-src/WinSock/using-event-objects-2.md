---
description: Bei Windows Sockets-Ereignis Objekten handelt es sich um einfache Konstrukte, die erstellt, geschlossen, festgelegt, gelöscht, gewartet und abgerufen werden können.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Verwenden von Ereignis Objekten (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343675"
---
# <a name="using-event-objects-windows-sockets-2"></a>Verwenden von Ereignis Objekten (Windows Sockets 2)

Bei Windows Sockets-Ereignis Objekten handelt es sich um einfache Konstrukte, die erstellt, geschlossen, festgelegt, gelöscht, gewartet und abgerufen werden können. Das akzeptierte Modell besteht darin, dass Clients ein Ereignis Objekt erstellen und das Handle als Parameter (oder als Komponente einer Parameter Struktur) in Funktionen wie [**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) und [**wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))bereitstellen. Wenn die nominierte Bedingung aufgetreten ist, verwendet der Dienstanbieter das Handle, um das Ereignis Objekt durch Aufrufen von [**wpusetevent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent)festzulegen. In der Zwischenzeit kann der Winsock-SPI-Client entweder blockieren und warten oder Abfragen, bis das Ereignis Objekt festgelegt wird (signalisiert). Der Client kann das Ereignis Objekt anschließend löschen oder zurücksetzen und wieder verwenden.

 

 
