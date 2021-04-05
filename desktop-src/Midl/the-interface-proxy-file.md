---
title: Die Schnittstellen Proxy Datei
description: Bei der Schnittstellen Proxy Datei (U \_ p. c) handelt es sich um eine c-Datei, die Routinen enthält, die den Client-Stub-und Server-Stub-Dateien einer COM-Schnittstelle (com) entsprechen.
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- Mittel l und com-Mittel l, Schnittstellen, Proxy Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947903"
---
# <a name="the-interface-proxy-file"></a>Die Schnittstellen Proxy Datei

Bei der Schnittstellen Proxy Datei (U \_ p. c) handelt es sich um eine c-Datei, die Routinen enthält, die den Client-Stub-und Server-Stub-Dateien einer COM-Schnittstelle (com) entsprechen. Diese Datei enthält Implementierungen der Ersatz Zeichenroutinen für Client und Server im Inline Modus des Compilers, oder äquivalente Daten und thunna in den interpretierten Modi sowie andere geeignete com-Daten, wie z. b. die Proxy-und stubvtables.

Die Schnittstellen Proxy Datei enthält die unterstützenden Routinen und Daten nur für Methoden der Schnittstellen, die in der aktuellen IDL-Datei definiert sind. Um dieses Verhalten zu verdeutlichen, wird in diesem Abschnitt ein erweitertes Beispiel verwendet. Beim Kompilieren einer IDL-Datei mit einer Schnittstelle, wie z. b. ifaceb, die von ifacea erbt, werden mit ifaceb verknüpfte zusätzliche Daten und Routinen in der aktuellen Proxy Datei generiert, während die ifacea-bezogenen Erweiterungs Daten und-Routinen in dem von der IDL-Datei generierten Proxy gefunden werden Der Compiler generiert alle Daten, die erforderlich sind, um die Ersatz Zeichen der Basisschnittstelle zu identifizieren, und um Sie bei Bedarf zu delegieren, um die durch die ifaceb-Schnittstelle verwendeten ifacea-Methoden zu unterstützen.

Für jede Methode in einer Schnittstelle in der aktuellen IDL-Datei enthält die Proxy Datei die folgenden zwei Ersatzmethoden, wenn Sie im gemischten Modus ([/OS](-os.md)) kompiliert werden, und äquivalente interpreterdaten, wenn Sie im Interpretermodus ([/Oi](-oi.md)) kompiliert werden.

-   Das Client seitige Ersatz Zeichen, z. b. der ifaceb- \_ Methoden \_ Proxy in diesem Beispiel.

    Dieses Client seitige Ersatz Zeichen ist der virtuelle Einstiegspunkt, an den der Client, z. b. ifaceb:: Method, sendet. Sie marshallt die Eingabeargumente in ein ausführbares Formular, überträgt die gemarshallten Argumente zusammen mit Informationen, die die-Schnittstelle und den-Vorgang identifizieren, und entmarshallt den Rückgabewert und alle Ausgabe Argumente, wenn der aufgerufene Vorgang zurückgegeben wird.

-   Das serverseitige Ersatz Zeichen, z. b. ifaceb- \_ \_ Methodenstub.

    Dieses serverseitige Ersatz Zeichen ist der virtuelle Einstiegspunkt, an den die zugrunde liegende Laufzeit zum Emulieren des Clients auf dem Server gesendet wird. Die Eingabeargumente werden zum Replizieren der Client Daten, zum Aufrufen der Implementierung der Schnittstelle des Servers und zum anschließenden marshunzieren und übertragen des Rückgabewerts sowie der Ausgabe Argumente an die Clientseite zurückgegeben.

Der Standardname für eine aus einer Datei erstellte Proxy Datei. idl ist die Datei \_ p. c. verwenden Sie den [**/Proxy**](-proxy.md) -Compilerschalter, um den Standardnamen der Schnittstellen Proxy Datei zu überschreiben. Die Schalter [**/env**](-env.md) und [**/out**](-out.md) beeinflussen diese Datei.

 

 




