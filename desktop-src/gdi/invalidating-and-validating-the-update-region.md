---
description: Eine Anwendung macht einen Teil eines Fensters ungültig und legt den Updatebereich mithilfe der InvalidateRect- oder InvalidateRgn-Funktion fest.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Ungültig machen und Überprüfen des Updatebereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6813d88674ef0339cfd3501b561e5a7c95fa5b41f0c7f212e625f9846f5beb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944170"
---
# <a name="invalidating-and-validating-the-update-region"></a>Ungültig machen und Überprüfen des Updatebereichs

Eine Anwendung macht einen Teil eines Fensters ungültig und legt den Updatebereich mithilfe der [**InvalidateRect-**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) oder [**InvalidateRgn-Funktion**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) fest. Diese Funktionen fügen dem Aktualisierungsbereich das angegebene Rechteck oder den angegebenen Bereich (in Clientkoordinaten) hinzu, indem sie das Rechteck oder den Bereich mit allem kombinieren, was das System oder die Anwendung möglicherweise zuvor dem Updatebereich hinzugefügt hat.

Die [**Funktionen InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) und [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) generieren keine [**WM \_ PAINT-Meldungen.**](wm-paint.md) Stattdessen sammelt das System die von diesen Funktionen vorgenommenen Änderungen und seine eigenen Änderungen, während ein Fenster andere Nachrichten in seiner Nachrichtenwarteschlange verarbeitet. Indem Änderungen akkumuliert werden, verarbeitet ein Fenster alle Änderungen gleichzeitig, anstatt Bits und Teile schritt für Schritt zu aktualisieren.

Die [**Funktionen ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) und [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) überprüfen einen Teil des Fensters, indem sie ein angegebenes Rechteck oder einen angegebenen Bereich aus dem Updatebereich entfernen. Diese Funktionen werden in der Regel verwendet, wenn das Fenster einen bestimmten Teil des Bildschirms im Updatebereich aktualisiert hat, bevor die [**WM \_ PAINT-Nachricht empfangen**](wm-paint.md) wird.

 

 



