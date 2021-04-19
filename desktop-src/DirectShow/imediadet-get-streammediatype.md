---
description: Die get \_ streammediatype-Methode ruft den Medientyp des aktuellen Streams ab. Alle Videostreams werden in videoinfoheader-Typen konvertiert, und alle Audiodatenströme werden in WaveFormatEx-Typen konvertiert.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'Imediadet:: get_StreamMediaType-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373936"
---
# <a name="imediadetget_streammediatype-method"></a>Imediadet:: get \_ streammediatype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_StreamMediaType` Methode ruft den Medientyp des aktuellen Streams ab. Alle Videostreams werden in [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Typen konvertiert, und alle Audiodatenströme werden in [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Typen konvertiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die mit dem Medientyp gefüllt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.

Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück. Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).

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

[**Imediadet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 
