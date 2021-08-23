---
description: Multimedia-Streamingfehler und Erfolgscodes
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Multimedia-Streamingfehler und Erfolgscodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d1a943ed4d41acd712ad19680e896df33b3afe2ed733bad86a129e2993e6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952199"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Multimedia-Streamingfehler und Erfolgscodes

> [!Note]  
> Diese API ist veraltet. Neue Anwendungen sollten sie nicht verwenden.

 

Die folgende Liste enthält Fehlermeldungen und Erfolgsbenachrichtigungen für Anwendungen, die die Multimediastreamingschnittstellen verwenden. Diese Liste enthält nicht alle möglichen Fehler. Die angezeigten Fehler gelten speziell für die Microsoft® DirectShow®implementierung der Multimediastreamingschnittstellen.



| Wert                       | Hexadezimalcode | Beschreibung                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ PENDING              | 0x00040001       | Das Beispielupdate ist noch nicht abgeschlossen.                                                                                                                                                         |
| MS \_ S \_ NOUPDATE             | 0x00040002       | Das Beispiel wurde nach dem erzwungenen Abschluss nicht aktualisiert.                                                                                                                                            |
| MS \_ S \_ ENDOFSTREAM          | 0x00040003       | Ende des Streams. Beispiel nicht aktualisiert.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | Ein [**IMediaStream-Objekt**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) konnte nicht aus einem [**IMultiMediaStream-Objekt**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) entfernt werden, da es immer noch mindestens ein zugeordnetes Beispiel enthält. |
| MS \_ E \_ PURPOSEID            | 0x80040402       | Die angegebene Zweck-ID kann nicht für den Aufruf verwendet werden.                                                                                                                                       |
| MS \_ E \_ NOSTREAM             | 0x80040403       | Mit den angegebenen Attributen kann kein Stream gefunden werden.                                                                                                                                      |
| MS \_ \_ E-VERKNUNG            | 0x80040404       | Die Suche wird für dieses [**IMultiMediaStream-Objekt nicht**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) unterstützt.                                                                                                      |
| MS \_ E \_ INCOMPATIBLE         | 0x80040405       | Die Streamformate sind nicht kompatibel.                                                                                                                                                     |
| MS \_ E \_ BUSY                 | 0x80040406       | Das Beispiel ist ausgelastet.                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | Das -Objekt kann den Aufruf nicht akzeptieren, da seine initialisierte Funktion oder entsprechung nicht aufgerufen wurde.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | Die Quelle ist bereits definiert.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | Der Streamtyp ist für diesen Vorgang ungültig.                                                                                                                                           |
| MS \_ E \_ NOTRUNNING           | 0x8004040A       | Das [**IMultiMediaStream-Objekt**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) befindet sich nicht im Ausführungszustand.                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multimediastreaming](multimedia-streaming.md)
</dt> </dl>

 

 



