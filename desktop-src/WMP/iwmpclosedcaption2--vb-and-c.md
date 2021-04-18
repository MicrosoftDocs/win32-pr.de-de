---
title: IWMPClosedCaption2-Schnittstelle (VB und C) (WMP. h)
description: Stellt Eigenschaften und Methoden für Untertitel bereit, die die iwmpclosedcaption-Schnittstelle ergänzen. Zusätzlich zu den Eigenschaften, die von iwmpclosedcaption geerbt werden, macht die IWMPClosedCaption2-Schnittstelle die folgenden Eigenschaften verfügbar.
ms.assetid: e34ea819-dc1a-48f3-9e55-cf2217379ddb
keywords:
- IWMPClosedCaption2 (VB und C) Interface Windows Media Player
- IWMPClosedCaption2 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPClosedCaption2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dbf81cef3734a6466b6fd177ccc87a38c5c7085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364972"
---
# <a name="iwmpclosedcaption2-vb-and-c-interface"></a>IWMPClosedCaption2-Schnittstelle (VB und c#)

Stellt Eigenschaften und Methoden für Untertitel bereit, die die **iwmpclosedcaption** -Schnittstelle ergänzen.

Zusätzlich zu den Eigenschaften, die von **iwmpclosedcaption** geerbt werden, macht die **IWMPClosedCaption2** -Schnittstelle die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die IWMPClosedCaption2-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die IWMPClosedCaption2-Schnittstelle **(VB und c#)** verfügt über diese Methoden.



| Methode                                                                                             | BESCHREIBUNG                                                                                       |
|:---------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| [**getsamilangid**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangid--vb-and-c.md)       | Gibt den Gebiets Schema Bezeichner (LCID) einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.<br/> |
| [**getsamilangname**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)   | Gibt den Namen einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.<br/>                     |
| [**getsamistylename**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md) | Gibt den Namen eines Stils zurück, der von der aktuellen Sami-Datei unterstützt wird.<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die IWMPClosedCaption2-Schnittstelle **(VB und c#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                                | Zugriffstyp           | BESCHREIBUNG                                                                         |
|:--------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------|
| [**Samilangcount**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-samilangcount--vb-and-c.md)<br/> | Lesen/Schreiben<br/> | Ruft die Anzahl der von der aktuellen satextdatei unterstützten Sprachen ab oder legt Sie fest.<br/> |
| [**Samistylecount**](wmplibiwmpclosedcaption2-samistylecount.md)<br/>                            | Lesen/Schreiben<br/> | Ruft die Anzahl der von der aktuellen satextdatei unterstützten Stile ab oder legt Sie fest.<br/>    |



 

Sie erhalten eine **IWMPClosedCaption2** -Schnittstelle durch Umwandeln des Werts, der von der [**AxWindowsMediaPlayer. closedcaption**](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) -Eigenschaft zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmpclosedcaption-Schnittstelle (VB und c#)**](iwmpclosedcaption--vb-and-c.md)
</dt> </dl>

 

 





