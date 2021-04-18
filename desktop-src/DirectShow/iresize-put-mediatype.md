---
description: Die Put \_ mediaType-Methode legt den Ausgabe Medientyp für den Filter zum Ändern der Größe fest.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: Iresize::p ut_MediaType-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364921"
---
# <a name="iresizeput_mediatype-method"></a>Iresize::p UT \_ mediaType-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_MediaType` Methode legt den Ausgabe Medientyp für den Filter zum Ändern der Größe fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* \[ in\]
</dt> <dd>

Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Des ruft diese Methode auf, bevor eine Verbindung mit der Ausgabe-PIN des Filters hergestellt wird. Verwenden Sie den Medientyp als Medientyp der Ausgabepin. Geben Sie diesen Medientyp in der [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode zurück, und überprüfen Sie diesen Typ in der [**ctransformfilter:: checktransform**](ctransformfilter-checktransform.md) -Methode. Des ruft diese Methode niemals auf, nachdem die Ausgabe-PIN verbunden ist.

Derzeit legt des den Ausgabe Medientyp auf ein unkomprimiertes RGB-Format mit einem **videoinfoheader** -Format Block (Formattyp ist gleich Format \_ videoinfo) fest. Der Untertyp ist möglicherweise mediasubtype \_ ARGB32, womit 32-Bit-RGB mit einem Alphakanal angegeben wird.

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

 

 




