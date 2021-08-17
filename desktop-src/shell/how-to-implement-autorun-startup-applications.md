---
description: Es gibt im Wesentlichen keine Einschränkungen für das Schreiben einer AutoRun-Startanwendung.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Implementieren von AutoRun-Startanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5c31f57c8a972ee6b138b55c09c432d9cf8fc1a9f33644c92c95229c344893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350770"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Implementieren von AutoRun-Startanwendungen

Es gibt im Wesentlichen keine Einschränkungen für das Schreiben einer AutoRun-Startanwendung. Sie können die Startanwendung implementieren, um alles zu tun, was Sie zum Installieren, Deinstallieren, Konfigurieren oder Ausführen Ihrer Anwendung für erforderlich halten. Die folgenden Tipps enthalten jedoch einige Richtlinien für die Implementierung einer effektiven AutoRun-Startanwendung.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Stellen Sie sicher, dass Benutzer so bald wie möglich Feedback erhalten, nachdem sie eine AutoRun-Festplatte in das Laufwerk eingefügt haben. Startanwendungen sollten kleine Programme sein, die schnell geladen werden. Sie sollten die Anwendung eindeutig identifizieren und eine einfache Möglichkeit bieten, den Vorgang abzubrechen.

### <a name="step-2"></a>Schritt 2:

Überprüfen Sie, ob das Programm bereits installiert ist. Falls nicht, ist der nächste Schritt wahrscheinlich das Setupverfahren. Die Startanwendung kann die Zeit nutzen, die der Benutzer beim Lesen des Dialogfelds aufwendet, indem ein anderer Thread gestartet wird, um mit dem Laden des Setupcodes zu beginnen. Wenn der Benutzer auf **OK** klickt, ist Ihr Setupprogramm bereits teilweise vorhanden, wenn es nicht vollständig geladen ist. Dieser Ansatz reduziert die Wahrnehmung des Benutzers in Bezug auf die Zeit, die zum Laden Ihrer Anwendung benötigt wird.

> [!Note]  
> In der Regel zeigt der erste Teil der Startanwendung Benutzern eine Benutzeroberfläche an, z. B. ein Dialogfeld, in dem sie gefragt werden, wie sie fortfahren möchten.

 

### <a name="step-3"></a>Schritt 3:

Starten Sie einen anderen Thread, um mit dem Laden von Anwendungscode zu beginnen, um die Wartezeit für den Benutzer zu verkürzen. Wenn die Anwendung bereits installiert wurde, hat der Benutzer wahrscheinlich den Datenträger eingefügt, um die Anwendung auszuführen.

### <a name="step-4"></a>Schritt 4:

Verwenden Sie die folgenden Hinweise, um die Festplattennutzung zu minimieren:

-   Halten Sie die Anzahl der Dateien, die sich auf der Festplatte befinden müssen, auf ein Minimum. Sie sollten auf Dateien beschränkt werden, die für die Ausführung des Programms von entscheidender Bedeutung sind oder das lesen von den Medien eine inakzeptable menge zeitaufwendige Zeit in Anspruch nehmen würde.
-   In vielen Fällen ist die Installation von nicht grundlegenden Dateien auf der Festplatte nicht erforderlich, kann aber Vorteile wie eine höhere Leistung bieten. Geben Sie dem Benutzer die Möglichkeit, zu entscheiden, wie der Ausgleich zwischen den Kosten und Vorteilen des Festplattenspeichers entstehen soll.
-   Stellen Sie eine Möglichkeit bereit, alle Komponenten zu deinstallieren, die auf der Festplatte platziert wurden.
-   Wenn Ihre Anwendung Daten zwischenspeichert, geben Sie dem Benutzer die Kontrolle darüber. Schließen Sie Optionen in die Startanwendung ein, z. B. das Festlegen eines Grenzwerts für die maximale Menge zwischengespeicherter Daten, die auf der Festplatte gespeichert werden, oder das Verwerfen zwischengespeicherter Daten durch die Anwendung beim Beenden.

### <a name="step-5"></a>Schritt 5:

Deaktivieren Sie Autorun bei Bedarf. AutoRun kann programmgesteuert oder vollständig mit der Registrierung unterdrückt werden, auch wenn ein Medium über eine Autorun.inf-Datei verfügt. Weitere Informationen finden Sie unter [Aktivieren und Deaktivieren von AutoRun.](autoplay-reg.md)

 

 



