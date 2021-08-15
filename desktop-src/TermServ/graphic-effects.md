---
title: Grafische Effekte
description: Eine Liste der Features, die deaktiviert werden sollten, wenn sie als Remotesitzung in einer Remotedesktopdienste werden.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cad01bb7b61c471ba81f382d1fc4031b8c44dcef63a78c5a0cc17641b5e457e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059438"
---
# <a name="graphic-effects"></a>Grafische Effekte

Ein Remotedesktopdienste-Server nutzt das Netzwerk, um alle Ein- und Ausgaben an seine Clientterminals zu übertragen. Folglich können Anwendungen, die grafische Effekte übermäßig nutzen, die Leistung für alle Remotedesktopdienste-Clients beeinträchtigen, indem sie das Netzwerk verlangsamen. Darüber hinaus kann die langsamere Übertragungsgeschwindigkeit über ein Netzwerk dazu führen, dass diese Sondereffekte weniger ansprechend erscheinen als in einer lokalen Videoumgebung.

Insbesondere sollten Anwendungen die Verwendung der folgenden Features deaktivieren oder minimieren, wenn sie in einer Remotedesktopdienste-Umgebung als Remotesitzung ausgeführt werden:

-   Begrüßungsbildschirme– grafische Produkt- oder Unternehmensinformationen, die angezeigt werden, während eine Anwendung gestartet wird. Die Übertragung eines Begrüßungsbildschirms an einen Remotedesktopverbindung-Client (RDC) verbraucht zusätzliche Netzwerkbandbreite und zwingt den Benutzer, vor dem Zugriff auf die Anwendung zu warten.
-   Animationen, die sowohl CPU-Zeit als auch Netzwerkbandbreite beanspruchen.
-   Direkte Eingabe oder Ausgabe auf dem Bildschirm. Wenn Sie Bits vom Bildschirm lesen müssen, verwalten Sie eine separate Kopie des Videopuffers aus dem Bildschirm. Wenn Sie eine ausführliche Bildschirmausgabe erstellen müssen, z. B. mehrere Bilder überlagern, um einen endgültigen zusammengesetzten Bildschirm zu erhalten, funktioniert dies in einem Off-Screen-Puffer, und senden Sie die Ergebnisse dann an den tatsächlichen Videopuffer.

Weitere Informationen zum Erkennen von Remotesitzungen finden Sie unter [Detecting the Remotedesktopdienste Environment](detecting-the-terminal-services-environment.md).

Verwenden Sie nach Möglichkeit die Microsoft Foundation Class-Bibliothek oder MFC. Der MFC verfügt über eine lange Liste von bewährten Klassen zum Ausführen einer Vielzahl von Aufgaben. Die meisten dieser Klassen funktionieren gut in Remotedesktopdienste Umgebung – in der Regel viel besser als neu entwickelten Lösungen. Ein gutes Beispiel ist die -Klasse, die kontextorientierten Hilfetext bietet– Hilfetext, der auf dem Bildschirm angezeigt wird, wenn der Mauszeiger auf eine Schaltfläche oder ein Menüelement zeigt. Wenn eine Anwendung die MFC-Implementierung verwendet, um dieses Feature zur Verfügung zu stellen, funktioniert sie auf dem Desktopsystem einigermaßen gut. Wenn die Anwendung dieses Feature jedoch mithilfe von Dialogfeldern oder einem alternativen Ansatz implementiert, funktioniert das Endergebnis in einer Remotedesktopdienste möglicherweise nicht so gut.

 

 




