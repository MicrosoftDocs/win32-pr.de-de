---
description: Beschreibt die von wsdcodegen verwendeten Eingabedateien und die von wsdcodegen generierten Ausgabedateien.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Informationen zu wsdcodegen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042054"
---
# <a name="about-wsdcodegen"></a>Informationen zu wsdcodegen

Wsdcodegen verwendet eine XML-Konfigurationsdatei, um den Speicherort der Dienst Metadaten zu bestimmen. Die Konfigurationsdatei wird auch zum Definieren von Schnittstellennamen, Schnittstellen-GUIDs, Klassennamen, Methodennamen und anderen Bezeichnerzeichen verwendet. Weitere Informationen zu dieser Datei finden Sie unter [wsdcodegen-Konfigurationsdatei](wsdcodegen-configuration-file.md).

Wsdcodegen erfordert zwei Arten von Eingabedateien: eine XML-Konfigurationsdatei und eine oder mehrere Dienst Beschreibungsdateien (WSDL-und/oder XSD-Dateien). Wsdcodegen verarbeitet diese Eingabedateien und generiert zwei Arten von Ausgabedateien: Schnittstellen Dateien und Header/Quelldateien.

## <a name="input-files"></a>Eingabedateien



| type                      | BESCHREIBUNG                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurationsdatei        | Eine XML-Datei, die den Speicherort der Dienst Metadaten angibt und Schnittstellennamen, Schnittstellen-GUIDs, Klassennamen, Methodennamen und andere Bezeichner definiert. |
| Dienst Beschreibungsdateien | Mindestens eine WSDL-oder XSD-Datei, die die auf dem Gerät zu implementierenden Dienste beschreibt.                                                                           |



 

## <a name="output-files"></a>Ausgabedateien



| type                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen Dateien             | Eine IDL-Datei (Interface Definition Language), die mit dem Mittelwert Compiler verwendet werden kann, um eine Schnittstellen Header Datei zu entwickeln. WSDAPI-Clients und WSDAPI-Dienste können diese Schnittstellen Datei verwenden.                                                                                                                                                           |
| C++-Header und-Quelldateien | C++-Dateien, die den Nachrichten Vertrag, den Namespace und die Typinformationen beschreiben. Sie enthalten möglicherweise Proxycode und/oder Stub-Code. Der Proxycode implementiert die-Schnittstelle eines Dienstanbieter und übersetzt Dienst Methodenaufrufe in WSDAPI-Vorgänge, die Service Requests ausführen. Der Stubcode übersetzt WSDAPI-Dienst Anforderungen in Code, der Dienst Methoden aufruft. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Code-Generator für Webdienste auf Geräten](web-services-for-devices-code-generator.md)
</dt> <dt>

[Verwenden von wsdcodegen](using-wsdcodegen.md)
</dt> </dl>

 

 



