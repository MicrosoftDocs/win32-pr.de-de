---
description: Der Hintergrund des Fensters ist die Farbe oder das Muster, mit dem der Client Bereich ausgefüllt wird, bevor ein Fenster mit dem Zeichnen beginnt.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Fenster Hintergrund
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d567b0bdc38866cd9332ff8ed399bfb23f53c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864320"
---
# <a name="window-background"></a>Fenster Hintergrund

Der Hintergrund des Fensters ist die Farbe oder das Muster, mit dem der Client Bereich ausgefüllt wird, bevor ein Fenster mit dem Zeichnen beginnt. Der Hintergrund des Fensters ist das, was auf dem Bildschirm vor dem Verschieben des Fensters war, das Löschen vorhandener Bilder und das verhindern, dass die neue Ausgabe der Anwendung mit nicht verknüpften Informationen gemischt wird.

Das System zeichnet den Hintergrund für ein Fenster oder gibt dem Fenster die Gelegenheit, dies zu tun, indem er eine [**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung sendet, wenn die Anwendung [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)aufruft. Wenn eine Anwendung die Nachricht nicht verarbeitet, sondern an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, löscht das System den Hintergrund, indem er mit dem Muster in dem Hintergrund Pinsel aufgefüllt wird, der von der-Klasse des Fensters angegeben wird. Wenn der Pinsel nicht gültig ist oder die Klasse keinen Hintergrund Pinsel hat, legt das System den **ferase** -Member in der [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur fest, die **BeginPaint** zurückgibt, aber es wird keine andere Aktion ausgeführt. Die Anwendung kann dann ggf. den Fenster Hintergrund zeichnen.

Wenn Sie [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md)verarbeitet, sollte die Anwendung den *wParam* -Parameter der Meldung verwenden, um den Hintergrund zu zeichnen. Dieser Parameter enthält ein Handle für den Anzeigegeräte Kontext für das Fenster. Nachdem der Hintergrund gezeichnet wurde, sollte die Anwendung einen Wert ungleich 0 (null) zurückgeben. Dadurch wird sichergestellt, dass [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) den **ferase** -Member der [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur nicht fälschlicherweise auf einen Wert ungleich 0 (null) festlegt (gibt an, dass der Hintergrund gelöscht werden soll), wenn die Anwendung die nachfolgende WM-Zeichnungs Nachricht verarbeitet. [**\_**](wm-paint.md)

Eine Anwendung kann einen klassenhintergrund Pinsel definieren, indem dem **hbrbackground** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur ein Pinsel handle oder ein System Farbwert zugewiesen wird, wenn die Klasse mit der [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion registriert wird. Zum Erstellen eines Pinsel Zieh Punkts kann die [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) [**-oder die**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) -Funktion verwendet werden. Ein System Farbwert kann einer der Werte sein, die für die Funktion " [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) " definiert sind. (Der Wert muss um eins angehoben werden, bevor er dem Element zugewiesen wird.)

Eine Anwendung kann die [**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Nachricht verarbeiten, obwohl ein klassenhintergrund Pinsel definiert ist. Dies ist typisch für Anwendungen, die es dem Benutzer ermöglichen, die Hintergrundfarbe oder das Muster des Fensters für ein angegebenes Fenster zu ändern, ohne dass sich dies auf andere Fenster der Klasse auswirkt In solchen Fällen darf die Anwendung die Nachricht nicht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.

Es ist nicht erforderlich, dass eine Anwendung Pinsel ausrichten kann, da das System den Pinsel mit dem Fenster Ursprung als Bezugspunkt zeichnet. Dadurch kann der Benutzer das Fenster verschieben, ohne dass sich dies auf die Ausrichtung von Muster Pinseln auswirkt.

 

 
