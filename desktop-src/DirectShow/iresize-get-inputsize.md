---
description: Die get \_ inputsize-Methode gibt die aktuelle Eingabe Größe des Filter Werts der Größenänderung zurück.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Iresize:: get_InputSize-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370810"
---
# <a name="iresizeget_inputsize-method"></a>Iresize:: get \_ inputsize-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `get_InputSize` -Methode gibt die aktuelle Eingabe Größe des Filter der Größenänderung zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piheight* \[ vorgenommen\]
</dt> <dd>

Empfängt die Höhe des Videos in Pixel.

</dd> <dt>

*piwidth* \[ vorgenommen\]
</dt> <dd>

Empfängt die Video Breite in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Eingabe-PIN des Filters nicht verbunden ist, wird ein Fehlercode zurückgegeben. Andernfalls wird die Breite und Höhe des Videos zurückgegeben, wie durch den Medientyp der Eingabe-PIN angegeben.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**Iresize-Schnittstelle**](iresize.md)
</dt> </dl>

 

 




