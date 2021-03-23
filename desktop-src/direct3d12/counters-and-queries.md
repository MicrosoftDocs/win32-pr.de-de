---
title: Zähler, Abfragen und prädikations
description: Stream Output-und UAV-Leistungsindikatoren werden in Direct3D 12 in einer ähnlichen Methode wie Direct3D 11 verwendet, obwohl der Arbeitsspeicher für die Leistungsindikatoren nun von der APP zugeordnet werden muss.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548738"
---
# <a name="counters-queries-and-predication"></a>Zähler, Abfragen und prädikations

In diesem Thema werden Datenstrom Ausgabe-Leistungsindikatoren, UAV-Leistungsindikatoren, Abfragen und das Prädikat behandelt.

Stream Output-und UAV-Leistungsindikatoren werden in Direct3D 12 in einer ähnlichen Methode wie Direct3D 11 verwendet, obwohl der Arbeitsspeicher für die Leistungsindikatoren nun von der APP zugeordnet werden muss. Abfragen in Direct3D 12 unterscheiden sich eher von denen in Direct3D 11, mit dem Hinzufügen von Zäunen und anderen Prozessen, die die Notwendigkeit einiger Abfrage Typen entfernen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                           | Beschreibung                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stream-ausgabezähler](stream-output-counters.md)<br/> | Die Streamausgabe ist die Fähigkeit der GPU, Vertices in einen Puffer zu schreiben. Der Status der Datenstrom-ausgabezähler Monitor.<br/>                                                               |
| [UAV-Leistungsindikatoren](uav-counters.md)<br/>                     | UAV-Leistungsindikatoren können verwendet werden, um einen atomaren 32-Bit-Zähler mit einer nicht geordneten Zugriffs Ansicht (UAV) zuzuordnen.<br/>                                                                                |
| [Abfragen](queries.md)<br/>                               | In Direct3D 12 werden Abfragen in Arrays von Abfragen gruppiert, die als Abfrage Heap bezeichnet werden. Ein Abfrage Heap weist einen Typ auf, der die gültigen Abfrage Typen definiert, die mit diesem Heap verwendet werden können.<br/> |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Leistungsmessung](performance-measurement.md)
</dt> </dl>

 

 





