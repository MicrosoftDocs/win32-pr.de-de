---
description: Mithilfe eines Fenster Geräte Kontexts kann eine Anwendung an beliebiger Stelle in einem Fenster gezeichnet werden, einschließlich des nicht-Client Bereichs.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Fenster Geräte Kontexte anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75abed6177771d9beff56ad5e7dec1f8e0a704c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979368"
---
# <a name="window-display-device-contexts"></a>Fenster Geräte Kontexte anzeigen

Mithilfe eines *Fenster Geräte Kontexts* kann eine Anwendung an beliebiger Stelle in einem Fenster gezeichnet werden, einschließlich des nicht-Client Bereichs. Fenster Geräte Kontexte werden in der Regel von Anwendungen verwendet, die die Nachrichten von [**WM \_ ncpaint**](wm-ncpaint.md) und [**WM \_ ncaktivierungs**](../winmsg/wm-ncactivate.md) für Windows mit benutzerdefinierten nicht-Client-Bereichen verarbeiten. Die Verwendung eines Fenster Geräte Kontexts wird für keinen anderen Zweck empfohlen.

Eine Anwendung kann einen Fenster Gerätekontext abrufen, indem Sie die [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) -Funktion oder die [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion mit der angegebenen Option DCX- \_ Fenster verwendet. Mit der-Funktion wird ein Fenster Gerätekontext aus dem Kontext Cache des Anzeige Geräts abgerufen. Ein Fenster, in dem ein Fenster Gerätekontext verwendet wird, muss nach dem Zeichnen mithilfe der [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion so bald wie möglich freigegeben werden. Fenster Geräte Kontexte werden immer aus dem Cache entfernt. die \_ Klassen Stile CS owndc und CS \_ classdc wirken sich nicht auf den Gerätekontext aus.

Wenn eine Anwendung einen Fenster Gerätekontext abruft, legt das System den Ursprung des Geräts auf die linke obere Ecke des Fensters anstelle der oberen linken Ecke des Client Bereichs fest. Außerdem wird der Clippingbereich so festgelegt, dass das gesamte Fenster (nicht nur der Client Bereich) enthalten ist. Das System legt die aktuellen Attributwerte eines Fenster-Geräte Kontexts auf dieselben Standardwerte fest wie ein gemeinsamer Gerätekontext. Eine Anwendung kann die Attributwerte ändern, aber das System behält keine Änderungen bei, wenn der Gerätekontext freigegeben wird.

 

 
