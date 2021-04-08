---
title: Closedcaption-Objekt
description: Das closedcaption-Objekt bietet eine Möglichkeit zum Einschließen von Untertiteln mit einem Medien Clip. Der Beschriftungs Text befindet sich in einer synchronisierten, zugänglichen Medienaustausch Datei (Sami).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Closedcaption-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104038207"
---
# <a name="closedcaption-object"></a>Closedcaption-Objekt

Das **closedcaption** -Objekt bietet eine Möglichkeit zum Einschließen von Untertiteln mit einem Medien Clip. Der Beschriftungs Text befindet sich in einer synchronisierten, zugänglichen Medienaustausch Datei (Sami).

Das **closedcaption** -Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningid](closedcaption-captioningid.md)     | Gibt den Namen des Frames oder Steuer Elements an, in dem die Untertitel angezeigt werden, oder ruft ihn ab.                   |
| [Samifilename](closedcaption-samifilename.md)     | Gibt den Namen der Datei an, die die für den Untertitel erforderlichen Informationen enthält, oder ruft ihn ab. |
| [Samilang](closedcaption-samilang.md)             | Gibt die für Untertitel angezeigte Sprache an oder ruft diese ab.                                 |
| [Samilangcount](closedcaption-samilangcount.md)   | Ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.                                |
| [Samistyle](closedcaption-samistyle.md)           | Gibt den Beschriftungs Stil an oder ruft ihn ab.                                                  |
| [Samistylecount](closedcaption-samistylecount.md) | Ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.                                   |



 

Das **closedcaption** -Objekt unterstützt die folgenden Methoden.



| Methode                                                 | BESCHREIBUNG                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getsamilangid](closedcaption-getsamilangid.md)       | Ruft den Gebiets Schema Bezeichner (LCID) einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird. |
| [getsamilangname](closedcaption-getsamilangname.md)   | Ruft den Namen einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.                     |
| [getsamistylename](closedcaption-getsamistylename.md) | Ruft den Namen eines Stils ab, der von der aktuellen Sami-Datei unterstützt wird.                        |



 

Der Zugriff auf das **closedcaption** -Objekt erfolgt über die folgende Eigenschaft.



| Object                      | Eigenschaft                                  |
|-----------------------------|-------------------------------------------|
| [Player](player-object.md) | [closedcaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




