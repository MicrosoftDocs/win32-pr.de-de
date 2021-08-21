---
title: IWMPClosedCaption2 getSAMILangID-Methode
description: Die getSAMILangID-Methode gibt den Gebietsschemabezeichner (LCID) einer Sprache zurück, die von der aktuellen SAMI-Datei unterstützt wird.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- getSAMILangID-Methode Windows Media Player
- getSAMILangID-Methode Windows Media Player , IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2-Schnittstelle Windows Media Player , getSAMILangID-Methode
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
ms.openlocfilehash: a0fc62222f98d6c056bb8ce9ffd328582a6764202bb8446617471d3f7cb4a5ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506429"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>IWMPClosedCaption2::getSAMILangID-Methode

Die **getSAMILangID-Methode** gibt den Gebietsschemabezeichner (LCID) einer Sprache zurück, die von der aktuellen SAMI-Datei unterstützt wird.

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

*nIndex* \[ In\]
</dt> <dd>

Ein **System.Int32,** der der nullbasierte Index der abzurufenden LCID ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Int32,** das die LCID der Sprache mit dem angegebenen Index ist.

## <a name="remarks"></a>Hinweise

Die Sprachen in einer SAMI-Datei werden in der reihenfolge indiziert, die in der Datei angezeigt wird, beginnend mit 0 (null).

Diese Methode gibt 0 zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer.openState ist gleich 13).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





