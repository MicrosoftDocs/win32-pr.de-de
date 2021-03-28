---
description: Eine Anwendung erklärt einen Teil eines Fensters für ungültig und legt den Aktualisierungs Bereich mithilfe der invalidaterierten-oder InvalidateRgn-Funktion fest.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Ungültig machen und Validieren der Update Region
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978577"
---
# <a name="invalidating-and-validating-the-update-region"></a>Ungültig machen und Validieren der Update Region

Eine Anwendung erklärt einen Teil eines Fensters für ungültig und legt den Aktualisierungs Bereich mithilfe der [**invalidaterierten**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) -oder [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) -Funktion fest. Diese Funktionen fügen das angegebene Rechteck oder den Bereich (in den Client Koordinaten) dem Aktualisierungs Bereich hinzu, wobei das Rechteck oder die Region mit dem Element kombiniert wird, das vom System oder der Anwendung zuvor der Aktualisierungs Region hinzugefügt wurde.

Die [**invalidatup**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) -und [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) -Funktionen generieren keine [**WM- \_ Paint**](wm-paint.md) -Meldungen. Stattdessen sammelt das System die Änderungen, die von diesen Funktionen vorgenommen werden, und ihre eigenen Änderungen, während ein Fenster andere Nachrichten in der Nachrichten Warteschlange verarbeitet. Durch das Anhäufen von Änderungen werden alle Änderungen gleichzeitig von einem Fenster verarbeitet, statt Bits und Teile einzeln zu aktualisieren.

Die Funktionen [**validatenund**](/windows/desktop/api/Winuser/nf-winuser-validaterect) [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validieren einen Teil des Fensters, indem ein angegebenes Rechteck oder eine angegebene Region aus dem Aktualisierungs Bereich entfernt wird. Diese Funktionen werden in der Regel verwendet, wenn das Fenster vor dem Empfang der [**WM \_ Paint**](wm-paint.md) -Meldung einen bestimmten Teil des Bildschirms in der Update Region aktualisiert hat.

 

 



