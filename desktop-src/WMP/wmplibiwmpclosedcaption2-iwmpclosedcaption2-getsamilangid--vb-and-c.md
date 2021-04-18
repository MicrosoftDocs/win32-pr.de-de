---
title: IWMPClosedCaption2 getsamilangid-Methode
description: Die getsamilangid-Methode gibt den Gebiets Schema Bezeichner (LCID) einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- getsamilangid-Methode, Windows-Media Player
- getsamilangid-Methode, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface, Windows Media Player, getsamilangid-Methode
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371521"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>IWMPClosedCaption2:: getsamilangid-Methode

Die **getsamilangid** -Methode gibt den Gebiets Schema Bezeichner (LCID) einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*nIndex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der null basierte Index der abzurufenden LCID ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Int32** , bei dem es sich um die LCID der Sprache mit dem angegebenen Index handelt.

## <a name="remarks"></a>Bemerkungen

Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).

Diese Methode gibt 0 zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).

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

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





