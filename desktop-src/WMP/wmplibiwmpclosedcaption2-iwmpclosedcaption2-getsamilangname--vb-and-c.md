---
title: IWMPClosedCaption2 getSAMILangName-Methode
description: Die getSAMILangName-Methode gibt den Namen einer Sprache zurück, die von der aktuellen SAMI-Datei unterstützt wird.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- getSAMILangName-Windows Media Player
- getSAMILangName-Methode Windows Media Player , IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2-Schnittstelle Windows Media Player , getSAMILangName-Methode
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99941c7c8c62480ea13572b22083a2d64bda9924cdf3d26200dbc9ac6ba9bdf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930303"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>IWMPClosedCaption2::getSAMILangName-Methode

Die **getSAMILangName-Methode** gibt den Namen einer Sprache zurück, die von der aktuellen SAMI-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*nIndex* \[ In\]
</dt> <dd>

**Ein System.Int32,** das der nullbasierte Index des abzurufenden Sprachnamens ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String-Datei,** die der Name der Sprache ist, wie in der SAMI-Datei angegeben.

## <a name="remarks"></a>Hinweise

Die Sprachen in einer SAMI-Datei werden in der Reihenfolge indiziert, die in der Datei angezeigt wird, beginnend mit 0 (null).

Diese Methode gibt eine Zeichenfolge der Länge 0 ("") zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer.openState ist gleich 13).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMILang (VB und C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





