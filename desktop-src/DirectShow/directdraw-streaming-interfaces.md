---
description: DirectDraw-Streamingschnittstellen
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: DirectDraw-Streamingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11e7eec0ec7ad82c0046b8c052ff00093b496c05495ec38590d201724d7620e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983050"
---
# <a name="directdraw-streaming-interfaces"></a>DirectDraw-Streamingschnittstellen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Sample Grabber-Filter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm zu erhalten.

 

Wenn Sie von DirectDraw unterstützte Videoformate in Ihren Streams verwenden, bieten Ihnen die folgenden Schnittstellen eine leistungsfähigere Kontrolle über die Daten als die generischeren Basisschnittstellen.



| Schnittstelle                                                  | BESCHREIBUNG                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Legt das Streamformat und das DirectDraw-Objekt fest, das dem Medienstream zugeordnet ist, und ruft es ab. diese Schnittstelle wird von [**IMediaStream ableiten.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) Sie können diese Schnittstelle auch verwenden, um Videobeispiele zu erstellen. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Ermöglicht das Anfügen von Videobeispielen an DirectDraw-Oberflächen. diese Schnittstelle wird von der [**IStreamSample-Schnittstelle**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) ableiten. Jede angefügte Oberfläche enthält ein Clippingrechteck, um das Rendering zu vereinfachen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Liste der Multimedia-Streamingschnittstellen](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



