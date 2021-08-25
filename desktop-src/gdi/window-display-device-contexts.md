---
description: Mit einem Fenstergerätekontext kann eine Anwendung überall in einem Fenster zeichnen, einschließlich des Nichtclientbereichs.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Fensteranzeigegerätekontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfed34646323114ffcfb7753331b1b5c305a7a0c01a475795a7918f6e5a2dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965090"
---
# <a name="window-display-device-contexts"></a>Fensteranzeigegerätekontexte

Mit *einem Fenstergerätekontext* kann eine Anwendung überall in einem Fenster zeichnen, einschließlich des Nicht-Clientbereichs. Fenstergerätekontexte werden in der Regel von Anwendungen verwendet, die die [**WM \_ NCPAINT-**](wm-ncpaint.md) und [**WM \_ NCACTIVATE-Nachrichten**](../winmsg/wm-ncactivate.md) für Fenster mit benutzerdefinierten Nichtclientbereichen verarbeiten. Die Verwendung eines Fenstergerätekontexts wird für keinen anderen Zweck empfohlen.

Eine Anwendung kann einen Fenstergerätekontext abrufen, indem sie die [**GetWindowDC-**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) oder [**GetDCEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdcex) mit der angegebenen DCX \_ WINDOW-Option verwendet. Die Funktion ruft einen Fenstergerätekontext aus dem Kontextcache des Anzeigegeräts ab. Ein Fenster, das einen Fenstergerätekontext verwendet, muss es nach dem Zeichnen mithilfe der [**ReleaseDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-releasedc) so schnell wie möglich wieder frei geben. Fenstergerätekontexte befinden sich immer aus dem Cache. Die \_ Klassenstile CS OWNDC und \_ CS CLASSDC wirken sich nicht auf den Gerätekontext aus.

Wenn eine Anwendung einen Fenstergerätekontext abruft, legt das System den Ursprung des Geräts auf die obere linke Ecke des Fensters statt auf die obere linke Ecke des Clientbereichs fest. Außerdem wird der Ausschneidebereich so definiert, dass er nicht nur den Clientbereich, sondern auch das gesamte Fenster enthält. Das System legt die aktuellen Attributwerte eines Fenstergerätekontexts auf die gleichen Standardwerte fest wie ein gemeinsamer Gerätekontext. Eine Anwendung kann die Attributwerte ändern, aber das System behält keine Änderungen bei, wenn der Gerätekontext freigegeben wird.

 

 
