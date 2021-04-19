---
title: Iwmpmediacollection getmediaatom-Methode
description: Die getmediaatom-Methode gibt den Index eines angegebenen Attributs innerhalb des Satzes verfügbarer Attribute zurück.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- getmediaatom-Methode, Windows-Media Player
- getmediaatom-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection Interface, Windows Media Player, getmediaatom-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367196"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>Iwmpmediacollection:: getmediaatom-Methode

Die- `getMediaAtom` Methode gibt den Index eines angegebenen Attributs innerhalb des Satzes verfügbarer Attribute zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstritemname* \[ in\]
</dt> <dd>

**System. String** der Name des Elements, für das der Index abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der **System. Int32** -Wert, der der Index ist.

## <a name="remarks"></a>Bemerkungen

Die mit dieser Methode abgerufene Indexnummer kann an das **iwmpmedia. getiteminfobyatom** -Element übermittelt werden, um auf Attributwerte zuzugreifen. Diese Technik ist in der Regel effizienter, wenn Sie mit großen Wiedergabelisten arbeiten als der Zugriff auf einen Attribut Wert über " **iwmpmedia. getiteminfo**".

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmedia. getiteminfo (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia. getiteminfobyatom (VB und c#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





