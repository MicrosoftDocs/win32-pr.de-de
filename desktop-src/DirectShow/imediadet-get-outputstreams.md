---
description: Die get \_ outputstreams-Methode ruft die Anzahl der in der Medienquelle enthaltenen Audiodaten-und Videostreams ab. Alle anderen Streamtypen, z. b. Datenströme, werden ignoriert.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Imediadet:: get_OutputStreams-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369206"
---
# <a name="imediadetget_outputstreams-method"></a>Imediadet:: get \_ outputstreams-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `get_OutputStreams` -Methode ruft die Anzahl der in der Medienquelle enthaltenen Audiodaten und Videostreams ab. Alle anderen Streamtypen, z. b. Datenströme, werden ignoriert.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt die Anzahl der Ausgabestreams.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Rufen Sie vor dem Aufrufen dieser Methode [**imediadet::p UT \_ filename**](imediadet-put-filename.md) auf, um den Dateinamen festzulegen. Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück. Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).

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

 

 




