---
title: Befehls Verknüpfungen und Variationen
description: Befehls Verknüpfungen und Variationen
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712528"
---
# <a name="command-shortcuts-and-variations"></a>Befehls Verknüpfungen und Variationen

Beim Arbeiten mit MCI-Befehlen können Sie mehrere Tastenkombinationen verwenden. Mit diesen Tastenkombinationen können Sie einen einzelnen Bezeichner verwenden, um auf alle Geräte zu verweisen, die Ihre Anwendung geöffnet hat, oder um ein Gerät zu öffnen, ohne explizit einen [**geöffneten**](open.md) Befehl ([**MCI \_ Open**](mci-open.md)) auszugeben.

Sie können "All" (MCI \_ All \_ Device \_ ID) als Geräte Bezeichner für jeden Befehl angeben, der keine Informationen zurückgibt. Wenn Sie "alle" angeben, sendet MCI den Befehl sequenziell an alle Geräte, die von der aktuellen Anwendung geöffnet wurden.

Beispielsweise schließt der Befehl "alle" [**Schließen**](close.md) alle geöffneten Geräte, und der Befehl "alle" Wiedergeben beginnt [**mit der wieder**](play.md) Gabe aller Geräte, die von der Anwendung geöffnet wurden. Da MCI die Befehle sequenziell an die MCI-Geräte sendet, gibt es ein Intervall zwischen dem Zeitpunkt, an dem der erste und das letzte Gerät den Befehl erhalten.

Die Verwendung von "All" ist eine bequeme Möglichkeit, einen Befehl an alle Ihre Geräte zu übertragen, aber Sie sollten sich nicht darauf verlassen, dass Geräte synchronisiert werden. die zeitliche Steuerung zwischen Nachrichten kann variieren.

Wenn Sie einen Befehl ausgeben und ein Gerät angeben, das nicht geöffnet ist, versucht MCI, das Gerät zu öffnen, bevor der Befehl implementiert wird. Die folgenden Regeln gelten für das automatische Öffnen von Geräten:

-   Das Feature für automatisches Öffnen funktioniert nur mit der Befehls Zeichenfolgen-Schnittstelle.
-   Die Funktion für automatisches Öffnen schlägt für Befehle fehl, die für benutzerdefinierte Gerätetreiber spezifisch sind.
-   Automatisch geöffnete Geräte Antworten nicht auf Befehle, die "All" als Gerätenamen verwenden.
-   Die Funktion zum automatischen öffnen lässt die Anwendung das Flag "Type" nicht zu. Ohne den Gerätenamen bestimmt MCI den Gerätenamen aus den Einträgen in der Registrierung. Wenn Sie ein bestimmtes Gerät verwenden möchten, können Sie den Gerätenamen mit dem Dateinamen kombinieren, indem Sie das Ausrufezeichen verwenden, wie im Referenzmaterial für den Befehl " [**Öffnen**](open.md) " beschrieben.

Wenn eine Anwendung das Feature für automatisches Öffnen zum Öffnen eines Geräts verwendet, sollte die Anwendung den Rückgabewert jedes nachfolgenden geöffneten Befehls überprüfen, um sicherzustellen, dass das Gerät noch geöffnet ist. MCI schließt auch automatisch alle Geräte, die automatisch geöffnet werden. MCI schließt ein Gerät in der Regel in den folgenden Situationen:

-   Der Befehl ist abgeschlossen.
-   Sie brechen den Befehl ab.
-   Sie fordern eine Benachrichtigung in einem nachfolgenden Befehl an.
-   MCI erkennt einen Fehler.

 

 




