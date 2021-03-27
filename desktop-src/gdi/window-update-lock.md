---
description: Eine Fenster Update Sperre ist eine vorübergehende Unterbrechung der Zeichnung in einem Fenster.
ms.assetid: 92b1ba04-ff79-4a37-9633-99412cdafe95
title: Fenster Update Sperre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4897915020134387947c7a77009c4bdbd63cfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215643"
---
# <a name="window-update-lock"></a>Fenster Update Sperre

Eine *Fenster Update Sperre* ist eine vorübergehende Unterbrechung der Zeichnung in einem Fenster. Das System verwendet die Sperre, um zu verhindern, dass andere Fenster über das Überwachungs Rechteck zeichnen, wenn der Benutzer ein Fenster verschiebt oder Größe verschiebt. Anwendungen können die Sperre verwenden, um das Zeichnen zu verhindern, wenn Sie ähnliche Verschiebungs-oder Größen Anpassungs Vorgänge mit ihren eigenen Fenstern ausführen.

Eine Anwendung verwendet die [**lockwindowupdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) -Funktion, um eine Fenster Update Sperre festzulegen oder zu löschen. dabei wird das Fenster angegeben, das gesperrt werden soll. Die Sperre gilt für das angegebene Fenster und alle untergeordneten Fenster. Wenn die Sperre festgelegt wird, geben die Funktionen [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) und [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) einen Anzeigegeräte Kontext mit einem sichtbaren Bereich zurück, der leer ist. Wenn dies der so ist, kann die Anwendung weiterhin im Fenster gezeichnet werden, aber die gesamte Ausgabe wird abgeschnitten. Die Sperre bleibt bestehen, bis Sie von der Anwendung gelöscht wird, indem **lockwindowupdate** aufgerufen und **null** für das Fenster angegeben wird. Obwohl **lockwindowupdate** erzwingt, dass der sichtbare Bereich eines Fensters leer ist, macht die Funktion das angegebene Fenster nicht unsichtbar und löscht das sichtbare WS- \_ Stilbit nicht.

Nachdem die Sperre festgelegt wurde, kann die Anwendung die [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) -Funktion mit dem Wert DCX \_ lockwindowupdate verwenden, um einen Anzeigegeräte Kontext abzurufen, der über dem gesperrten Fenster gezeichnet werden soll. Dadurch kann die Anwendung bei der Verarbeitung von Tastatur-oder Maus Meldungen ein Verfolgungs Rechteck zeichnen. Diese Methode wird vom System verwendet, wenn der Benutzer die Größe von Fenstern verschiebt. **Getdcex** Ruft den Anzeigegeräte Kontext aus dem Kontext Cache des Anzeige Geräts ab, sodass die Anwendung den Gerätekontext nach dem Zeichnen so bald wie möglich freigeben muss.

Während eine Fenster Update Sperre festgelegt wird, erstellt das System ein akkumuliertes Begrenzungs Rechteck für jedes gesperrte Fenster. Wenn die Sperre deaktiviert ist, verwendet das System dieses umschließende Rechteck, um den Aktualisierungs Bereich für das Fenster und seine untergeordneten Fenster festzulegen, und erzwingt eine endgültige WM-Zeichnungs Nachricht. [**\_**](wm-paint.md) Wenn das akkumulierte umgebende Rechteck leer ist (d. h., wenn keine Zeichnung aufgetreten ist, während die Sperre festgelegt wurde), wird der Update Bereich nicht festgelegt.

 

 



