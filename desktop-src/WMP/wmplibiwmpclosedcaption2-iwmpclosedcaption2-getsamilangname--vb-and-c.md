---
title: IWMPClosedCaption2 getsamilangname-Methode
description: Die getsamilangname-Methode gibt den Namen einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- getsamilangname-Methode, Windows Media Player
- getsamilangname-Methode, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface Windows Media Player, getsamilangname-Methode
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
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367094"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>IWMPClosedCaption2:: getsamilangname-Methode

Die **getsamilangname** -Methode gibt den Namen einer Sprache zurück, die von der aktuellen Sami-Datei unterstützt wird.

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

*nIndex* \[ in\]
</dt> <dd>

**Ein System. Int32** -Wert, der der null basierte Index des abzurufenden sprach namens ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System. String** , bei der es sich um den Namen der Sprache handelt, wie in der Sami-Datei angegeben.

## <a name="remarks"></a>Bemerkungen

Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).

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

[**Iwmpclosedcaption. samilang (VB und c#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





