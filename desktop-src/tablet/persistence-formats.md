---
description: Eine Anwendung sollte in der Lage sein, Daten aus mehreren Formaten zu erstellen und zu nutzen.
ms.assetid: bf60fab7-866b-4659-8316-653509ac5112
title: Persistenzformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853dc316d25395a30a15b02734ea4b7ed901b92379e04faa42f5abe5e768af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596640"
---
# <a name="persistence-formats"></a>Persistenzformate

Eine Anwendung sollte in der Lage sein, Daten aus mehreren Formaten zu erstellen und zu nutzen. Diese umfassen häufig proprietäre Binärformate und sollten auch einige Standardformate enthalten, z. B. Rich Text Format (RTF) oder HTML.

In der folgenden Tabelle sind einige Formate aufgeführt, die Ink enthalten können.



| Format                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Binary<br/>                           | Anwendungen sollten das ink serialisierte Format (ISF) verwenden, um Ink in ihre Binärformate zu codieren.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| HTML<br/>                             | Ein HTML-Format wird dringend für die Darstellung heterogener Inhalte empfohlen. Anwendungen sollten verstärkten Graphics Interchange Format (GIF) verwenden, um Ink in ihre HTML-Dokumente zu codieren. Weitere Informationen zu verstärkten GIFs finden Sie unter [Bausteine.](building-blocks.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Image<br/>                            | Für Anwendungen, für die es keine andere Schnittmenge der Kompatibilität gibt, sollte eine Freihandanwendung Bitmap- und Metadatei-formatierte Bilder in die Zwischenablage verschieben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Serialisiertes Freihandformat (Ink Serialized Format; ISF)<br/>      | Bei ISF handelt es sich um die kompakteste permanente Freihanddarstellung. Obwohl sie häufig nur Ink-Daten enthält, ist ISF erweiterbar. Anwendungen können benutzerdefinierte Attribute (identifiziert durch eine GUID (Globally Unique Identifier) für ein Ink-Objekt, einen [**Ink-Strich**](inkdisp-class.md) oder einen Ink-Punkt festlegen. Dadurch können Sie alle Arten von Daten oder Metadaten als Attribut in einem ISF-Stream speichern. Für die Interoperabilität der Zwischenablage kann Freihand in einen Standardmäßigen Zwischenablageslot für ISF platziert werden, der in den Headerdateien des Software Development Kits (SDK) definiert ist.<br/> ISF ist ein für Microsoft Tablet PC Technology spezifisches Format und wird nur in den [**Load-**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) und [**Save-Methoden**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save) des [**Ink-Objekts**](inkdisp-class.md) unterstützt.<br/> |
| RTF<br/>                              | Es ist möglich, ein RTF-Zwischenablageformat zu generieren und Freihand in der RTF als OLE-Objekte zu codieren. Dadurch kann die Ink-Datei in einen OLE-Container eingefügt werden, z. B. Microsoft Word oder eine RichEdit-basierte Anwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Extensible Markup Language (XML)<br/> | Anwendungen können eines der Base64-codierten Ink-Formate verwenden, um Ink in einem XML-Dateiformat zu speichern. Ein XML-Format ist nützlich für die Eingabe von Freihandinhalten in eine Datenbank, z. B. im Fall eines Signaturfelds oder sogar als primäres Anwendungsdateiformat. Dadurch entschärft sich die Notwendigkeit, einen Parser zu schreiben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

 

 




