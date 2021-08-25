---
description: Die \_ get StreamTypeB-Methode ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: IMediaDet::get_StreamTypeB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8fc424a6fcbba4450980e389b88878d019d7e82a40bb42e11ce29097c254123c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083710"
---
# <a name="imediadetget_streamtypeb-method"></a>IMediaDet::get \_ StreamTypeB-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `get_StreamTypeB` -Methode ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt eine Zeichenfolgendarstellung des Medientyps GUID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Der zurückgegebene **BSTR** ist wie folgt formatiert: `{73647561-0000-0010-8000-00AA00389B71}`

Die -Methode belegt Arbeitsspeicher für die Zeichenfolge. Die Anwendung muss **SysFreeString** aufrufen, um den Arbeitsspeicher freizugeben.

Legen Sie vor dem Aufrufen dieser Methode den Dateinamen und den Stream fest, indem [**Sie IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) und [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md)aufrufen.

Wenn sich die Medienerkennung im Bitmapgrabbermodus befindet, gibt diese Methode E \_ INVALIDARG zurück. Weitere Informationen finden Sie unter [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




