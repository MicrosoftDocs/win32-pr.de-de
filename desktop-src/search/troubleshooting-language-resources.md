---
description: Dieses Thema enthält bewährte Methoden und Vorschläge für die Überprüfung und Problembehandlung Ihrer iwordbreaker-und istemmer-Implementierungen.
ms.assetid: b0e199b9-8d81-4445-92f7-de9b8a00a9cb
title: Problembehandlung bei Sprachressourcen und bewährten Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63a0a8acda3fff1627b37f41c2d81a67b37d66a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750320"
---
# <a name="troubleshooting-language-resources-and-best-practices"></a>Problembehandlung bei Sprachressourcen und bewährten Methoden

Dieses Thema enthält bewährte Methoden und Vorschläge für die Überprüfung und Problembehandlung Ihrer [**iwordbreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) -und [**istemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) -Implementierungen.

Dieses Thema ist wie folgt organisiert:

-   [Bewährte Methoden](#best-practices)
-   [Testen der Wort Stamm Erkennung](#testing-stemmer-consistency)
-   [Testen auf ungültige Eingaben in der Wort Stamm Erkennung](#testing-for-invalid-input-in-the-stemmer)
-   [Testen der Konsistenz von Wörter Trennungen](#testing-word-breaker-consistency)
-   [Testen auf ungültige Eingaben in der Wörter Trennung](#testing-for-invalid-input-in-the-word-breaker)

### <a name="best-practices"></a>Bewährte Methoden

-   Stellen Sie sicher, dass das Threading Modell für Sprachressourcen in der Registrierung auf "beides" festgelegt ist.
-   Platzieren Sie nach Möglichkeit Sprach Daten in einer Ressource anstelle einer separaten Datei in der dll. Dies erleichtert die Installation und Sicherheit der dll. Außerdem führt das Einfügen von Sprach Daten in eine Ressource zu einer verbesserten Leistung für diese Sprachressourcen Komponente.
-   Minimieren Sie die Systemressourcen, die von Sprachressourcen Komponenten verwendet werden. Wenn z. b. für jede Instanz eines Sprachressourcen Objekts Schreib geschützter Zugriff auf ein Lexikon erforderlich ist, sollten Sie das Lexikon in allen Instanzen freigeben.
-   Verwenden Sie ggf. die neutrale Wörter Trennung, um Text zu verarbeiten, der nicht in der Sprache oder dem Gebiets Schema für die Implementierung der Wörter Trennung liegt. Dadurch wird sichergestellt, dass der Text in allen Sprachen konsistent verarbeitet wird.
-   Überprüfen Sie alle Rückgabecodes, und geben Sie Sie von Funktionen wie [**istemmer:: generatewordforms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) und [**iwordbreaker:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext)zurück. Wenn die Indizierung fehlschlägt, ist es wichtig, den Fehler zu übergeben, damit der Benutzer darüber informiert wird, welche Dokumente indiziert wurden.

### <a name="testing-stemmer-consistency"></a>Testen der Wort Stamm Erkennung

Es wird empfohlen, dass Sie die Leistung einer [**istemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) -Implementierung unter den folgenden Bedingungen auf Konsistenz überwachen:

-   Die Wort Stamm Erkennung führt konsistent über mehrere Aufrufe von [**istemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init)hinweg durch. Die Wort Stamm Erkennung wird mit denselben Parametern wie in der vorherigen Initialisierung erneut initialisiert, ohne die Parameter freizugeben.
-   Beim gleichen Test Korpus und bei Wiederholungen derselben Abfrage erzeugt [**istemmer:: generatewordforms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) die identische Ausgabe und führt identische Aufrufe der Methoden des [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekts aus.

### <a name="testing-for-invalid-input-in-the-stemmer"></a>Testen auf ungültige Eingaben in der Wort Stamm Erkennung

Es wird empfohlen, zu überwachen, wie die [**istemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) -Methoden alle Fehler im Zusammenhang mit ungültigen Parametern behandeln. Außerdem wird empfohlen, dass Sie sicherstellen, dass die Wort Stamm Erkennung keine unbehandelten Ausnahmen ausgelöst hat. Die Wort Stamm Erkennung sollte die folgenden Fehler behandeln:

-   Wenden Sie sich an [**istemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init) , bei dem *pflicense* auf **null** festgelegt ist. Init schlägt fehl und führt nicht zu einer Zugriffsverletzung.
-   Aufrufen von [**istemmer:: getlicensetouse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) , bei dem der *ppwcslicense* -Parameter auf **null** festgelegt ist. **Istemmer:: getlicensetouse** führt nicht zu einer Zugriffsverletzung.
-   Aufrufen von [**istemmer:: generatewordforms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) , bei dem der *pwcinbuf* -Parameter auf **null** festgelegt ist. **Istemmer:: generatewordforms** schlägt fehl (gibt E \_ fehl) und führt nicht zu einer Zugriffsverletzung.
-   Aufrufen von [**istemmer:: generatewordforms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) , bei dem der *CWC* -Parameter gleich 0 ist. **Istemmer:: generatewordforms** gibt erfolgreich zurück (gibt S \_ OK zurück) und führt nicht zu einer Zugriffsverletzung.
-   Aufrufen von [**istemmer:: generatewordforms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) , bei dem der *pwcinbuf* -Parameter auf **null** festgelegt ist und der *CWC* -Parameter gleich 0 ist. **Istemmer:: generatewordforms** schlägt fehl (gibt E \_ fehl) und führt nicht zu einer Zugriffsverletzung.

### <a name="testing-word-breaker-consistency"></a>Testen der Konsistenz von Wörter Trennungen

Es wird empfohlen, dass Sie sicherstellen, dass die [**iwordbreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) -Implementierung unter den folgenden Bedingungen einheitlich funktioniert:

-   Die Wörter Trennung führt konsistent über mehrere Aufrufe der [**iwordbreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) -Methode hinweg durch. Die Wörter Trennung wird erneut mit denselben Parametern wie in der vorherigen Initialisierung initialisiert, ohne die Parameter freizugeben.
-   Beim gleichen Test Korpus und bei Wiederholungen derselben Abfrage erzeugt die [**iwordbreak:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode die identische Ausgabe und führt identische Aufrufe der Methoden der [**iwordsink**](iwordsink.md) -und [**iphrasesink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) -Objekte aus.

### <a name="testing-for-invalid-input-in-the-word-breaker"></a>Testen auf ungültige Eingaben in der Wörter Trennung

Es wird empfohlen, sicherzustellen, dass die [**iwordbreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) -Methoden alle Fehler im Zusammenhang mit ungültigen Parametern behandeln. Außerdem wird empfohlen, dass Sie sicherstellen, dass die Wörter Trennungs Methoden keine unbehandelten Ausnahmen ausgelöst werden. Die Wörter Trennung sollte die folgenden Funktionen ausführen und die folgenden Fehler behandeln:

-   Der Aufrufe von [**iwordbreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) muss entweder Sprache \_ E \_ Database \_ nicht \_ gefunden oder S \_ OK zurückgeben.
-   Der Aufruf von [**iwordbreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) initialisiert den *pflicense* -Parameter erfolgreich auf **false** und ruft [**istemmer:: getlicensetouse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) auf und führt nicht zu einer Zugriffsverletzung.
-   Die Wörter Trennung liest nicht über das Ende des *awcbuffer* -Parameters in der [**iwordbreaker:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode hinaus.
-   [**Iwordbreaker:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) wird aufgerufen, wobei *pwcinbuf* auf **null** festgelegt ist. **Iwordbreaker:: breaktext** schlägt fehl (gibt E \_ fehl) und führt nicht zu einer Zugriffsverletzung.
-   Aufrufen von [**iwordbreaker:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) , bei dem der *CWC* -Parameter gleich 0 (null) ist. **Iwordbreaker:: breaktext** wird erfolgreich zurückgegeben (gibt S \_ OK zurück) und führt nicht zu einer Zugriffsverletzung.
-   Aufrufen der [**iwordbreak:: breaktext**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode, bei der der *pwcinbuf* -Parameter auf NULL festgelegt ist und der *CWC* -Parameter gleich 0 ( **null** ) ist. **Iwordbreaker:: breaktext** schlägt fehl (gibt E \_ fehl) und führt nicht zu einer Zugriffsverletzung.
-   Während der Indexerstellung generierte Ausdrücke enthalten die gleiche Anzahl von Wörtern.
-   Ausdrücke werden während der Indexerstellung durch aufeinander folgende Aufrufe der [**iwordformsink::P utword**](iwordsink-putword.md) -Methode und der [**iwordformsink::P utaltword**](iwordsink-putaltword.md) -Methode generiert. Die Wörter Trennung verwendet nur das [**iphrasesink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) -Objekt während der Abfragezeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Grundlegendes zu Sprachressourcen Komponenten](understanding-language-resource-components.md)
</dt> <dt>

[Implementieren von Wörter Trennungen und Wort Stamm Erkennungen](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Überlegungen zu linguistischer und Unicode](linguistic-and-unicode-considerations.md)
</dt> </dl>

 

 
