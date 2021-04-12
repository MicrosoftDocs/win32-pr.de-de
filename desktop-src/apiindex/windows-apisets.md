---
description: API-Sätze sind funktionale Gruppen von Win32-APIs im Core-Betriebssystem. Sie bieten eine architektonische Trennung von der Host-dll, in der eine gegebene Win32-API definiert ist, und die Funktionsgruppe, zu der die API gehört.
title: Windows-API-Sätze
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 15c8e6ad8124abf06e6ab3c2a8ca2bcd83772855
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104474724"
---
# <a name="windows-api-sets"></a>Windows-API-Sätze

Alle Versionen von Windows 10 verwenden eine gemeinsame Basis von Betriebssystemkomponenten, die als *zentrales Betriebssystem* bezeichnet werden (in einigen Kontexten wird diese gemeinsame Basis auch als " *onecore*" bezeichnet). In den Kern Betriebssystemkomponenten sind Win32-APIs in Funktionsgruppen namens *API-Sätze* organisiert.

Der Zweck eines API-Satzes besteht darin, eine architektonische Trennung von der Host-dll bereitzustellen, in der eine gegebene Win32-API implementiert ist, und den funktionalen Vertrag, zu dem die API gehört. Die Entkopplung, die API-Sätze zwischen Implementierung und Verträge bieten, bietet viele Vorteile für Entwickler. Insbesondere kann die Verwendung von API-Sets in Ihrem Code die Kompatibilität mit allen Windows 10-Geräten verbessern.

API-Sätze berücksichtigen speziell die folgenden Szenarien:

- Obwohl die gesamte Breite der Win32-API auf PCs unterstützt wird, ist nur eine Teilmenge der Win32-API auf anderen Windows 10-Geräten verfügbar, beispielsweise hololens, Xbox und andere Geräte, auf denen Windows 10X ausgeführt wird. Der Name des API-Satzes stellt einen Abfrage Mechanismus bereit, um zu erkennen, ob eine API auf einem bestimmten Gerät verfügbar ist.

- Einige Win32-API-Implementierungen sind in DLLs mit unterschiedlichen Namen auf verschiedenen Windows 10-Geräten vorhanden. Die Verwendung von API-Satz Namen anstelle von DLL-Namen beim Erkennen von API-Verfügbarkeit und verzögertes Laden von APIs stellt eine korrekte Route zur Implementierung bereit, unabhängig davon, wo die API tatsächlich implementiert ist

Weitere Informationen finden Sie unter [API-Satz Ladevorgang](api-set-loader-operation.md) und [erkennen der Verfügbarkeit von API-Sets](detect-api-set-availability.md).

## <a name="linking-to-umbrella-libraries"></a>Verknüpfen mit Dach Bibliotheken

Um das einschränken Ihres Codes auf Win32-APIs zu vereinfachen, die im Kernbetriebssystem unterstützt werden, stellen wir eine Reihe von *Dach Bibliotheken* bereit. Beispielsweise stellt eine Bildschirm Bibliothek mit dem Namen "onecore. lib" die Exporte für die Teilmenge der Win32-APIs bereit, die allen Windows 10-Geräten gemeinsam sind.

Die APIs in einer Oberflächen-Bibliothek können über eine Reihe von Modulen implementiert werden. Diese Details werden von der Umbrella-Bibliothek entfernt, sodass Ihr Code über Windows 10-Versionen und-Geräte hinweg besser portierbar ist. Anstatt mit Bibliotheken wie kernel32. lib und advapi32. lib zu verknüpfen, verknüpfen Sie einfach Ihre Desktop-App oder Ihren Treiber mit der Desktop Bibliothek, die den Satz der wichtigsten Betriebssystem-APIs enthält, an denen Sie interessiert sind.

Weitere Informationen finden Sie unter [Windows](windows-umbrella-libraries.md)-Ober Schirm-Bibliotheken.

## <a name="api-set-contract-names"></a>API-Satz Vertrags Namen

API-Sätze werden durch einen starken Vertrags Namen identifiziert, der diesen Standard Konventionen folgt, die vom Bibliotheks Lader erkannt werden. 

- Der Name muss entweder mit der Zeichen folgen **-API** oder mit **ext-** beginnen. 
    - Namen, die mit **API-** Zeichen beginnen, die auf allen Windows 10-Versionen garantiert vorhanden sind.
    - Namen, die mit **ext** beginnen, repräsentieren APIs, die möglicherweise nicht in allen Windows 10-Versionen vorhanden sind.
- Der Name muss auf die Sequenz **l \<n\> - \<n\> - \<n\>** enden, wobei **n** aus Dezimalziffern besteht.
- Der Text des Namens kann alphanumerische Zeichen oder Bindestriche ( **-** ) sein.
- Für den Namen wird die Groß-/Kleinschreibung nicht beachtet.

Im folgenden finden Sie einige Beispiele für API-Satz Vertrags Namen:

- **API-MS-WIN-Core-ums-L1-1-0**
- **ext-MS-WIN-com-OLE32-L1-1-5**
- **ext-MS-WIN-Ntuser-Window-L1-1-0**
- **ext-MS-WIN-Ntuser-Window-L1-1-1**

Sie können einen API-Satz Namen im Kontext eines Lade Programm Vorgangs verwenden, z. b. [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [P/aufrufen](/dotnet/standard/native-interop/pinvoke) anstelle eines dll-Modul namens, um eine korrekte Route zur Implementierung sicherzustellen, unabhängig davon, wo die API tatsächlich auf dem aktuellen Gerät implementiert ist. Wenn Sie dies tun, müssen Sie jedoch die Zeichenfolge " **. dll** " am Ende des Vertrags namens anfügen. Dies ist eine Anforderung des Lade Moduls, ordnungsgemäß zu funktionieren, und wird nicht als Teil des Vertrags namens angesehen. Obwohl Vertrags Namen in diesem Kontext ähnlich wie DLL-Namen angezeigt werden, unterscheiden Sie sich grundsätzlich von den Namen der dll-Module und verweisen nicht direkt auf eine Datei auf dem Datenträger.

Mit der Ausnahme, dass die Zeichenfolge **. dll** in Lade Ladevorgängen angefügt wird, sollten API-Satz Vertrags Namen als unveränderlicher Bezeichner angesehen werden, der einer bestimmten Vertragsversion entspricht.

## <a name="identifying-api-sets-for-win32-apis"></a>Identifizieren von API-Sätzen für Win32-APIs

Um zu ermitteln, ob eine bestimmte Win32-API zu einem API-Satz gehört, überprüfen Sie die Tabelle "Requirements" in der Referenz Dokumentation für die API. Wenn die API zu einem API-Satz gehört, listet die Anforderungs Tabelle im Artikel den Namen des API-Satzes und die Windows-Version auf, in der die API erstmals in den API-Satz eingeführt wurde. Beispiele für APIs, die zu einem API-Satz gehören, finden Sie in den folgenden Artikeln:

- [Allowsetforegroundwindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [Findwindowsex](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [Getclassfile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>In diesem Abschnitt

* [API-Satz-Ladevorgang](api-set-loader-operation.md)
* [API-Satz-Verfügbarkeit erkennen](detect-api-set-availability.md)
* [Übergeordnete Windows-Bibliothek](windows-umbrella-libraries.md)