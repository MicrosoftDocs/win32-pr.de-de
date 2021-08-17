---
description: API-Sätze sind Funktionsgruppen von Win32-APIs im Kernbetriebssystem. Sie bieten eine architektonische Trennung von der Host-DLL, in der eine bestimmte Win32-API definiert ist, und der Funktionsgruppe, zu der die API gehört.
title: Windows API-Sätze
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 34724f255b963c23406ed5bdc59de0278e68a6f75de0d00b4d45aa449575af89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737607"
---
# <a name="windows-api-sets"></a>Windows API-Sätze

Alle Versionen von Windows 10 eine gemeinsame Basis von Betriebssystemkomponenten, die als Kernbetriebssystem bezeichnet wird *(in* einigen Kontexten wird diese allgemeine Basis auch *als OneCore.* In den Kernkomponenten des Betriebssystems sind Win32-APIs in Funktionsgruppen organisiert, die als *API-Sätze bezeichnet werden.*

Der Zweck eines API-Sets besteht in der Architekturtrennung von der Host-DLL, in der eine bestimmte Win32-API implementiert ist, und dem Funktionsvertrag, zu dem die API gehört. Die Entkopplung, die API-Sätze zwischen Implementierung und Verträgen bieten, bietet entwicklern viele Technische Vorteile. Insbesondere die Verwendung von API-Sätzen in Ihrem Code kann die Kompatibilität mit allen Windows 10 verbessern.

API-Sätze adressieren insbesondere die folgenden Szenarien:

- Obwohl die gesamte Breite der Win32-API auf PCs unterstützt wird, ist nur eine Teilmenge der Win32-API auf anderen Windows 10-Geräten wie HoloLens, Xbox und anderen Geräten verfügbar, auf denen Windows 10x ausgeführt wird. Der API-Satzname stellt einen Abfragemechanismus bereit, um sauber zu erkennen, ob eine API auf einem bestimmten Gerät verfügbar ist.

- Einige Win32-API-Implementierungen sind in DLLs mit unterschiedlichen Namen auf verschiedenen Windows 10 vorhanden. Die Verwendung von API-Satznamen anstelle von DLL-Namen beim Erkennen der API-Verfügbarkeit und verzögerten Laden von APIs stellt eine korrekte Route zur Implementierung bereit, unabhängig davon, wo die API tatsächlich implementiert ist.

Weitere Informationen finden Sie unter [API Set Loader operation (API Set Loader-Vorgang)](api-set-loader-operation.md) und Detect API set availability (Erkennen [der Verfügbarkeit von API-Sets).](detect-api-set-availability.md)

## <a name="linking-to-umbrella-libraries"></a>Verknüpfen mit Schirmbibliotheken

Um es einfacher zu machen, Ihren Code auf Win32-APIs zu beschränken, die im Kernbetriebssystem unterstützt werden, stellen wir eine Reihe von *Schirmbibliotheken zur Verfügung.* Beispielsweise stellt eine Oberbibliothek namens OneCore.lib die Exporte für die Teilmenge der Win32-APIs zur Verfügung, die für alle Windows 10 sind.

Die APIs in einer Schirmbibliothek können für eine Reihe von Modulen implementiert werden. Die Oberbibliothek abstrahiert diese Details von Ihnen, wodurch Ihr Code für Windows 10 Geräte portierbarer wird. Anstatt eine Verknüpfung mit Bibliotheken wie kernel32.lib und advapi32.lib zu erstellen, verknüpfen Sie einfach Ihre Desktop-App oder Ihren Treiber mit der Oberbibliothek, die die Kern-BETRIEBSSYSTEM-APIs enthält, an denen Sie interessiert sind.

Weitere Informationen finden Sie unter [Windows Schirmbibliotheken](windows-umbrella-libraries.md).

## <a name="api-set-contract-names"></a>API-Set-Vertragsnamen

API-Sätze werden durch einen starken Vertragsnamen identifiziert, der diesen standardkonventionen entspricht, die vom Bibliotheklader erkannt werden. 

- Der Name muss entweder mit der Zeichenfolge **api-** oder **ext- beginnen.** 
    - Namen, die mit **api beginnen,** stellen APIs dar, die in allen Versionen Windows 10 sind.
    - Namen, die mit **ext beginnen,** stellen APIs dar, die möglicherweise nicht in allen versionen Windows 10 sind.
- Der Name muss mit der Sequenz **\<n\> - \<n\> - \<n\> l** enden, wobei **n** aus Dezimalstellen besteht.
- Der Text des Namens kann alphanumerische Zeichen oder Bindestriche () **-** sein.
- Für den Namen wird die Groß-/Kleinschreibung nicht beachtet.

Hier sind einige Beispiele für API-Satzvertragsnamen:

- **api-ms-win-core-ums-l1-1-0**
- **ext-ms-win-com-ole32-l1-1-5**
- **ext-ms-win-ntuser-window-l1-1-0**
- **ext-ms-win-ntuser-window-l1-1-1**

Sie können einen API-Satznamen im Kontext eines [Ladevorgang wie LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [P/Invoke](/dotnet/standard/native-interop/pinvoke) anstelle eines DLL-Modulnamens verwenden, um eine korrekte Route zur Implementierung sicherzustellen, unabhängig davon, wo die API tatsächlich auf dem aktuellen Gerät implementiert ist. Wenn Sie dies tun, müssen  Sie die Zeichenfolge jedoch.dllam Ende des Vertragsnamens anfügen. Dies ist eine Anforderung des Ladeers, damit es ordnungsgemäß funktioniert, und wird nicht als Teil des Vertragsnamens betrachtet. Obwohl Vertragsnamen in diesem Kontext ähnlich wie DLL-Namen erscheinen, unterscheiden sie sich grundlegend von DLL-Modulnamen und verweisen nicht direkt auf eine Datei auf dem Datenträger.

Mit Ausnahme des Anfügens der **.dll** in Ladevorgängen sollten API-Satzvertragsnamen als unveränderbarer Bezeichner betrachtet werden, der einer bestimmten Vertragsversion entspricht.

## <a name="identifying-api-sets-for-win32-apis"></a>Identifizieren von API-Sätzen für Win32-APIs

Um festzustellen, ob eine bestimmte Win32-API zu einem API-Satz gehört, lesen Sie die Anforderungstabelle in der Referenzdokumentation für die API. Wenn die API zu einem API-Satz gehört, werden in der Tabelle mit den Anforderungen im Artikel der Name des API-Sets und die Windows-Version aufgeführt, in der die API zum ersten Mal in den API-Satz eingeführt wurde. Beispiele für APIs, die zu einem API-Satz gehören, finden Sie in den folgenden Artikeln:

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>In diesem Abschnitt

* [API-Satz-Ladevorgang](api-set-loader-operation.md)
* [API-Satz-Verfügbarkeit erkennen](detect-api-set-availability.md)
* [Übergeordnete Windows-Bibliothek](windows-umbrella-libraries.md)