---
description: In-Process-Erweiterungen werden in alle Prozesse geladen, die sie auslösen.
title: Leitfaden zum Implementieren von In-Process-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ccbee300cbfe1b08bc0509472ac3afcaa9ea3db54f6f1e38131cc08d2e8381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858175"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Leitfaden zum Implementieren von In-Process-Erweiterungen

In-Process-Erweiterungen werden in alle Prozesse geladen, die sie auslösen. Beispielsweise kann eine Shellnamespaceerweiterung in einen beliebigen Prozess geladen werden, der direkt oder indirekt auf den Shellnamespace zugreift. Der Shellnamespace wird von vielen Shellvorgängen verwendet, z. B. der Anzeige eines allgemeinen Dateidialogfelds, dem Starten eines Dokuments über die zugehörige Anwendung oder dem Abrufen des Symbols, das zur Darstellung einer Datei verwendet wird. Da In-Process-Erweiterungen in beliebige Prozesse geladen werden können, muss darauf geachtet werden, dass sie sich nicht negativ auf die Hostanwendung oder andere Prozesserweiterungen auswirken.

Eine Laufzeit von besonderem Hinweis ist die *Common Language Runtime (CLR),* auch bekannt als *verwalteter Code* oder die *.NET Framework*. **Microsoft empfiehlt, keine verwalteten In-Process-Erweiterungen in Windows Explorer oder Windows Internet Explorer zu schreiben, und betrachtet sie nicht als unterstütztes Szenario.**

In diesem Thema werden Faktoren erläutert, die berücksichtigt werden müssen, wenn Sie bestimmen, ob eine andere Runtime als die CLR für die Verwendung durch Prozesserweiterungen geeignet ist. Beispiele für andere Runtimes sind Java, Visual Basic, JavaScript/ECMAScript, Vb und die C/C++-Laufzeitbibliothek. Dieses Thema enthält auch einige Gründe dafür, dass verwalteter Code in Prozesserweiterungen nicht unterstützt wird.

## <a name="version-conflicts"></a>Versionskonflikte

Ein Versionskonflikt kann durch eine Laufzeit entstehen, die das Laden mehrerer Runtimeversionen innerhalb eines einzelnen Prozesses nicht unterstützt. Versionen der CLR vor Version 4.0 fallen in diese Kategorie. Wenn das Laden einer Version einer Runtime das Laden anderer Versionen derselben Runtime ausschließt, kann dies zu einem Konflikt kommen, wenn die Hostanwendung oder eine andere in-Process-Erweiterung eine in Konflikt stehende Version verwendet. Im Falle eines Versionskonflikts mit einer anderen In-Process-Erweiterung kann der Konflikt schwierig zu reproduzieren sein, da der Fehler die richtigen in Konflikt stehenden Erweiterungen erfordert und der Fehlermodus von der Reihenfolge abhängt, in der die in Konflikt stehenden Erweiterungen geladen werden.

Betrachten Sie eine In-Process-Erweiterung, die mit einer Version der CLR vor Version 4.0 geschrieben wurde. Für jede Anwendung auf dem Computer, die ein Dialogfeld **"Datei öffnen"** verwendet, können möglicherweise der verwaltete Code des Dialogs und die zugehörige CLR-Abhängigkeit in den Prozess der Anwendung geladen werden. Die Anwendung oder Erweiterung, die zuerst eine Version vor 4.0 der CLR in den Prozess der Anwendung laden soll, schränkt ein, welche Versionen der CLR anschließend von diesem Prozess verwendet werden können. Wenn eine verwaltete Anwendung mit einem Dialogfeld **Öffnen** auf einer in Konflikt stehenden Version der CLR basiert, kann die Erweiterung möglicherweise nicht ordnungsgemäß ausgeführt werden und zu Fehlern in der Anwendung führen. Wenn die Erweiterung dagegen die erste erweiterung ist, die in einem Prozess geladen wird und eine in Konflikt stehende Version von verwaltetem Code danach versucht, den Start auszuführen (möglicherweise lädt eine verwaltete Anwendung oder eine ausgeführte Anwendung die CLR bei Bedarf), schlägt der Vorgang fehl. Für den Benutzer scheint es, dass einige Funktionen der Anwendung nach dem Zufallsprinzip nicht mehr funktionieren, oder die Anwendung stürzt ab.

Beachten Sie, dass Versionen der CLR gleich oder höher als Version 4.0 im Allgemeinen nicht anfällig für das Versionsproblem sind, da sie so konzipiert sind, dass sie gleichzeitig und mit den meisten Versionen vor 4.0 der CLR vorhanden sind (mit Ausnahme von Version 1.0, die nicht gleichzeitig mit anderen Versionen vorhanden sein kann). Es können jedoch andere Probleme als Versionskonflikte auftreten, wie im weiteren Verlauf dieses Themas erläutert.

## <a name="performance-issues"></a>Leistungsprobleme

Leistungsprobleme können bei Laufzeiten auftreten, die erhebliche Leistungseinbußen verursachen, wenn sie in einen Prozess geladen werden. Die Leistungseinbußen können in Form von Speicherauslastung, CPU-Auslastung, verstrichener Zeit oder sogar Adressraumnutzung auftreten. ClR, JavaScript/ECMAScript und Java sind bekanntermaßen Laufzeiten mit hohen Auswirkungen. Da In-Process-Erweiterungen in viele Prozesse geladen werden können und häufig in leistungsabhängigen Momenten (z. B. bei der Vorbereitung eines Menüs für die Anzeige des Benutzers) erfolgen, können Laufzeiten mit hohen Auswirkungen sich negativ auf die allgemeine Reaktionsfähigkeit auswirken.

Eine Laufzeit mit hohen Auswirkungen, die erhebliche Ressourcen verbraucht, kann zu einem Fehler im Hostprozess oder einer anderen Prozesserweiterung führen. Beispielsweise kann eine Laufzeit mit großen Auswirkungen, die Hunderte von Megabyte Adressraum für ihren Heap beansprucht, dazu führen, dass die Hostanwendung kein großes Dataset laden kann. Da In-Process-Erweiterungen in mehrere Prozesse geladen werden können, kann sich der hohe Ressourcenverbrauch in einer einzelnen Erweiterung schnell mit einem hohen Ressourcenverbrauch im gesamten System multiplizieren.

Wenn eine Laufzeit geladen bleibt oder anderweitig weiterhin Ressourcen verbraucht, auch wenn die Erweiterung, die diese Runtime verwendet, entladen wurde, ist diese Runtime nicht für die Verwendung in einer Erweiterung geeignet.

## <a name="issues-specific-to-the-net-framework"></a>Spezifische Probleme für die .NET Framework

In den folgenden Abschnitten werden Beispiele für Probleme bei der Verwendung von verwaltetem Code für Erweiterungen erläutert. Dabei handelt es sich nicht um eine vollständige Liste aller möglichen Probleme, die auftreten können. Die hier beschriebenen Probleme sind beide Gründe dafür, dass verwalteter Code in Erweiterungen nicht unterstützt wird, und Punkte, die beim Auswerten der Verwendung anderer Runtimes zu berücksichtigen sind.

### <a name="re-entrancy"></a>Wiedereinführung

Wenn die CLR einen SINGLETHREAD-Apartmentthread (STA) blockiert, z. B. aufgrund einer Monitor.Enter-, WaitHandle.WaitOne- oder einer strittigen [**Lock-Anweisung,**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) wechselt die CLR in ihrer Standardkonfiguration in eine geschachtelte Nachrichtenschleife, während sie wartet. Viele Erweiterungsmethoden sind an der Verarbeitung von Nachrichten gehindert, und diese unvorhersehbare und unerwartete Wiederinvarianz kann zu anomalem Verhalten führen, das schwer zu reproduzieren und zu diagnostizieren ist.

### <a name="the-multithreaded-apartment"></a>Multithread-Apartment

Die CLR erstellt *Runtime Callable Wrapper* für Component Object Model -Objekte (COM). Dieselben Runtime Callable Wrapper werden später vom Finalizer der CLR zerstört, der Teil des Multithread-Apartment (MTA) ist. Das Verschieben des Proxys aus dem STA in den MTA erfordert Marshalling, aber nicht alle Schnittstellen, die von Erweiterungen verwendet werden, können gemarshallt werden.

### <a name="non-deterministic-object-lifetimes"></a>Nicht deterministische Objektlebensdauern

Die CLR verfügt über schwächere Objektlebensdauergarantien als nativer Code. Viele Erweiterungen haben Verweisanzahlanforderungen für Objekte und Schnittstellen, und das von der CLR verwendete Garbage Collection-Modell kann diese Anforderungen nicht erfüllen.

-   Wenn ein CLR-Objekt einen Verweis auf ein COM-Objekt abruft, wird der COM-Objektverweis, der vom Runtime Callable Wrapper gehalten wird, erst freigegeben, wenn der Runtime Callable Wrapper garbage-collected wird. Das nicht deterministische Releaseverhalten kann mit einigen Schnittstellenverträgen in Konflikt geraten. Die [**IPersistPropertyBag::Load-Methode**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) erfordert beispielsweise, dass kein Verweis auf den Eigenschaftenbehälter vom -Objekt beibehalten wird, wenn die **Load-Methode** zurückgegeben wird.
-   Wenn ein CLR-Objektverweis an nativen Code zurückgegeben wird, gibt der Runtime Callable Wrapper seinen Verweis auf [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) das CLR-Objekt ab, wenn der endgültige Releaseaufruf des Runtime Callable Wrappers erfolgt, aber das zugrunde liegende CLR-Objekt wird erst abgeschlossen, wenn es vom Garbage Collection-Objekt erfasst wird. Die nicht deterministische Finalisierung kann mit einigen Schnittstellenverträgen in Konflikt geraten. Miniaturansichtshandler sind beispielsweise erforderlich, um alle Ressourcen sofort freizugeben, wenn ihre Verweisanzahl auf 0 (null) fällt.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Zulässige Verwendungsmöglichkeiten von verwaltetem Code und anderen Runtimes

Es ist akzeptabel, verwalteten Code und andere Runtimes zu verwenden, um Out-of-Process-Erweiterungen zu implementieren. Beispiele für Out-of-Process-Shellerweiterungen sind:

-   Vorschauhandler
-   Befehlszeilenbasierte Aktionen, z. B. aktionen, die unter  \\ *Shellverbbefehlsunterschlüsseln* registriert \\  sind.
-   COM-Objekte, die auf einem lokalen Server implementiert sind, für Shell-Erweiterungspunkte, die eine Out-of-Process-Aktivierung ermöglichen.

Einige Erweiterungen können entweder als In-Process- oder Out-of-Process-Erweiterungen implementiert werden. Sie können diese Erweiterungen als Out-of-Process-Erweiterungen implementieren, wenn sie diese Anforderungen für In-Process-Erweiterungen nicht erfüllen. Die folgende Liste zeigt Beispiele für Erweiterungen, die entweder als In-Process- oder Out-of-Process-Erweiterungen implementiert werden können:

-   [**IExecuteCommand,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) das einem **DelegateExecute-Eintrag** zugeordnet ist, der unter einem **Shellverb-Befehlsunterschlüssel** registriert \\  \\  ist.
-   [**IDropTarget,**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) das der CLSID zugeordnet ist, die unter einem \\ *Shellverb* \\ **DropTarget-Unterschlüssel** registriert ist.
-   [**IExplorerCommandState,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) der einem **CommandStateHandler-Eintrag** zugeordnet ist, der unter einem **Shellverb-Unterschlüssel** registriert \\  ist.

 

 
