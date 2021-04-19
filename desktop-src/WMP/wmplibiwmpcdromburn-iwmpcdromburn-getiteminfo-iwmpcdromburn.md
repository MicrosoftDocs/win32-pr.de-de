---
title: Iwmpcdromburn getiteminfo-Methode
description: Die getiteminfo-Methode ruft den Wert des angegebenen Attributs für die CD ab.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370189"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>Iwmpcdromburn:: getiteminfo-Methode

Die **getiteminfo** -Methode ruft den Wert des angegebenen Attributs für die CD ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstritem* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der einen der folgenden Werte enthält.



| Wert         | BESCHREIBUNG                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| Availabletime | Ruft die auf der CD verfügbare Zeit (in Sekunden) ab.                                          |
| Leer         | Ruft einen **System. Boolean** (dargestellt als Zeichenfolge) ab, der angibt, ob die CD leer ist. |
| FreeSpace     | Ruft den freien Speicherplatz auf der CD in Bytes ab.                                                |
| Totalspace    | Ruft den gesamten Speicherplatz auf der CD in Bytes ab.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. String** -Wert, der den Wert des angegebenen Attributs ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





