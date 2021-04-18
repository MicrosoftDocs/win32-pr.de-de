---
description: Eine Anwendung sollte in der Lage sein, Daten aus mehreren Formaten zu erzeugen und zu nutzen.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Persistenzformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8edd88a4b170d2299832a205d80dc6704aea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351026"
---
# <a name="persistence-formats"></a>Persistenzformate

Eine Anwendung sollte in der Lage sein, Daten aus mehreren Formaten zu erzeugen und zu nutzen. Diese umfassen häufig proprietäre Binär Formate und sollten außerdem einige Standardformate enthalten, z. b. RTF (Rich Text Format) oder HTML.

In der folgenden Tabelle sind einige Formate aufgelistet, die frei Hand Eingaben enthalten können.



| Format                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binary<br/>                           | Anwendungen sollten das frei Hand Format (Ink serialisiert Format, ISF) verwenden, um Freihand in Ihre Binär Formate zu codieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Ein HTML-Format wird für die Darstellung Hetero gener Inhalte dringend empfohlen. Anwendungen sollten die Verwendung von Graphics Interchange Format (GIF) zum Codieren von frei Hand Eingaben in Ihre HTML-Dokumente verwenden. Weitere Informationen zu den verstärkten-GIFs finden Sie unter [Bausteine](building-blocks.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Image<br/>                            | Bei Anwendungen, für die keine andere Schnittmenge an Kompatibilität besteht, sollte eine frei Hand fähige Anwendung Bitmap-und metadateiformatierte Images in die Zwischenablage verschieben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Serialisiertes Freihandformat (Ink Serialized Format; ISF)<br/>      | Bei ISF handelt es sich um die kompakteste permanente Freihanddarstellung. Obwohl Sie häufig nur frei Hand Daten enthält, ist ISF erweiterbar. Anwendungen können benutzerdefinierte Attribute (identifiziert durch eine Globally Unique Identifier (GUID)) [**auf ein frei**](inkdisp-class.md) Hand Objekt, einen frei Hand Strich oder einen frei Hand Punkt festlegen. Dies ermöglicht es Ihnen, beliebige Arten von Daten oder Metadaten als Attribut in einem ISF-Stream zu speichern. Für die Interoperabilität zwischen der Zwischenablage können frei Hand Eingaben in einem Standard-Zwischenablage Slot für ISF abgelegt werden, der in den Software Development Kit-Header Dateien (SDK) definiert ist.<br/> ISF ist ein spezifisches Format der Microsoft Tablet PC-Technologie und wird nur in den [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) -und [**Save**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) -Methoden des [**Ink**](inkdisp-class.md) -Objekts unterstützt.<br/> |
| RTF<br/>                              | Es ist möglich, ein RTF-Zwischenablage Format zu generieren und Freihand in RTF als OLE-Objekte zu codieren. Dadurch kann die frei Hand Eingabe in einen OLE-Container eingefügt werden, wie z. b. Microsoft Word oder eine RichEdit-basierte Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Extensible Markup Language (XML)<br/> | Anwendungen können entweder eines der frei Hand Formate verwenden, die Base-64-codiert sind, um frei Hand Eingaben im XML-Dateiformat zu speichern. Ein XML-Format eignet sich zum Eingeben von frei Hand Inhalten in eine Datenbank, wie im Fall eines Signatur Felds oder sogar als primäres Dateiformat für Anwendungen. Dadurch wird die Notwendigkeit zum Schreiben eines Parsers verringert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




