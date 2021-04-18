---
description: Die get \_ Streamtype-Methode ruft die Globally Unique Identifier (GUID) für den Medientyp des aktuellen Streams ab.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Imediadet:: get_StreamType-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361445"
---
# <a name="imediadetget_streamtype-method"></a>Imediadet:: get \_ Streamtype-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_StreamType` Methode ruft die Globally Unique Identifier (GUID) für den Medientyp des aktuellen Streams ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt die GUID des Haupt Typs für den Medientyp.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft den **majortype** -Member der Struktur des [**am- \_ Medien \_ Typs**](/windows/win32/api/strmif/ns-strmif-am_media_type) ab. Die **am \_ Medientyp \_** -Struktur beschreibt das Format des Streams, und der **majortype** -Member ist eine GUID, die die allgemeine Kategorie angibt, z. b. Audiodaten oder Videos. Bei einem Videostream ist die GUID MediaType \_ Video. Bei Audiodaten handelt es sich um MediaType \_ -Audiodaten. Um die gesamte **\_ \_ Medientyp** Struktur abzurufen, rufen Sie die [**imediadet:: get \_ streammediatype**](imediadet-get-streammediatype.md) -Methode auf.

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

 

 




