---
title: IWMPClosedCaption2 getsamistylename-Methode
description: Die getsamistylename-Methode gibt den Namen eines Stils zurück, der von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- getsamistylename-Methode, Windows Media Player
- getsamistylename-Methode, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface Windows Media Player, getsamistylename-Methode
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
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367093"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>IWMPClosedCaption2:: getsamistylename-Methode

Die **getsamistylename** -Methode gibt den Namen eines Stils zurück, der von der aktuellen Sami-Datei unterstützt wird.

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

*nIndex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der null basierte Index des abzurufenden Format namens ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System. String** , bei der es sich um den Namen des Stils handelt, der in der Sami-Datei angegeben ist.

## <a name="remarks"></a>Bemerkungen

Die Stile in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).

Diese Methode gibt eine Zeichenfolge der Länge 0 (null) zurück (""), es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).

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

[**Iwmpclosedcaption-Schnittstelle (VB und c#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Iwmpclosedcaption. samistyle (VB und c#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





