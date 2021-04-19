---
description: Die get \_ streamtypeb-Methode ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'Imediadet:: get_StreamTypeB-Methode (qedit. h)'
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
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367771"
---
# <a name="imediadetget_streamtypeb-method"></a>Imediadet:: get \_ streamtypeb-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_StreamTypeB` Methode ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt eine Zeichen folgen Darstellung der Medientyp-GUID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der zurückgegebene **BSTR** ist wie folgt formatiert: `{73647561-0000-0010-8000-00AA00389B71}`

Die-Methode ordnet Speicher für die Zeichenfolge zu. Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.

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

 

 




