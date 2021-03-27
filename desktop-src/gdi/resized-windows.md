---
description: Das System ändert die Größe eines Fensters, wenn der Benutzermenü Befehle im Menü (z. b. Größe und Maximierung) auswählt, oder wenn die Anwendung Funktionen aufruft, wie z. b. die SetWindowPos-Funktion.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Fenstergröße geändert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863627"
---
# <a name="resized-windows"></a><span data-ttu-id="746f6-103">Fenstergröße geändert</span><span class="sxs-lookup"><span data-stu-id="746f6-103">Resized Windows</span></span>

<span data-ttu-id="746f6-104">Das System ändert die Größe eines Fensters, wenn der Benutzermenü Befehle im Menü (z. b. Größe und Maximierung) auswählt, oder wenn die Anwendung Funktionen aufruft, wie z. b. die [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="746f6-104">The system changes the size of a window when the user chooses window menu commands, such as Size and Maximize, or when the application calls functions, such as the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function.</span></span> <span data-ttu-id="746f6-105">Wenn die Größe eines Fensters geändert wird, geht das System davon aus, dass der Inhalt des zuvor verfügbar gemachten Teils des Fensters nicht beeinträchtigt wird und nicht neu gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="746f6-105">When a window changes size, the system assumes that the contents of the previously exposed portion of the window are not affected and need not be redrawn.</span></span> <span data-ttu-id="746f6-106">Das System macht nur den neu verfügbar gemachten Teil des Fensters ungültig, was Zeit spart, wenn die [**endgültige \_ WM**](wm-paint.md) -Zeichnungs Nachricht von der Anwendung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="746f6-106">The system invalidates only the newly exposed portion of the window, which saves time when the eventual [**WM\_PAINT**](wm-paint.md) message is processed by the application.</span></span> <span data-ttu-id="746f6-107">In diesem Fall wird **WM \_ Paint** nicht generiert, wenn die Größe des Fensters reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="746f6-107">In this case, **WM\_PAINT** is not generated when the size of the window is reduced.</span></span>

<span data-ttu-id="746f6-108">Bei einigen Fenstern wird der Inhalt durch jede Änderung der Fenstergröße ungültig.</span><span class="sxs-lookup"><span data-stu-id="746f6-108">For some windows, any change to the size of the window invalidates the contents.</span></span> <span data-ttu-id="746f6-109">Beispielsweise muss eine Clock-Anwendung, die das Gesicht der Uhr anpasst, damit Sie in das Fenster passt, die Uhr neu zeichnen, wenn die Größe des Fensters geändert wird.</span><span class="sxs-lookup"><span data-stu-id="746f6-109">For example, a clock application that adapts the face of the clock to fit neatly within its window must redraw the clock whenever the window changes size.</span></span> <span data-ttu-id="746f6-110">Um zu erzwingen, dass das System den gesamten Client Bereich des Fensters für ungültig erklärt, wenn eine vertikale, horizontale oder vertikale und horizontale Änderung vorgenommen wird, muss eine Anwendung \_ beim Registrieren der Fenster Klasse die CS-Klasse "vredraw" oder "CS \_ hredraw" oder beides angeben.</span><span class="sxs-lookup"><span data-stu-id="746f6-110">To force the system to invalidate the entire client area of the window when a vertical, horizontal, or both vertical and horizontal change is made, an application must specify the CS\_VREDRAW or CS\_HREDRAW style, or both, when registering the window class.</span></span> <span data-ttu-id="746f6-111">Jedes Fenster, das zu einer Fenster Klasse gehört, in der diese Stile vorhanden sind, wird jedes Mal ungültig, wenn der Benutzer oder die Anwendung die Größe des Fensters ändert.</span><span class="sxs-lookup"><span data-stu-id="746f6-111">Any window belonging to a window class having these styles is invalidated each time the user or the application changes the size of the window.</span></span>

 

 
