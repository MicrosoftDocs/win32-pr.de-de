---
title: Wsutil-Compilertool
description: Das Windows-Webdienste-Compilertool (WsUtil.exe) unterstützt das Dienstmodell und die Serialisierung von Datentypen. Es verarbeitet WSDL-, XML-Schema-und-Richtlinien Dokumente und generiert C-Header und-Quelldateien.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- Wsutil-Compilertool-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949235"
---
# <a name="wsutil-compiler-tool"></a>Wsutil-Compilertool

Das Windows-Webdienste-Compilertool (WsUtil.exe) unterstützt das [Dienstmodell](service-model-layer-overview.md) und die [Serialisierung](serialization.md) von Datentypen. Es verarbeitet WSDL-, XML-Schema-und-Richtlinien Dokumente und generiert C-Header und-Quelldateien. Dieses Tool ähnelt dem WSDL-Compilertool für verwalteten Code, ist stattdessen jedoch auf nativen Code ausgerichtet.

Zur Unterstützung des [Dienst Modells](service-model-layer-overview.md)generiert WsUtil.exe Header, die sowohl für den Client als auch für den Dienst verwendet werden. Es generiert bei Bedarf die c-Proxy Datei für die Clientseite und c-Stubdateien für die Dienst Seite.

Zur Unterstützung der [Serialisierung](serialization.md)generiert der Compiler Header für Element Beschreibungen für globale Element Definitionen und alle typdefinitions Informationen in den Proxy Dateien, die von der Serialisierungs-Engine verwendet werden.


Informationen zu Befehlszeilenoptionen für die Verarbeitung von WSDL-Dateien, XML-Schema Dateien und Webdienst-Richtlinien Dateien finden Sie in den folgenden Themen:

-   [Webdienst-Compilertool](web-service-compiler-tool.md)
-   [WSDL und Dienstverträge](wsdl-support.md)
-   [Unterstützung von Schemas](schema-support.md)
-   [Richtlinien Unterstützung](policy-support.md)

## <a name="security"></a>Sicherheit

Beachten Sie bei der Verwendung von wsutil die folgenden Probleme, und beachten Sie die entsprechenden Vorsichtsmaßnahmen:

-   Wsutil ruft keine XML-Metadaten über das Netzwerk ab, und wsutil löst keine Import-und/oder include-Anweisungen in den eingabemetadatendateien aus. Wsutil öffnet und liest WSDL-, XSD-und-Richtlinien Dateien. XML-Metadaten sind nicht Manipulations beständig. Stellen Sie sicher, dass Sie nur WSDL-, XSD-und Richtlinien Dateien verwenden, die von der vertrauenswürdigen Quelle abgerufen werden, und stellen Sie sicher, dass die Dateien vor und nach deren Verwendung manipuliert werden. Überprüfen Sie sorgfältig den Inhalt der Eingabedateien, und überprüfen Sie, ob der Inhalt der Dateien sicher für die Verwendung in der Anwendung ist. Wsutil.exe überprüft keine Echtheit der Metadatendateien.
-   Wsutil generiert Header-und Stubdateien, die nicht Manipulations beständig sind. Sie müssen die richtigen zugriffszugriffsrechte für die von wsutil.exe generierten Quelldateien festlegen, um den nicht autorisierten Zugriff auf diese Dateien zu verhindern. Wsutil verwendet System. IO. StreamWriter zum Erstellen der Ausgabedateien.
-   Benutzer müssen sich bewusst sein, dass wsutil ihre lokalen Dateien überschreiben kann, und Sie sollten darauf achten, sichere Dateinamen und Verzeichnisse für Ausgabedateien mithilfe des/Out-Schalters anzugeben.
-   Wsutil oder wsutilhelper.dll, die in wsutil.exe geladen werden, können unerwartet beendet werden oder eine große Menge an Systemressourcen verbrauchen, wenn Sie angegriffen werden oder wenn eine sehr große Menge von Eingabe Metadaten verarbeitet wird. Das Tool ist für die Verwendung während der Entwicklungszeit konzipiert. dieses Tool sollte nur als Entwicklungszeit Tool verwendet werden. Es ist möglicherweise nicht sicher, dass Sie in der mittleren Ebene zur Verarbeitung von Richtlinien Informationen verwendet werden.
-   Wsutilhelper.dll-Hilfsprogramm-DLL wird in verwaltete wsutil.exe geladen, um Richtlinien Informationen zu verarbeiten. Der Benutzer sollte sicherstellen, dass im binären Pfad keine böswillige Binärdatei mit demselben Dateinamen vorhanden ist. Ebenso sollte der Benutzer in der Buildumgebung sicherstellen, dass der binäre Pfad ordnungsgemäß eingerichtet ist, dass keine bösartige Binärdatei mit demselben "wsutil.exe"-Namen vorhanden ist.
-   Wsutil generiert eine SAL-Anmerkung für Vorgänge und Struktur Felder, wenn dies möglich ist. Der Benutzer von Dateien, die von wsutil generiert wurden, sollte die mit SAL-Anmerkung angegebene Anforderung einhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Dienstmodell Ebene](service-model-layer-overview.md)
</dt> <dt>

[Serialisierung](serialization.md)
</dt> <dt>

[Webdienst-Compilertool](web-service-compiler-tool.md)
</dt> <dt>

[WSDL-Unterstützung](wsdl-support.md)
</dt> <dt>

[Unterstützung von Schemas](schema-support.md)
</dt> <dt>

[Richtlinien Unterstützung](policy-support.md)
</dt> </dl>

 

 




