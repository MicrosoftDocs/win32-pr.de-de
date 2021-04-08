---
description: Basis-Multimedia-streamingschnittstellen
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Basis-Multimedia-streamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961222"
---
# <a name="base-multimedia-streaming-interfaces"></a>Basis-Multimedia-streamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Die grundlegenden Multimedia Streaming-Schnittstellen bieten eine programmgesteuerte Möglichkeit, auf multimediarestreams zuzugreifen. Wenn Sie jedoch eine Basisschnittstelle für den Zugriff auf einen bestimmten Datentyp verwenden, können Sie den Umfang der Kontrolle über die Daten einschränken, damit Medien Entwickler abgeleitete Versionen dieser Schnittstellen erstellen, die eine leistungsfähigere Kontrolle über die einzigartigen Funktionen Ihres Medientyps bieten.



| Schnittstelle                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Definiert, wie auf das Multimedia-Streamobjekt der höchsten Ebene zugegriffen wird. Dieses Objekt enthält und ermöglicht den Zugriff auf andere Streamobjekte. [**Imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) verfügt über Methoden, die bestimmte Streams auflisten oder abrufen, sowie das Überprüfen der Gesamtdauer des Streams und des Suchens innerhalb des Streams.                                                                                                       |
| [**Imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Definiert ein generisches Streamobjekt. Verwenden Sie die zugehörigen Methoden, um einen Zeiger auf den Stream abzurufen, Informationen zum Stream abzurufen und um Beispiele aus den Streamdaten zu erstellen. Sie können auch freigegebene streambeispiele erstellen, auf die mehrere Streams ohne Duplizierung der Beispiel Daten zugreifen können.                                                                                                                                                  |
| [**Istreamsample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Steuert das Verhalten eines bestimmten streambeispiels. Sie können den Stream, der das Beispiel erstellt hat, abrufen, die Start-und Endzeiten des Beispiels sowie den Abschluss Status überprüfen und eine benutzerdefinierte Funktion für das Beispiel selbst ausführen (über die [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) -Methode). In der Regel werden die Beispiel Daten von der Update-Methode ordnungsgemäß verarbeitet, z. b. beim Rendern von Videodaten oder beim Wiedergeben von Audiodaten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Liste der Multimedia-streamingschnittstellen](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



