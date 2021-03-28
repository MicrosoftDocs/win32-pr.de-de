---
description: In-Process-Erweiterungen werden in alle Prozesse geladen, die diese auslöst.
title: Leitfaden für die Implementierung von In-Process-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e4dc9fd0573f3f98f0ec1110079f95f56a8c42e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960861"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Leitfaden für die Implementierung von In-Process-Erweiterungen

In-Process-Erweiterungen werden in alle Prozesse geladen, die diese auslöst. Beispielsweise kann eine Shell-Namespace Erweiterung in jeden Prozess geladen werden, der entweder direkt oder indirekt auf den Shellnamespace zugreift. Der Shellnamespace wird von vielen shellvorgängen verwendet, wie z. b. der Anzeige eines allgemeinen Datei Dialogfelds, dem Start eines Dokuments durch die zugehörige Anwendung oder dem Abrufen des Symbols, das zum Darstellen einer Datei verwendet wird. Da in-Process-Erweiterungen in beliebige Prozesse geladen werden können, muss darauf geachtet werden, dass Sie sich nicht negativ auf die Host Anwendung oder andere Prozess interne Erweiterungen auswirken.

Eine Laufzeit eines bestimmten Hinweises ist die *Common Language Runtime (CLR)*, die auch als *verwalteter Code* oder als *.NET Framework* bezeichnet wird. **Microsoft empfiehlt, verwaltete Prozess interne Erweiterungen in Windows Explorer oder Windows Internet Explorer zu schreiben, und berücksichtigt sie nicht als unterstütztes Szenario.**

In diesem Thema werden Faktoren erläutert, die Sie berücksichtigen sollten, wenn Sie bestimmen, ob eine andere Runtime als die CLR von in-Process-Erweiterungen verwendet werden kann. Beispiele für andere Laufzeiten sind Java, Visual Basic, JavaScript/ECMAScript, Delphi und die C/C++-Lauf Zeit Bibliothek. Dieses Thema enthält auch einige Gründe, warum verwalteter Code in Prozess internen Erweiterungen nicht unterstützt wird.

## <a name="version-conflicts"></a>Versions Konflikte

Ein Versions Konflikt kann über eine Laufzeit auftreten, die das Laden von mehreren Lauf Zeit Versionen innerhalb eines einzelnen Prozesses nicht unterstützt. Versionen der CLR vor Version 4,0 fallen in diese Kategorie. Wenn das Laden einer Laufzeitversion das Laden von anderen Versionen derselben Laufzeit verhindert, kann dies zu einem Konflikt führen, wenn die Host Anwendung oder eine andere Prozess interne Erweiterung eine widersprüchliche Version verwendet. Im Fall eines Konflikts mit einer anderen Prozess internen Erweiterung kann es schwierig sein, den Konflikt zu reproduzieren, da der Fehler die rechts in Konflikt stehenden Erweiterungen erfordert und der Fehler Modus von der Reihenfolge abhängig ist, in der die in Konflikt stehenden Erweiterungen geladen werden.

Stellen Sie sich eine in-Process-Erweiterung vor, die mit einer Version der CLR vor Version 4,0 geschrieben wurde. Jede Anwendung auf dem Computer, die ein Dialogfeld zum **Öffnen** von Dateien verwendet, kann potenziell den verwalteten Code des Dialog Felds und seine zugehörige CLR-Abhängigkeit in den Prozess der Anwendung laden. Die Anwendung oder Erweiterung, die zuerst eine Pre-4,0-Version der CLR in den Prozess der Anwendung lädt, schränkt die Versionen der CLR ein, die anschließend von diesem Prozess verwendet werden können. Wenn eine verwaltete Anwendung mit einem **geöffneten** Dialogfeld auf einer in Konflikt stehenden Version der CLR basiert, kann die Ausführung der Erweiterung möglicherweise fehlschlagen und Fehler in der Anwendung verursachen. Wenn die Erweiterung dagegen das erste ist, das in einem Prozess geladen werden soll, und eine in Konflikt stehende Version von verwaltetem Code versucht, danach zu starten (möglicherweise eine verwaltete Anwendung oder eine laufende Anwendung lädt die CLR bei Bedarf), schlägt der Vorgang fehl. Für den Benutzer wird angezeigt, dass einige Features der Anwendung zufällig nicht mehr funktionieren, oder die Anwendung stürzt auf einen gewissen Fall ab.

Beachten Sie, dass CLR-Versionen, die kleiner oder gleich der Version 4,0 sind, in der Regel nicht anfällig für das Versions Verwaltungsproblem sind, weil Sie für die Koexistenz miteinander und mit den meisten Pre-4,0-Versionen der CLR entwickelt wurden (mit Ausnahme von Version 1,0, die nicht mit anderen Versionen koexistieren kann). Es können jedoch andere Probleme als Versions Konflikte auftreten, wie im weiteren Verlauf dieses Themas erläutert.

## <a name="performance-issues"></a>Leistungsprobleme

Leistungsprobleme können bei Laufzeiten auftreten, die eine erhebliche Leistungs Einbuße verursachen, wenn Sie in einen Prozess geladen werden. Die Leistungseinbußen können in Form der Speicherauslastung, CPU-Auslastung, verstrichenen Zeit oder sogar des Adressraum Verbrauchs liegen. Die CLR, JavaScript/ECMAScript und Java sind bekanntermaßen mit hoher Auswirkung auf Runtimes. Da in-Process-Erweiterungen in viele Prozesse geladen werden können und dies häufig in Leistungs sensitiven Augenblicken erfolgt (z. b. beim Vorbereiten eines Menüs für die Anzeige des Benutzers), können sich leistungsstarke Laufzeiten negativ auf die Gesamt Reaktionsfähigkeit auswirken.

Eine zeitintensive Laufzeit, die beträchtliche Ressourcen beansprucht, kann einen Fehler im Host Prozess oder eine andere Prozess interne Erweiterung verursachen. Beispielsweise kann eine Laufzeitumgebung mit hoher Auswirkung, bei der Hunderte von Megabyte Adressraum für Ihren Heap verwendet werden, dazu führen, dass die Host Anwendung kein großes Dataset laden kann. Da in-Process-Erweiterungen in mehrere Prozesse geladen werden können, kann der hohe Ressourcenverbrauch in einer einzelnen Erweiterung den hohen Ressourcenverbrauch auf dem gesamten System schnell multiplizieren.

Wenn eine Laufzeit geladen wird oder anderweitig weiterhin Ressourcen beansprucht, auch wenn die Erweiterung, die diese Laufzeit verwendet, entladen wurde, ist diese Laufzeit nicht für die Verwendung in einer Erweiterung geeignet.

## <a name="issues-specific-to-the-net-framework"></a>Spezifische Probleme des .NET Framework

In den folgenden Abschnitten werden Beispiele für Probleme erläutert, die beim Verwenden von verwaltetem Code für Erweiterungen gefunden werden. Dabei handelt es sich nicht um eine vollständige Liste aller möglichen Probleme, die auftreten können. Die hier erläuterten Probleme sind beide, weil verwalteter Code in Erweiterungen und Punkten, die bei der Auswertung der Verwendung anderer Laufzeiten berücksichtigt werden sollten, nicht unterstützt wird.

### <a name="re-entrancy"></a>Wiedereintritt

Wenn die CLR beispielsweise einen STA-Thread (Single Thread-Apartment) blockiert, z. b. aufgrund einer Monitor. Enter-, WaitHandle. WaitOne-oder Konflikten [**Lock**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) -Anweisung, gibt die CLR in der Standardkonfiguration eine schsted Message-Schleife ein, während Sie wartet. Viele Erweiterungs Methoden sind nicht für die Verarbeitung von Nachrichten zulässig. diese unvorhersehbare und unerwartete Wiederholung kann zu anomalen Verhalten führen, das schwer zu reproduzieren und zu diagnostizieren ist.

### <a name="the-multithreaded-apartment"></a>Das Multithread-Apartment

Die CLR erstellt *Runtime Callable Wrapper* für Component Object Model (com)-Objekte. Diese gleichen Runtime Callable Wrapper werden später durch den Finalizer der CLR zerstört, der Teil des Multithread-Apartment (MTA) ist. Das Verschieben des Proxys aus dem STA in den MTA erfordert Marshalling, aber nicht alle Schnittstellen, die von Erweiterungen verwendet werden, können gemarshallt werden.

### <a name="non-deterministic-object-lifetimes"></a>Lebensdauer von nicht deterministischen Objekten

Die CLR verfügt über eine schwächere Objekt Lebensdauer Garantien als nativen Code. Viele Erweiterungen haben Verweis Zähler Anforderungen für Objekte und Schnittstellen, und das von der CLR verwendete Garbage Collection-Modell kann diese Anforderungen nicht erfüllen.

-   Wenn ein CLR-Objekt einen Verweis auf ein COM-Objekt erhält, wird der COM-Objekt Verweis, der vom Runtime Callable Wrapper gehalten wird, erst freigegeben, wenn der Runtime Callable Wrapper in der Garbage Collection erfasst wird. Nicht deterministisches Freigabe Verhalten kann mit einigen Schnittstellen Verträgen in Konflikt stehen. Die [**IPersistPropertyBag:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) -Methode erfordert beispielsweise, dass kein Verweis auf den Eigenschaften Behälter durch das Objekt beibehalten wird, wenn die **Load** -Methode zurückgegeben wird.
-   Wenn ein CLR-Objekt Verweis an systemeigenen Code zurückgegeben wird, gibt der Runtime Callable Wrapper seinen Verweis auf das CLR-Objekt zurück, wenn der letzte Aufruf von [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) des Runtime Callable-Wrapper erfolgt. das zugrunde liegende CLR-Objekt wird jedoch erst beendet, wenn eine Garbage Collection durchgeführt wird. Die nicht deterministische Beendigung kann mit einigen Schnittstellen Verträgen in Konflikt stehen. Miniatur Ansichts Handler sind z. b. erforderlich, um alle Ressourcen sofort freizugeben, wenn der Verweis Zähler auf 0 (null) sinkt.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Akzeptable Verwendungen von verwaltetem Code und anderen Laufzeiten

Es ist zulässig, verwalteten Code und andere Laufzeiten zu verwenden, um Out-of-Process-Erweiterungen zu implementieren. Beispiele für Out-of-Process-Shellerweiterungen:

-   Vorschau Handler
-   Befehlszeilen basierte Aktionen, z. b. die, die unter den \\  \\ **Befehls** unter Schlüsseln des shellverbs registriert sind.
-   COM-Objekte, die auf einem lokalen Server implementiert sind, für Shell-Erweiterungs Punkte, die die Aktivierung außerhalb des Prozesses zulassen.

Einige Erweiterungen können als Prozess interne oder prozessübergreifende Erweiterungen implementiert werden. Diese Erweiterungen können als prozessübergreifende Erweiterungen implementiert werden, wenn Sie diese Anforderungen für in-Process-Erweiterungen nicht erfüllen. Die folgende Liste enthält Beispiele für Erweiterungen, die entweder als Prozess interne Erweiterungen oder als prozessübergreifende Erweiterungen implementiert werden können:

-   [**Iexecutecommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) , der einem **delegateexecute** -Eintrag zugeordnet ist, der unter dem  \\  \\ **Befehls** Unterschlüssel des shellverbs registriert ist.
-   [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) , das der CLSID zugeordnet ist, die unter einem Unterschlüssel des \\ *shellverb*- \\ **DropTarget** registriert ist.
-   [**Iexplorercommandstate**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) , der einem **commandstatehandler** -Eintrag zugeordnet ist, der unter einem Unterschlüssel des  \\ *shellverbs* registriert ist.

 

 
