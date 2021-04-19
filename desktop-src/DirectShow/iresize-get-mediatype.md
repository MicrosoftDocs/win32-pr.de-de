---
description: Die "get \_ MediaType"-Methode gibt den aktuellen Ausgabe Medientyp des resizerfilterfilters zurück.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'Iresize:: get_MediaType-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370317"
---
# <a name="iresizeget_mediatype-method"></a>Iresize:: get \_ mediaType-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `get_MediaType` -Methode gibt den aktuellen Ausgabe Medientyp des resizerfilterfilters zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine vom Aufrufer zugeordnete Objekt- [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur. Die-Methode füllt diese-Struktur mit dem Medientyp. Der Aufrufer muss ggf. den Format Block freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn der Ausgabe Medientyp nicht festgelegt wurde, wird ein Standard Medientyp zurückgegeben. Der Filter muss seinen Ausgabe Medientyp aktualisieren, wenn die Methoden **Put \_ mediaType** oder **Put \_ size** aufgerufen werden. der von zurückgegebene Medientyp `get_MediaType` muss diese Änderungen widerspiegeln.

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

 

 




