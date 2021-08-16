---
title: Befehlsverknüpfungen und Variationen
description: Befehlsverknüpfungen und Variationen
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a3379b5eb6dced9ccebb3e04e76be87fdca7ea5af341b647cb0205888c283
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807920"
---
# <a name="command-shortcuts-and-variations"></a>Befehlsverknüpfungen und Variationen

Sie können mehrere Tastenkombinationen verwenden, wenn Sie mit MCI-Befehlen arbeiten. Mit diesen Tastenkombinationen können Sie einen einzelnen Bezeichner verwenden, um auf alle Geräte zu verweisen, die Ihre Anwendung geöffnet hat, oder um ein Gerät zu öffnen, ohne explizit einen offenen [**Befehl**](open.md) [**(MCI \_ OPEN)**](mci-open.md)ausstellen zu müssen.

Sie können "all" (MCI ALL DEVICE ID) als Gerätebezeichner für jeden Befehl angeben, \_ der keine Informationen zurück \_ \_ gibt. Wenn Sie "all" angeben, sendet MCI den Befehl sequenziell an alle Geräte, die von der aktuellen Anwendung geöffnet werden.

Der Befehl [**"alle**](close.md) schließen" schließt z. B. alle geöffneten Geräte, und der Befehl [**"alle**](play.md) wieder geben" beginnt mit der Wiedergabe aller Geräte, die von der Anwendung geöffnet werden. Da MCI die Befehle sequenziell an die MCI-Geräte sendet, gibt es ein Intervall zwischen dem Empfang des Befehls durch das erste und das letzte Gerät.

Die Verwendung von "all" ist eine praktische Möglichkeit, einen Befehl an alle Ihre Geräte zu übertragen, aber Sie sollten sich nicht darauf verlassen, dass gerätesynchron sind. Die Zeitsteuerung zwischen Nachrichten kann variieren.

Wenn Sie einen Befehl ausführen und ein gerät angeben, das nicht geöffnet ist, versucht MCI, das Gerät zu öffnen, bevor der Befehl implementieren wird. Die folgenden Regeln gelten für das automatische Öffnen von Geräten:

-   Das Feature zum automatischen Öffnen funktioniert nur mit der Befehlszeichenfolgenschnittstelle.
-   Das Feature zum automatischen Öffnen schlägt bei Befehlen fehl, die für benutzerdefinierte Gerätetreiber spezifisch sind.
-   Automatisch geöffnete Geräte reagieren nicht auf Befehle, die "all" als Gerätenamen verwenden.
-   Das Feature zum automatischen Öffnen lässt nicht zu, dass Ihre Anwendung das Flag "type" ankn.) Ohne den Gerätenamen bestimmt MCI den Gerätenamen aus den Einträgen in der Registrierung. Um ein bestimmtes Gerät zu verwenden, können Sie den Gerätenamen mit dem Dateinamen kombinieren, indem Sie das Ausrufezeichen verwenden, wie im Referenzmaterial für den [**open-Befehl**](open.md) beschrieben.

Wenn eine Anwendung das Feature zum automatischen Öffnen verwendet, um ein Gerät zu öffnen, sollte die Anwendung den Rückgabewert jedes nachfolgenden geöffneten Befehls überprüfen, um sicherzustellen, dass das Gerät noch geöffnet ist. MCI schließt auch automatisch alle Geräte, die automatisch geöffnet werden. MCI schließt ein Gerät in der Regel in den folgenden Situationen:

-   Der Befehl ist abgeschlossen.
-   Sie bricht den Befehl ab.
-   Sie fordern eine Benachrichtigung in einem nachfolgenden Befehl an.
-   MCI erkennt einen Fehler.

 

 




