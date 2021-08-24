---
description: Das System ändert die Größe eines Fensters, wenn der Benutzer Fenstermenübefehle wie Größe und Maximieren auswählt oder wenn die Anwendung Funktionen aufruft, z. B. die SetWindowPos-Funktion.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Geänderte Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efd6f71d1657c0d01b3df9101fc15fa35f54ecfc01b1588b696cd9110dad317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602720"
---
# <a name="resized-windows"></a>Geänderte Windows

Das System ändert die Größe eines Fensters, wenn der Benutzer Fenstermenübefehle wie Größe und Maximieren auswählt oder wenn die Anwendung Funktionen aufruft, z. B. die [**SetWindowPos-Funktion.**](/windows/win32/api/winuser/nf-winuser-setwindowpos) Wenn sich die Größe eines Fensters ändert, geht das System davon aus, dass der Inhalt des zuvor verfügbar gemachten Teils des Fensters nicht betroffen ist und nicht neu gezeichnet werden muss. Das System macht nur den neu verfügbar gemachten Teil des Fensters ungültig, was Zeit spart, wenn die letztliche [**WM \_ PAINT-Nachricht**](wm-paint.md) von der Anwendung verarbeitet wird. In diesem Fall wird **WM \_ PAINT** nicht generiert, wenn die Größe des Fensters reduziert wird.

Bei einigen Fenstern macht jede Änderung der Fenstergröße den Inhalt ungültig. Beispielsweise muss eine Uhranwendung, die das Gesicht der Uhr an das Fenster anpasst, neu gezeichnet werden, wenn sich die Größe des Fensters ändert. Um zu erzwingen, dass das System den gesamten Clientbereich des Fensters ungültig macht, wenn eine vertikale, horizontale oder vertikale und horizontale Änderung vorgenommen wird, muss eine Anwendung beim Registrieren der Fensterklasse den CS \_ VREDRAW- oder CS HREDRAW-Stil oder beides \_ angeben. Jedes Fenster, das zu einer Fensterklasse mit diesen Stilen gehört, wird jedes Mal ungültig, wenn der Benutzer oder die Anwendung die Größe des Fensters ändert.

 

 
