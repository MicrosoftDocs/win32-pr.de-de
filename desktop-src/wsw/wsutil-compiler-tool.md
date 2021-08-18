---
title: WsUtil-Compilertool
description: Das Windows Web Services-Compilertool, WsUtil.exe, unterstützt das Dienstmodell und die Serialisierung von Datentypen. Es verarbeitet WSDL-, XML-Schema- und Richtliniendokumente und generiert C-Header und Quelldateien.
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- WsUtil Compiler tool Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9a4e5761a068e991463451595c410c01f868d4d3e6c9df6ab25a7cb232d678
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119324900"
---
# <a name="wsutil-compiler-tool"></a>WsUtil-Compilertool

Das Windows Web Services-Compilertool, WsUtil.exe, unterstützt das [Dienstmodell](service-model-layer-overview.md) und [die Serialisierung](serialization.md) von Datentypen. Es verarbeitet WSDL-, XML-Schema- und Richtliniendokumente und generiert C-Header und Quelldateien. Dieses Tool ähnelt dem WSDL-Compilertool für verwalteten Code, ist aber stattdessen auf nativen Code ausgerichtet.

Zur Unterstützung des [Dienstmodells](service-model-layer-overview.md)generiert WsUtil.exe Header, die sowohl für den Client als auch für den Dienst verwendet werden sollen. Bei Bedarf werden C-Proxydateien für die Clientseite und C-Stubdateien für die Dienstseite generiert.

Zur Unterstützung [der Serialisierung](serialization.md)generiert der Compiler Header für Elementbeschreibungen für globale Elementdefinitionen und alle Typdefinitionsinformationen in den Proxydateien, die von der Serialisierungs-Engine verwendet werden.


Befehlszeilenoptionen zum Verarbeiten von WSDL-Dateien, XML-Schemadateien und Webdienstrichtliniendateien finden Sie in den folgenden Themen:

-   [Webdienstcompilertool](web-service-compiler-tool.md)
-   [WSDL und Dienstverträge](wsdl-support.md)
-   [Unterstützung von Schemas](schema-support.md)
-   [Richtlinienunterstützung](policy-support.md)

## <a name="security"></a>Sicherheit

Wenn Sie WsUtil verwenden, beachten Sie die folgenden Probleme, und beachten Sie die entsprechenden Vorsichtsmaßnahmen:

-   Wsutil ruft keine XML-Metadaten über das Netzwerk ab, und wsutil löst keine Import- und/oder Include-Anweisungen in die Eingabemetadatendateien auf. Wsutil wird geöffnet und liest wsdl-, xsd- und richtliniendateien. XML-Metadaten sind nicht manipulationssicher. Stellen Sie sicher, dass Sie nur wsdl-, xsd- und Richtliniendateien verwenden, die aus einer vertrauenswürdigen Quelle stammen, und stellen Sie sicher, dass Sie die Dateien vor und nach der Verwendung vor Manipulationen schützen. Überprüfen Sie sorgfältig den Inhalt der Eingabedateien, und überprüfen Sie, ob der Inhalt der Dateien sicher für die Verwendung in der Anwendung ist. Wsutil.exe führt keine Überprüfung der Authentizität der Metadatendateien durch.
-   Wsutil generiert Header- und Stubdateien, die nicht manipulationssicher sind. Sie müssen die richtigen Zugriffsrechte für Quelldateien festlegen, die von wsutil.exe, um nicht authentifizierten Zugriff auf diese Dateien zu verhindern. Wsutil verwendet System.IO.StreamWriter, um die Ausgabedateien zu erstellen.
-   Benutzer müssen beachten, dass Wsutil ihre lokalen Dateien überschreiben kann, und sie sollten darauf achten, sichere Dateinamen und Verzeichnisse für Ausgabedateien mithilfe des Schalters /out anzugeben.
-   Wsutil oder wsutilhelper.dll in wsutil.exe geladen werden, kann unerwartet beendet werden oder große Mengen von Systemressourcen verbrauchen, wenn sie angegriffen werden oder eine sehr große Menge von Eingabemetadaten verarbeiten. Das Tool ist nur für die Verwendung während der Entwicklungszeit konzipiert. Dieses Tool sollte nur als Entwicklungszeittool verwendet werden. Es ist möglicherweise nicht sicher für die Verwendung auf der mittleren Ebene, Richtlinieninformationen zu verarbeiten.
-   Wsutilhelper.dll Hilfs-DLL wird in verwaltete wsutil.exe geladen, um Richtlinieninformationen zu verarbeiten. Der Benutzer sollte sicherstellen, dass im binären Pfad keine schädliche Binärdatei mit demselben Dateinamen vorhanden ist. Ebenso sollte der Benutzer sicherstellen, dass in der Buildumgebung der binäre Pfad ordnungsgemäß eingerichtet ist, dass keine schädliche Binärdatei mit demselben Namen wsutil.exe vorhanden ist.
-   Wsutil generiert nach Möglichkeit SAL-Anmerkungen für Vorgänge und Strukturfelder. Der Benutzer von wsutil generierten Dateien sollte die durch die SAL-Anmerkung angegebene Anforderung erfüllen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Dienstmodellebene](service-model-layer-overview.md)
</dt> <dt>

[Serialisierung](serialization.md)
</dt> <dt>

[Webdienstcompilertool](web-service-compiler-tool.md)
</dt> <dt>

[WSDL-Unterstützung](wsdl-support.md)
</dt> <dt>

[Unterstützung von Schemas](schema-support.md)
</dt> <dt>

[Richtlinienunterstützung](policy-support.md)
</dt> </dl>

 

 




