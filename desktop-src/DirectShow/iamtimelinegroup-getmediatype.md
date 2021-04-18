---
description: Die getmediatype-Methode ruft den unkomprimierten Medientyp für die Gruppe ab.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'Iamtimelinegroup:: getmediatype-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365840"
---
# <a name="iamtimelinegroupgetmediatype-method"></a>Iamtimelinegroup:: getmediatype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetMediaType` Methode ruft den unkomprimierten Medientyp für die Gruppe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PMT* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die mit dem Medientyp gefüllt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss den Format Block des zurückgegebenen Medientyps freigeben, der im **pbformat** -Member der zurückgegebenen \_ \_ Medientyp-Struktur angegeben ist. Sie können die Hilfsfunktion " [**fremediatype**](freemediatype.md) " aus der Basisklassen Bibliothek verwenden.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinegroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




