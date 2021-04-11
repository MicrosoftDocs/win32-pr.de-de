---
title: Definieren von COM-Schnittstellen
description: Microsoft definiert viele COM-Schnittstellen. In den meisten Fällen können Sie diese generischen Schnittstellen wieder verwenden. Allerdings gelten für einige Anwendungen bestimmte Anforderungen, die es wünschenswert machen, ihre eigenen Objekt Schnittstellen zu definieren.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516c02a2c337b2c76229094b0e42d75b44f65d16
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102402"
---
# <a name="defining-com-interfaces"></a>Definieren von COM-Schnittstellen

Microsoft definiert viele COM-Schnittstellen. In den meisten Fällen können Sie diese generischen Schnittstellen wieder verwenden. Allerdings gelten für einige Anwendungen bestimmte Anforderungen, die es wünschenswert machen, ihre eigenen Objekt Schnittstellen zu definieren.

Alle COM-Schnittstellen müssen direkt oder indirekt von der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle abgeleitet werden. Innerhalb dieser Einschränkung kann die benutzerdefinierte Schnittstelle fast jede Methode oder jeden Parameter unterstützen, einschließlich asynchroner Methoden. Sie können auch eine Typbibliothek für die benutzerdefinierten Schnittstellen generieren, damit Clients zur Laufzeit auf Informationen zu den Methoden des Objekts zugreifen können. Nachdem Sie eine Schnittstelle definiert haben, beschreiben Sie Sie in Microsoft Interface Definition Language (mittlerer l), kompilieren und registrieren Sie Sie wie jede generische Schnittstelle. Mit verteiltem com sind Schnittstellen Methoden sowohl für Remote Prozesse als auch für andere Prozesse auf dem gleichen Computer verfügbar.

Zum Schluss erfordert das Entwickeln von COM-Schnittstellen eine Entwicklungsumgebung, die einen C/C++-Compiler und den Midl.exe Compiler umfasst.

Die Schritte zum Erstellen einer COM-Schnittstelle lauten wie folgt:

-   Entscheiden Sie, wie Sie marshalingunterstützung für Ihre Schnittstelle bereitstellen möchten. entweder mit einem Typbibliotheks gesteuerten Marshalling oder mit einer Proxy-/Stub-DLL. Sogar in-Process-Schnittstellen müssen gemarshallt werden, wenn Sie über Apartment Grenzen hinweg verwendet werden sollen. Es empfiehlt sich, die Marshalling-Unterstützung für jede com-Schnittstelle zu entwickeln, auch wenn Sie nicht glauben, dass Sie Sie benötigen. Weitere Informationen finden Sie unter [Interface Marshaling.](interface-marshaling.md)
-   Beschreiben Sie die Schnittstelle oder Schnittstellen in einer Schnittstellen Definitionsdatei (IDL). Außerdem können Sie bestimmte lokale Aspekte Ihrer Schnittstelle in einer Anwendungs Konfigurationsdatei (ACF) angeben. Wenn Sie das Typbibliotheks gesteuerte Marshalling verwenden, fügen Sie eine [**Library**](/windows/desktop/Midl/library) -Anweisung hinzu, die auf die Schnittstellen verweist, für die Sie Typinformationen generieren möchten.
-   Verwenden Sie den Mittelwert Compiler, um eine Typbibliotheks Datei und eine Header Datei zu generieren, bzw. Proxy-/Stubdateien für die C-Sprache, die dll-Datendatei und die Header Datei. Weitere Informationen finden Sie unter [Mittel l-Kompilierung](midl-compilation.md) .
-   Abhängig von der gewählten Marshallingmethode schreiben Sie eine Modul Definitionsdatei (DEF), kompilieren Sie alle in der Mitte generierten Dateien, und verknüpfen Sie Sie mit einer einzelnen Proxy-dll, und registrieren Sie die Schnittstelle in der Systemregistrierung, oder registrieren Sie die Typbibliothek. Weitere Informationen finden Sie unter [Laden und Registrieren einer Typbibliothek](loading-and-registering-a-type-library.md) und entwickeln [und Registrieren einer Proxy-dll](building-and-registering-a-proxy-dll.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anatomie einer IDL-Datei](anatomy-of-an-idl-file.md)
</dt> <dt>

[COM-Clients und-Server](com-clients-and-servers.md)
</dt> <dt>

[Schnittstellen Entwurfs Regeln](interface-design-rules.md)
</dt> <dt>

[Das Component Object Model](the-component-object-model.md)
</dt> </dl>

 

 