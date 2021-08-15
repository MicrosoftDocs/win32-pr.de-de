---
description: Die get \_ MediaType-Methode gibt den aktuellen Ausgabemedientyp des Resizerfilters zurück.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: IResize::get_MediaType-Methode (Qedit.h)
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
ms.openlocfilehash: d9e23c78a25f1cda141cb0c3ce55688c12bdf3aab447aca596326e01544b4e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818231"
---
# <a name="iresizeget_mediatype-method"></a>IResize::get \_ MediaType-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_MediaType` -Methode gibt den aktuellen Ausgabemedientyp des Größenfilters zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmt* \[ out\]
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die vom Aufrufer zugeordnet wird. Die -Methode füllt diese Struktur mit dem Medientyp auf. Der Aufrufer muss den Formatblock (sofern verfügbar) frei geben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn der Ausgabemedientyp nicht festgelegt wurde, geben Sie einen Standardmedientyp zurück. Der Filter muss seinen Ausgabemedientyp aktualisieren, wenn die **Put \_ MediaType-** oder **put \_ Size-Methoden** aufgerufen werden. Der von zurückgegebene Medientyp muss `get_MediaType` diese Änderungen widerspiegeln.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9.0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IResize-Schnittstelle**](iresize.md)
</dt> </dl>

 

 




