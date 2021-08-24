---
title: IWMPClosedCaption2 getSAMIStyleName-Methode
description: Die getSAMIStyleName-Methode gibt den Namen eines Stils zurück, der von der aktuellen SAMI-Datei unterstützt wird.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- getSAMIStyleName-Windows Media Player
- getSAMIStyleName-Methode Windows Media Player , IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2-Schnittstelle Windows Media Player , getSAMIStyleName-Methode
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd599370afb9029a481fbae33264796232e4f129c1a5da0d2658452b785a870c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031350"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>IWMPClosedCaption2::getSAMIStyleName-Methode

Die **getSAMIStyleName-Methode** gibt den Namen eines Stils zurück, der von der aktuellen SAMI-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*nIndex* \[ In\]
</dt> <dd>

Ein **System.Int32,** das der nullbasierte Index des abzurufenden Formatnamens ist

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,die** den Namen des Stils wie in der SAMI-Datei angegeben ist.

## <a name="remarks"></a>Hinweise

Die Stile in einer SAMI-Datei werden in der Reihenfolge indiziert, die in der Datei angezeigt wird, beginnend mit 0 (null).

Diese Methode gibt eine Zeichenfolge der Länge 0 ("") zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer.openState ist gleich 13).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMIStyle (VB und C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





