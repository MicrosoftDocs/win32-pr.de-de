---
description: DirectDraw-streamingschnittstellen
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: DirectDraw-streamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041217"
---
# <a name="directdraw-streaming-interfaces"></a>DirectDraw-streamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Wenn Sie von DirectDraw Unterstützte Videoformate in ihren Streams verwenden, erhalten Sie mit den folgenden Schnittstellen eine leistungsfähigere Kontrolle über die Daten als die allgemeineren Basis Schnittstellen.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Idirectdrawmediastream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Legt das Streamformat und das DirectDraw-Objekt fest, das dem Mediendaten Strom zugeordnet ist, und ruft es ab. Diese Schnittstelle wird von [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)abgeleitet. Sie können diese Schnittstelle auch zum Erstellen von Videobeispielen verwenden. |
| [**Idirectdrawstreamsample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Ermöglicht das Anfügen von Videobeispielen an DirectDraw-Oberflächen. Diese Schnittstelle wird von der [**istreamsample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) -Schnittstelle abgeleitet. Jede angefügte Oberfläche enthält ein Clippingrechteck, um das Rendering zu vereinfachen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Liste der Multimedia-streamingschnittstellen](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



