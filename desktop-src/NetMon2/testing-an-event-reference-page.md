---
description: Der letzte Schritt beim Erstellen einer Ereignisverweisseite (ERP) besteht darin, sie zu testen.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Testen einer Ereignisverweisseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aa9fb8697181085a9b74333dba82328e90b502e6590a764fac589efa8e6f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676635"
---
# <a name="testing-an-event-reference-page"></a>Testen einer Ereignisverweisseite

Der letzte Schritt beim Erstellen einer Ereignisverweisseite (ERP) besteht darin, sie zu testen. Sie können ein ERP testen, indem Sie die Datei in einem HTML-Browser wie Microsoft Internet Explorer anzeigen. Alternativ können Sie erp und die zugehörige Experten-DLL installieren, um sie auf den Ereignisaufruf zu testen und im Netzwerkmonitor Ereignisanzeige anzuzeigen.

## <a name="viewing-erps-that-have-no-dll"></a>Anzeigen von ERPs ohne DLL

Um das fertige ERP ohne installierte Experten-DLL anzuzeigen, öffnen Sie die Datei mit einem HTML-Viewer, der Ihre eingebetteten Quellen unterstützt. Die folgende Abbildung zeigt die ERP-Beispieldatei, die unter [Schreiben eines ERP](writing-an-event-reference-page.md) beschrieben wird, da sie mit Microsoft Internet Explorer Version 4.01 angezeigt wird.

![ERP-Beispieldatei](images/ie-erp.png)

Testen von ERPs, die über eine DLL verfügen

Nachdem die ERP-Dateien und die [**Experten-DLL**](experts.md) erstellt wurden, können Sie die vollständige Funktionalität Ihrer ERPs mit Netzwerkmonitor testen. Es wird davon ausgegangen, dass die DLL gedebuggt ist und gültige Ereignisse generieren kann.

**So testen Sie ERPs mit einer DLL**

1.  Überprüfen Sie, ob die richtige Experten-DLL im entsprechenden Verzeichnis installiert ist. Weitere Informationen finden Sie unter [Installing an Expert to Netzwerkmonitor 2.1](installing-an-expert-to-network-monitor-2-1.md).
2.  Überprüfen Sie den [richtigen Namen](naming-an-event-reference-page.md) der ERP-Datei.
3.  Überprüfen Sie den [richtigen Speicherort](installing-existing-erps-to-network-monitor-2-1.md) der ERPs im Netzwerkmonitor Verzeichnis.
4.  Testen Sie Experten-ERPs auf der Netzwerkmonitor-Benutzeroberfläche.
5.  Generieren sie ein Testereignis.
6.  Vergewissern Sie sich, dass das ERP im Netzwerkmonitor Ereignisanzeige angezeigt wird.

Weitere Informationen zum Erstellen eines ERP finden Sie unter:

-   [Erstellen von Referenzseiten für Experten- und Überwachungsereignisse](creating-expert-and-monitor-event-reference-pages.md)
-   [Schreiben einer Ereignisverweisseite](writing-an-event-reference-page.md)
-   [Benennen einer Ereignisverweisseite](naming-an-event-reference-page.md)

 

 



