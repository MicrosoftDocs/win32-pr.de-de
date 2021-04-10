---
description: Topologieknotenattribute
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Topologieknotenattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959369"
---
# <a name="topology-node-attributes"></a>Topologieknotenattribute

Die folgenden Attribute gelten für topologieknoten.

## <a name="general-topology-node-attributes"></a>Attribute der allgemeinen topologieknoten



| Attribut                                                                       | BESCHREIBUNG                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ toponode \_ Connect- \_ Methode**](mf-toponode-connect-method-attribute.md)   | Gibt an, wie der topologielader diesen topologieknoten verbindet und ob dieser Knoten optional ist.                                                        |
| [**MF- \_ toponode- \_ Decoder**](mf-toponode-decoder-attribute.md)                  | Gibt an, ob das Objekt eines topologiedjeders ein Decoder ist.                                                                                                  |
| [**MF- \_ toponode- \_ Entschlüsselung**](mf-toponode-decryptor-attribute.md)              | Gibt an, ob das zugrunde liegende Objekt eines topologieknotens eine Entschlüsselung ist.                                                                                     |
| [**MF- \_ toponode- \_ verwerfen**](mf-toponode-discardable-attribute.md)          | Gibt an, ob die Pipeline Beispiele von einem topologieknoten ablegen kann.                                                                                    |
| [**MF- \_ toponode- \_ Fehler \_ majortype**](mf-toponode-error-majortype-attribute.md) | Enthält den Haupt Medientyp für einen topologieknoten. Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte. |
| [**MF- \_ toponode- \_ \_ Fehleruntertyp**](mf-toponode-error-subtype-attribute.md)     | Enthält den Medien Untertyp für einen topologieknoten. Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte.    |
| [**MF- \_ toponode- \_ ErrorCode**](mf-toponode-errorcode-attribute.md)              | Enthält den Fehlercode des letzten Verbindungsfehlers für diesen topologieknoten.                                                                  |
| [**MF- \_ toponode \_ gesperrt**](mf-toponode-locked-attribute.md)                    | Gibt an, ob die Medientypen für diesen topologieknoten geändert werden können.                                                                                  |
| [**Hier finden Sie ein MF- \_ toponode- \_ Markin \_**](mf-toponode-markin-here-attribute.md)         | Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.                                                                                             |
| [**MF \_ toponode \_ markout \_ hier**](mf-toponode-markout-here-attribute.md)       | Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.                                                                                            |



 

## <a name="source-node-attributes"></a>Quellknoten Attribute



| Attribut                                                                                       | BESCHREIBUNG                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MF \_ toponode \_ mediastart**](mf-toponode-mediastart-attribute.md)                            | Gibt die Startzeit einer Präsentation in Relation zum Start der Medien Quelldatei in 100-Nanosecond-Einheiten an. |
| [**MF- \_ toponode- \_ mediastop**](mf-toponode-mediastop-attribute.md)                              | Gibt die Endzeit einer Präsentation in 100-Nanosecond-Einheiten relativ zum Start der Medien Quelldatei an.  |
| [**MF- \_ toponode- \_ Präsentations \_ Deskriptor**](mf-toponode-presentation-descriptor-attribute.md) | Enthält einen Zeiger auf den Präsentations Deskriptor für die Medienquelle.                                           |
| [**Element-ID der MF \_ -toponode \_ \_ -Sequenz**](mf-toponode-sequence-elementid-attribute.md)           | Gibt das Element an, das einen Quellknoten enthält.                                                                |
| [**MF- \_ toponode- \_ Quelle**](mf-toponode-source-attribute.md)                                    | Enthält einen Zeiger auf die Medienquelle, die einem topologieknoten zugeordnet ist.                                           |
| [**MF- \_ toponode-Daten \_ Strom \_ Deskriptor**](mf-toponode-stream-descriptor-attribute.md)             | Enthält einen Zeiger auf den Datenstrom Deskriptor für die Medienquelle.                                                 |
| [**MF- \_ toponode- \_ workwarteschlangen- \_ ID**](mf-toponode-workqueue-id-attribute.md)                       | Gibt eine Arbeits Warteschlange für einen topologieknoten an.                                                                       |
| [**MF \_ toponode \_ workqueue \_ MMCSS- \_ Klasse**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Gibt eine MMCSS-Aufgabe (Multimedia Class Scheduler Service) für einen topologieknoten an.                                  |
| [**MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Gibt einen MMCSS-Task Bezeichner für einen topologieknoten an.                                                            |



 

## <a name="transform-node-attributes"></a>Knoten Attribute transformieren



| Attribut                                                                             | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MF- \_ toponode \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | Gibt an, ob die einem topologieknoten zugeordnete Transformation die DirectX-Video Beschleunigung (DXVA) unterstützt. |
| [**MF- \_ toponode- \_ Ableitung**](mf-toponode-drain-attribute.md)                            | Gibt an, wann eine Transformation entladen wird.                                                                     |
| [**MF- \_ toponode-Leerung \_**](mf-toponode-flush-attribute.md)                            | Gibt an, wann eine Transformation geleert wird.                                                                     |
| [**MF \_ toponode \_ Transform \_ objectID**](mf-toponode-transform-objectid-attribute.md) | Der Klassen Bezeichner (CLSID) der diesem topologieknoten zugeordneten Transformation.                          |



 

## <a name="output-node-attributes"></a>Ausgabe Knoten Attribute



| Attribut                                                                                  | BESCHREIBUNG                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF- \_ toponode \_ Deaktivieren von \_ Preroll**](mf-toponode-disable-preroll-attribute.md)            | Gibt an, ob die Medien Sitzung vorab auf der Medien Senke, die durch diesen topologieknoten dargestellt wird, verwendet wird.            |
| [**MF \_ toponode \_ noshutdown \_ beim \_ Entfernen**](mf-toponode-noshutdown-on-remove-attribute.md) | Gibt an, ob die Medien Sitzung beim Entfernen des Ausgabe Knotens aus der Topologie von der Medien-Senke heruntergefahren wird. |
| [**MF- \_ toponode- \_ Rate**](mf-toponode-rateless-attribute.md)                           | Gibt an, ob die Medien Senke, die diesem topologieknoten zugeordnet ist, ratlos ist.                                 |
| [**MF- \_ toponode- \_ streamid**](mf-toponode-streamid-attribute.md)                           | Der Datenstrom Bezeichner der Stream-Senke, die diesem topologieknoten zugeordnet ist.                                     |



 

## <a name="tee-node-attributes"></a>Tee-Knoten Attribute



| Attribut                                                                  | BESCHREIBUNG                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**MF \_ toponode \_ primaryoutput**](mf-toponode-primaryoutput-attribute.md) | Gibt an, welche Ausgabe die primäre Ausgabe auf einem Tee-Knoten ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 



