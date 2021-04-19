---
title: Iwmplibrary (VB und C)-Schnittstelle (WMP. h)
description: Stellt eine Bibliothek dar. Die iwmplibrary-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 956b2da1-5f01-48d6-8faa-e360c225afda
keywords:
- Windows Media Player der iwmplibrary (VB und C)-Schnittstelle
- Windows Media Player der iwmplibrary (VB und C), beschrieben
topic_type:
- apiref
api_name:
- IWMPLibrary (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9749d3a2363c3863180639f249d7261ec1b9694
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371240"
---
# <a name="iwmplibrary-vb-and-c-interface"></a>Iwmplibrary (VB und c#)-Schnittstelle

Stellt eine Bibliothek dar.

Die **iwmplibrary** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmplibrary (VB und c#)** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmplibrary (VB und c#)** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                                           |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**isidentical**](wmplibiwmplibrary-iwmplibrary-isidentical--vb-and-c.md) | Gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iwmplibrary (VB und c#)** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp          | BESCHREIBUNG                                                                   |
|:----------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)<br/> | Schreibgeschützt<br/> | Ruft eine **iwmpmediacollection** -Schnittstelle für die aktuelle Bibliothek ab.<br/> |
| [**Benennen**](wmplibiwmplibrary-iwmplibrary-name--vb-and-c.md)<br/>                       | Schreibgeschützt<br/> | Ruft den anzeigen amen der aktuellen Bibliothek ab.<br/>                      |
| [**Sorte**](wmplibiwmplibrary-iwmplibrary-type--vb-and-c.md)<br/>                       | Schreibgeschützt<br/> | Ruft einen Wert ab, der den Bibliothekstyp angibt.<br/>                      |



 

Verwenden Sie die folgende Methode, um eine **iwmplibrary** -Schnittstelle zu erhalten.



| Object                                                   | Eigenschaft                                                         |
|----------------------------------------------------------|------------------------------------------------------------------|
| [Iwmplibraryservices](iwmplibraryservices--vb-and-c.md) | [**getlibrarybytype**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmplibraryservices. getlibrarybytype (VB und c#)**](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md)
</dt> </dl>

 

 





