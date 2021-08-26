---
title: Definieren von COM-Schnittstellen
description: Microsoft definiert viele COM-Schnittstellen. In den meisten Fällen können Sie diese generischen Schnittstellen wiederverwenden. Einige Anwendungen haben jedoch bestimmte Anforderungen, die es wünschenswert oder erforderlich machen, ihre eigenen Objektschnittstellen zu definieren.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e676172e51fca810f0cbb7ba93b5d52b814319b6e8b890f20ba9c51617f7ac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071020"
---
# <a name="defining-com-interfaces"></a>Definieren von COM-Schnittstellen

Microsoft definiert viele COM-Schnittstellen. In den meisten Fällen können Sie diese generischen Schnittstellen wiederverwenden. Einige Anwendungen haben jedoch bestimmte Anforderungen, die es wünschenswert oder erforderlich machen, ihre eigenen Objektschnittstellen zu definieren.

Alle COM-Schnittstellen müssen direkt oder indirekt von der [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) abgeleitet werden. Innerhalb dieser Einschränkung kann Ihre benutzerdefinierte Schnittstelle fast jede Methode oder jeden Parameter unterstützen, einschließlich asynchroner Methoden. Sie können auch eine Typbibliothek für Ihre benutzerdefinierten Schnittstellen generieren, damit Clients zur Laufzeit auf Informationen zu den Methoden Ihres Objekts zugreifen können. Nachdem Sie eine Schnittstelle definiert, in Microsoft Interface Definition Language (MIDL) beschrieben, kompiliert und registriert haben, verwenden Sie sie wie jede generische Schnittstelle. Mit verteilten COM sind Schnittstellenmethoden sowohl für Remoteprozesse als auch für andere Prozesse auf demselben Computer verfügbar.

Schließlich erfordert das Erstellen von COM-Schnittstellen eine Entwicklungsumgebung, die einen C/C++-Compiler und den Midl.exe Compiler enthält.

Die Schritte zum Erstellen einer COM-Schnittstelle sind wie folgt:

-   Entscheiden Sie, wie Sie Marshallingunterstützung für Ihre Schnittstelle bereitstellen möchten. entweder mit typbibliotheksgesteuertem Marshalling oder mit einer Proxy-/Stub-DLL. Selbst Prozessinterfaces müssen gemarshallt werden, wenn sie über Apartmentgrenzen hinweg verwendet werden sollen. Es ist eine gute Idee, Marshallingunterstützung in jede COM-Schnittstelle zu integrieren, auch wenn Sie nicht glauben, dass Sie sie benötigen. Weitere Informationen finden Sie unter [Schnittstellen marshallen.](interface-marshaling.md)
-   Beschreiben der Schnittstelle oder Schnittstellen in einer IDL-Datei (Interface Definition). Darüber hinaus können Sie bestimmte lokale Aspekte Ihrer Schnittstelle in einer Anwendungskonfigurationsdatei (Application Configuration File, ACF) angeben. Wenn Sie typbibliotheksgesteuertes Marshalling verwenden, fügen Sie eine [**Bibliotheks-Anweisung**](/windows/desktop/Midl/library) hinzu, die auf die Schnittstellen verweist, für die Sie Typinformationen generieren möchten.
-   Verwenden Sie den MIDL-Compiler, um eine Typbibliotheksdatei und headerdatei oder C-Sprachproxy-/Stubdateien, Schnittstellenbezeichnerdateien, DLL-Datendateien und Headerdateien zu generieren. Weitere Informationen finden Sie unter [MIDL-Kompilierung.](midl-compilation.md)
-   Schreiben Sie abhängig von der gewählten Marshallingmethode eine Moduldefinitionsdatei (DEF), kompilieren und verknüpfen Sie alle MIDL-generierten Dateien in einer einzelnen Proxy-DLL, und registrieren Sie die Schnittstelle in der Systemregistrierung, oder registrieren Sie die Typbibliothek. Weitere Informationen finden Sie unter [Laden und Registrieren einer Typbibliothek](loading-and-registering-a-type-library.md) und Erstellen und Registrieren einer [Proxy-DLL.](building-and-registering-a-proxy-dll.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufbau einer IDL-Datei](anatomy-of-an-idl-file.md)
</dt> <dt>

[COM-Clients und -Server](com-clients-and-servers.md)
</dt> <dt>

[Schnittstellenentwurfsregeln](interface-design-rules.md)
</dt> <dt>

[Das Component Object Model](the-component-object-model.md)
</dt> </dl>

 

 