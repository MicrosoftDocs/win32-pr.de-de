---
title: Formate
description: Formate
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Medienformat-SDK, Eingaben
- Windows Medienformat-SDK,Streams
- Windows Medienformat-SDK, Ausgaben
- Windows Medienformat-SDK, Formate
- Advanced Systems Format (ASF), Eingaben
- ASF (Advanced Systems Format), Eingaben
- Advanced Systems Format (ASF),streams
- ASF (Advanced Systems Format), Streams
- Advanced Systems Format (ASF), Ausgaben
- ASF (Advanced Systems Format), Ausgaben
- Advanced Systems Format (ASF),formats
- ASF (Advanced Systems Format), Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f217b9935926d7bd7d5cba9ac53e6834385685e4a0f87ea6ba713cc8ff70b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089690"
---
# <a name="formats"></a>Formate

Die Informationen in einem Format beschreiben alles, was Sie über einen bestimmten Medientyp wissen müssen. Jedes Format hat einen Haupttyp wie Audio oder Video und kann einen Untertyp haben. Formate enthalten je nach Haupttyp unterschiedliche Informationen. Audio- und Videoformate erfordern viel mehr Informationen als andere Typen.

Genau wie die Objekte des Windows Media Format SDK zwischen Eingabenummern, Datenstromnummern und Ausgabenummern unterscheiden (siehe [Eingaben, Streams](inputs-streams-and-outputs.md)und Ausgaben), gibt es wichtige Unterschiede zwischen Eingabeformaten, Streamformaten und Ausgabeformaten. Diese Unterschiede werden hier beschrieben:

## <a name="input-formats"></a>Eingabeformate

Ein Eingabeformat beschreibt die digitalen Medien, die Sie an das Writer-Objekt übergeben. Wenn ein Stream in einer ASF-Datei mit einem Codec komprimiert wird, unterstützt der Codec nur bestimmte Eingabeformate. Wenn Sie die Windows Medienaudio- und Videocodecs verwenden, können Sie die unterstützten Eingabeformate mithilfe des Writer-Objekts aufzählen. Beim Schreiben einer Datei sind Sie dafür verantwortlich, ein Eingabeformat auszuwählen, das Ihren Eingabemedien entspricht.

Obwohl das Format der Eingabemedien vom Codec unterstützt werden muss, der die Daten komprimiert, müssen einige Eingabeformateinstellungen nicht mit dem Streamformat übereinstimmen. Beispielsweise kann das Eingabeformat für einen Videostream eine Framegröße haben, die sich von der im Streamformat definierten Größe unterscheiden kann. In diesen Fällen führt der Codec Konvertierungen durch.

## <a name="stream-formats"></a>Streamformate

Ein Streamformat beschreibt die Form des Mediums, wie es in der ASF-Datei gespeichert wird. Das Streamformat ist das im Profil beschriebene Format und kann mit dem Eingabe- und Ausgabeformat identisch sein. Wenn ein Codec verwendet wird, um die Daten in einem Stream zu komprimieren, ist das Streamformat anders als das Eingabe- und Ausgabeformat.

Wenn Sie die Codecs Windows Media Audio und Video verwenden, müssen Sie eine Liste der unterstützten Streamformate aus dem Codec abrufen, um sicherzustellen, dass Sie nicht versuchen, ein Format anzugeben, das der Code nicht unterstützt. Einige Formateinstellungen, z. B. die Größe und Farbtiefe eines Videoframes, müssen manuell konfiguriert werden, nachdem das Codecformat abgerufen wurde.

## <a name="output-formats"></a>Ausgabeformate

Ein Ausgabeformat beschreibt die digitalen Medien, die der Reader (oder synchroner Reader) an Ihre Anwendung übergibt. Wenn ein Stream in einer ASF-Datei mit einem Codec komprimiert wird, unterstützt der Codec nur bestimmte Ausgabeformate. Wenn Sie die Windows Medienaudio- und Videocodecs verwenden, können Sie die unterstützten Ausgabeformate mithilfe des Readerobjekts aufzählen. Jeder der Windows Mediencodecs hat ein Standardausgabeformat, Sie können jedoch ein beliebiges unterstütztes Ausgabeformat für die Beispielbereitstellung auswählen.

Obwohl das Ausgabemedienformat vom Codec unterstützt werden muss, der die Daten komprimiert hat, müssen einige Ausgabeformateinstellungen nicht mit dem Streamformat übereinstimmen. Beispielsweise kann das Ausgabeformat für einen Videostream eine Framegröße haben, die sich von der im Streamformat definierten Größe unterscheiden kann. In diesen Fällen führt der Codec Konvertierungen durch.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> </dl>

 

 




