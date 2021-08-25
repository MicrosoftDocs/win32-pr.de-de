---
title: Verwenden von Registerkartensteuerelementen
description: Dieses Thema enthält zwei Beispiele, in denen Registerkartensteuerelemente verwendet werden.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a373a1d7d1fc44da851480841aab04bf364b27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465268"
---
# <a name="using-tab-controls"></a>Verwenden von Registerkartensteuerelementen

Dieses Thema enthält zwei Beispiele, in denen Registerkartensteuerelemente verwendet werden. Das erste Beispiel veranschaulicht die Verwendung eines Registerkartensteuerelements, um zwischen mehreren Textseiten im Hauptfenster einer Anwendung zu wechseln. Im zweiten Beispiel wird veranschaulicht, wie ein Registerkartensteuerelement verwendet wird, um zwischen mehreren Seiten von Steuerelementen in einem Dialogfeld zu wechseln.

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="create-a-tab-control-in-the-main-window.md">Erstellen eines Registerkartensteuerelements im Hauptfenster</a><br /> | Im Beispiel in diesem Abschnitt wird veranschaulicht, wie Sie ein Registerkartensteuerelement erstellen und im Clientbereich des Hauptfensters der Anwendung anzeigen. Die Anwendung zeigt ein drittes Fenster (ein statisches Steuerelement) im Anzeigebereich des Registerkartensteuerelements an. Das übergeordnete Fenster positioniert und größent das Registerkartensteuerelement und das statische Steuerelement, wenn es die <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> Meldung verarbeitet. <br /> In diesem Beispiel gibt es sieben Registerkarten, eine für jeden Tag der Woche. Wenn der Benutzer eine Registerkarte auswählt, zeigt die Anwendung den Namen des entsprechenden Tages im statischen Steuerelement an. <br /> | 
| <a href="create-a-tabbed-dialog-box.md">Erstellen eines Dialogfelds im Registerkartenbett</a><br /> | Das Beispiel in diesem Abschnitt veranschaulicht das Erstellen eines Dialogfelds, das Registerkarten verwendet, um mehrere Seiten von Steuerelementen bereitzustellen. Das Hauptdialogfeld ist ein modales Dialogfeld. Jede Seite von Steuerelementen wird durch eine Dialogfeldvorlage definiert, die über den <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> Stil verfügt. Wenn eine Registerkarte ausgewählt ist, wird ein modusloses Dialogfeld für die eingehende Seite erstellt, und das Dialogfeld für die ausgehende Seite wird zerstört. <br /><blockquote>[!Note]<br />In vielen Fällen können Sie dialogfelder mit mehreren Seiten mithilfe von Eigenschaftenblättern einfacher implementieren. Weitere Informationen zu Eigenschaftenblättern finden Sie unter <a href="property-sheets.md">Informationen zu Eigenschaftenblättern.</a></blockquote><br /> Die Vorlage für das Hauptdialogfeld definiert einfach zwei Schaltflächensteuerelemente. Beim Verarbeiten der <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> Meldung erstellt die Dialogfeldprozedur ein Registerkartensteuerelement und lädt die Vorlagenressourcen des Dialogfelds für jedes untergeordnete Dialogfeld. <br /> | 




 

