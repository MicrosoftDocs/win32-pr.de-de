---
description: Medienquellen Ereignisse
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Medienquellen Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363036"
---
# <a name="media-source-events"></a>Medienquellen Ereignisse

In diesem Thema werden die Ereignisse aufgelistet, die von Medienquellen und Mediendaten strömen gesendet werden. Medienquellen können auch benutzerdefinierte, hier nicht aufgelistete Ereignisse senden.

## <a name="media-source-events"></a>Medienquellen Ereignisse



| Ereignis                                                                      | BESCHREIBUNG                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Meendof Presentation-Ereignis](meendofpresentation.md)                       | Die Präsentation wurde beendet. Alle Streams in der Präsentation haben das Ende des Streams erreicht.      |
| [Menewstream-Ereignis](menewstream.md)                                       | Es wurde ein neuer Datenstrom erstellt. Das Ereignis enthält einen Zeiger auf den Stream.                            |
| [Mesourcecharakteristicschge-Ereignis](mesourcecharacteristicschanged.md) | Die Merkmale der Quelle wurden geändert. (Optional.)                                      |
| [MESourceMetadataChanged-Ereignis](mesourcemetadatachanged.md)               | Die Metadaten der Quelle wurden geändert. (Optional.)                                                   |
| [Mesourcepaused-Ereignis](mesourcepaused.md)                                 | Die Quelle wurde angehalten. Nicht alle Quellen unterstützen das Anhalten.                                          |
| [Mesourceratechanged-Ereignis](mesourceratechanged.md)                       | Die Wiedergabe Rate der Quelle wurde geändert. (Optional; gilt, wenn die Quelle Raten Kontrolle unterstützt.) |
| [Mesourceratechangerequnost-Ereignis](mesourceratechangerequested.md)       | Die Quelle fordert eine neue Wiedergabe Rate an. (Optional.)                                        |
| [Mesourceseeked-Ereignis](mesourceseeked.md)                                 | Die Quelle wurde im Seeding angezeigt. Nicht alle Quellen unterstützen Suchvorgänge.                                          |
| [Mesourcestarted-Ereignis](mesourcestarted.md)                               | Die Quelle wurde gestartet.                                                                          |
| [Mesourcestpt-Ereignis](mesourcestopped.md)                               | Die Quelle wurde beendet.                                                                          |
| [Meupdatedstream-Ereignis](meupdatedstream.md)                               | Ein vorhandener Stream wurde Seeding oder neu gestartet. Das Ereignis enthält einen Zeiger auf den Stream.         |



 

## <a name="media-stream-events"></a>Medienstrom Ereignisse



| Ereignis                                                    | BESCHREIBUNG                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Meendof Stream-Ereignis](meendofstream.md)                 | Der Stream wurde beendet.                                                                                                              |
| [Meerror-Ereignis](meerror.md)                             | Beim Streaming ist ein Fehler aufgetreten. Verwenden Sie dieses Ereignis für Fehler, die nicht mit einem der anderen hier aufgeführten Ereignisse verknüpft sind. |
| [Memediasample-Ereignis](memediasample.md)                 | Der Stream hat ein neues Beispiel generiert.                                                                                         |
| [Mestreamformatchanged-Ereignis](mestreamformatchanged.md) | Der Medientyp wurde geändert. (Optional.)                                                                                        |
| [Mestreampaused-Ereignis](mestreampaused.md)               | Der Stream wurde angehalten.                                                                                                         |
| [Mestreamseeked-Ereignis](mestreamseeked.md)               | Der Stream wurde im Seeding angezeigt.                                                                                                         |
| [Mestreamstarted-Ereignis](mestreamstarted.md)             | Der Stream wurde gestartet.                                                                                                        |
| [Mestreambeendete-Ereignis](mestreamstopped.md)             | Der Stream wurde beendet.                                                                                                        |
| [Mestreamthinmode-Ereignis](mestreamthinmode.md)           | Der thiningmodus wurde gestartet oder beendet. (Optional.)                                                                              |
| [Mestreamtick-Ereignis](mestreamtick.md)                   | Der Stream weist eine Lücke auf. (Optional.)                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen](media-sources.md)
</dt> </dl>

 

 



