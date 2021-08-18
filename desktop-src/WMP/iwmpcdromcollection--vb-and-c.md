---
title: IWMPCcollection -Schnittstelle (VB und C ) (Wmp.h)
description: Bietet eine Möglichkeit, eine Sammlung von CD- oder DVD-Laufwerken zu organisieren und darauf zu zugreifen. Die IWMPCcollection-Schnittstelle macht die folgende Eigenschaft verfügbar.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- IWMPCcollection-Schnittstelle (VB und C) Windows Media Player
- IWMPCcollection -Schnittstelle (VB und C) Windows Media Player , beschrieben
topic_type:
- apiref
api_name:
- IWMPCdromCollection (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c935d4875307c7712036ed51304996028db6ba2a88fc1d5e54c77b7948c72252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119299"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a>IWMPCcollection-Schnittstelle (VB und C#)

Bietet eine Möglichkeit, eine Sammlung von CD- oder DVD-Laufwerken zu organisieren und darauf zu zugreifen.

Die **IWMPCcollection-Schnittstelle** macht die folgende Eigenschaft verfügbar.

## <a name="members"></a>Member

Die **IWMPCcollection-Schnittstelle (VB und C#)** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPCcollection-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                                                     | Beschreibung                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**getByDriveSpecifier**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | Gibt eine **IWMPCface-Schnittstelle zurück,** die einem bestimmten Laufwerkbuchstaben zugeordnet ist.<br/> |
| [**Element**](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | Gibt eine **IWMPCführung-Schnittstelle** am angegebenen Index zurück.<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPCcollection-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                  | Zugriffstyp          | Beschreibung                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [**Count**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft die Anzahl der verfügbaren CD- und DVD-Laufwerke auf dem System ab.<br/> |



 

Verwenden Sie die folgende Eigenschaft, um eine **IWMPCcollection-Schnittstelle** zu erhalten.



| Object                                                                   | Eigenschaft                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**ccollection**](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPCführungsschnittstelle (VB und C#)**](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





