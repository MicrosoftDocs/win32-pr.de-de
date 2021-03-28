---
description: Es gibt im wesentlichen keine Einschränkungen, wie eine Autorun-Start Anwendung geschrieben werden kann.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Implementieren von Autorun-Start Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959693"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Implementieren von Autorun-Start Anwendungen

Es gibt im wesentlichen keine Einschränkungen, wie eine Autorun-Start Anwendung geschrieben werden kann. Sie können die Start Anwendung so implementieren, dass Sie alle erforderlichen Schritte zum Installieren, deinstallieren, konfigurieren oder Ausführen der Anwendung ausführen können. Die folgenden Tipps bieten jedoch einige Richtlinien für die Implementierung einer effektiven Autorun-Start Anwendung.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Stellen Sie sicher, dass Benutzer Feedback so schnell wie möglich erhalten, nachdem Sie eine Autorun-CD in das Laufwerk eingefügt haben. Start Anwendungen sollten kleine Programme sein, die schnell geladen werden. Sie sollten die Anwendung eindeutig identifizieren und eine einfache Möglichkeit bereitstellen, um den Vorgang abzubrechen.

### <a name="step-2"></a>Schritt 2:

Überprüfen Sie, ob das Programm bereits installiert ist. Wenn dies nicht der Fall ist, ist der nächste Schritt wahrscheinlich die Setup Prozedur. Die Start Anwendung kann die Zeit nutzen, die der Benutzer beim Lesen des Dialog Felds verbringt, indem er einen anderen Thread startet, um mit dem Laden des Setup Codes zu beginnen. Wenn der Benutzer auf **OK** klickt, wird das Setup Programm bereits teilweise, wenn es nicht vollständig geladen ist, angezeigt. Mit diesem Ansatz wird die Wahrnehmung des Benutzers für das Laden Ihrer Anwendung erheblich reduziert.

> [!Note]  
> Der erste Teil der Start Anwendung zeigt Benutzern in der Regel eine Benutzeroberfläche, z. b. ein Dialogfeld, in der Sie gefragt werden, wie Sie fortfahren möchten.

 

### <a name="step-3"></a>Schritt 3:

Starten Sie einen weiteren Thread, um das Laden des Anwendungs Codes zu beginnen, um die Wartezeit für den Benutzer zu verkürzen. Wenn die Anwendung bereits installiert wurde, wurde der Datenträger vom Benutzer wahrscheinlich zum Ausführen der Anwendung eingefügt.

### <a name="step-4"></a>Schritt 4:

Verwenden Sie die folgenden Hinweise, um die Festplattennutzung zu minimieren:

-   Halten Sie die Anzahl der Dateien, die sich auf der Festplatte befinden müssen, auf einen minimalen Wert fest. Sie sollten auf Dateien beschränkt werden, die für die Ausführung des Programms von entscheidender Bedeutung sind, oder die einen unzulässigen Zeitaufwand für das Lesen von Medien benötigen.
-   In vielen Fällen ist es nicht erforderlich, nicht erforderliche Dateien auf der Festplatte zu installieren, bietet jedoch möglicherweise Vorteile, z. b. eine bessere Leistung. Geben Sie dem Benutzer die Möglichkeit, zu entscheiden, wie Sie den Kompromiss zwischen den Kosten und den Vorteilen der Festplatten Speicherung treffen möchten.
-   Bietet eine Möglichkeit, alle Komponenten zu deinstallieren, die auf der Festplatte platziert wurden.
-   Wenn Ihre Anwendung Daten zwischenspeichert, können Sie dem Benutzer eine gewisse Kontrolle über die Anwendung einräumen. Schließen Sie Optionen in die Start Anwendung ein, z. b. das Festlegen einer Beschränkung für die maximale Menge an zwischengespeicherten Daten, die auf der Festplatte gespeichert werden, oder das Verwerfen von zwischengespeicherten Daten durch die Anwendung, wenn diese beendet wird.

### <a name="step-5"></a>Schritt 5:

Deaktivieren Sie bei Bedarf Autorun. Autorun kann entweder Programm gesteuert oder vollständig mit der Registrierung unterdrückt werden, auch wenn ein Medium über eine Autorun. inf-Datei verfügt. Weitere Informationen finden Sie unter [aktivieren und Deaktivieren von Autorun](autoplay-reg.md) .

 

 



