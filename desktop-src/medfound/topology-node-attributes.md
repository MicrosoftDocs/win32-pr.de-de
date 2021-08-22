---
description: Topologieknotenattribute
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Topologieknotenattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd366c03607c4fc6646a09dae8571e6e4847a45b985f4996d28c15a828937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034668"
---
# <a name="topology-node-attributes"></a>Topologieknotenattribute

Die folgenden Attribute gelten für Topologieknoten.

## <a name="general-topology-node-attributes"></a>Allgemeine Topologieknotenattribute



| attribute                                                                       | Beschreibung                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ \_ CONNECT-METHODE**](mf-toponode-connect-method-attribute.md)   | Gibt an, wie das Topologieladeprogramm diesen Topologieknoten verbindet und ob dieser Knoten optional ist.                                                        |
| [**MF \_ \_ TOPONODE-DECODER**](mf-toponode-decoder-attribute.md)                  | Gibt an, ob das -Objekt eines Obersten Knotens ein Decoder ist.                                                                                                  |
| [**MF \_ TOPONODE \_ DECRYPTOR**](mf-toponode-decryptor-attribute.md)              | Gibt an, ob das zugrunde liegende Objekt eines obersten Knotens ein Entschlüsselungsobjekt ist.                                                                                     |
| [**MF \_ TOPONODE \_ DISCARDABLE**](mf-toponode-discardable-attribute.md)          | Gibt an, ob die Pipeline Beispiele aus einem Topologieknoten löschen kann.                                                                                    |
| [**MF \_ TOPONODE \_ ERROR \_ MAJORTYPE**](mf-toponode-error-majortype-attribute.md) | Enthält den Hauptmedientyp für einen Topologieknoten. Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, weil der richtige Decoder nicht gefunden wurde. |
| [**MF \_ TOPONODE \_ ERROR \_ SUBTYPE**](mf-toponode-error-subtype-attribute.md)     | Enthält den Medienuntertyp für einen Topologieknoten. Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, weil der richtige Decoder nicht gefunden wurde.    |
| [**MF \_ TOPONODE \_ ERRORCODE**](mf-toponode-errorcode-attribute.md)              | Enthält den Fehlercode des letzten Verbindungsfehlers für diesen Topologieknoten.                                                                  |
| [**MF \_ TOPONODE \_ LOCKED**](mf-toponode-locked-attribute.md)                    | Gibt an, ob die Medientypen auf diesem Topologieknoten geändert werden können.                                                                                  |
| [**MF \_ TOPONODE \_ MARKIN \_ HIER**](mf-toponode-markin-here-attribute.md)         | Gibt an, ob die Pipeline das Mark-In auf diesem Knoten anwendet.                                                                                             |
| [**MF \_ TOPONODE \_ MARKOUT \_ HIER**](mf-toponode-markout-here-attribute.md)       | Gibt an, ob die Pipeline mark-out auf diesen Knoten anwendet.                                                                                            |



 

## <a name="source-node-attributes"></a>Quellknotenattribute



| attribute                                                                                       | Beschreibung                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)                            | Gibt die Startzeit einer Präsentation relativ zum Start der Medienquelldatei in Einheiten von 100 Nanosekunden an. |
| [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)                              | Gibt die Beendigungszeit einer Präsentation relativ zum Starten der Medienquelldatei in Einheiten von 100 Nanosekunden an.  |
| [**MF \_ TOPONODE \_ PRESENTATION \_ DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) | Enthält einen Zeiger auf den Präsentationsdeskriptor für die Medienquelle.                                           |
| [**MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID**](mf-toponode-sequence-elementid-attribute.md)           | Gibt das Element an, das einen Quellknoten enthält.                                                                |
| [**MF \_ \_ TOPONODE-QUELLE**](mf-toponode-source-attribute.md)                                    | Enthält einen Zeiger auf die Medienquelle, die einem Topologieknoten zugeordnet ist.                                           |
| [**MF \_ TOPONODE \_ STREAM \_ DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md)             | Enthält einen Zeiger auf den Streamdeskriptor für die Medienquelle.                                                 |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ ID**](mf-toponode-workqueue-id-attribute.md)                       | Gibt eine Arbeitswarteschlange für einen Topologieknoten an.                                                                       |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS-KLASSE \_**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Gibt einen MMCSS-Task (Multimedia Class Scheduler Service) für einen Topologieknoten an.                                  |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Gibt einen MMCSS-Taskbezeichner für einen Topologieknoten an.                                                            |



 

## <a name="transform-node-attributes"></a>Transformieren von Knotenattributen



| attribute                                                                             | Beschreibung                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | Gibt an, ob die einem Topologieknoten zugeordnete Transformation DirectX Video Acceleration (DXVA) unterstützt. |
| [**MF \_ TOPONODE \_ DRAIN**](mf-toponode-drain-attribute.md)                            | Gibt an, wann eine Transformation entladen wird.                                                                     |
| [**MF \_ TOPONODE \_ FLUSH**](mf-toponode-flush-attribute.md)                            | Gibt an, wann eine Transformation geleert wird.                                                                     |
| [**MF \_ TOPONODE \_ TRANSFORM \_ OBJECTID**](mf-toponode-transform-objectid-attribute.md) | Der Klassenbezeichner (CLSID) der Transformation, die diesem Topologieknoten zugeordnet ist.                          |



 

## <a name="output-node-attributes"></a>Ausgabeknotenattribute



| attribute                                                                                  | Beschreibung                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ DISABLE \_ PREROLL**](mf-toponode-disable-preroll-attribute.md)            | Gibt an, ob die Mediensitzung die Vorrolle für die Mediensenke verwendet, die von diesem Topologieknoten dargestellt wird.            |
| [**MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) | Gibt an, ob die Mediensitzung die Mediensenke herunterfährt, wenn der Ausgabeknoten aus der Topologie entfernt wird. |
| [**MF \_ TOPONODE \_ RATELESS**](mf-toponode-rateless-attribute.md)                           | Gibt an, ob die diesem Topologieknoten zugeordnete Mediensenke ratenlos ist.                                 |
| [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md)                           | Der Streambezeichner der Streamsenke, die diesem Topologieknoten zugeordnet ist.                                     |



 

## <a name="tee-node-attributes"></a>Tee-Knotenattribute



| attribute                                                                  | Beschreibung                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**MF \_ TOPONODE \_ PRIMARYOUTPUT**](mf-toponode-primaryoutput-attribute.md) | Gibt an, welche Ausgabe die primäre Ausgabe auf einem Teeknoten ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 



