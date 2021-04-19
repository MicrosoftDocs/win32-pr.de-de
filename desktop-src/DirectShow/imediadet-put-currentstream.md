---
description: Die Put \_ currentstream-Methode gibt die Datenstrom Nummer an, die vom Medien Detektor verwendet werden soll.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: Imediadet::p ut_CurrentStream-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372370"
---
# <a name="imediadetput_currentstream-method"></a>Imediadet::p UT \_ currentstream-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_CurrentStream` Methode gibt die Datenstrom Nummer an, die vom Medien Detektor verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Die streamnummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Rufen Sie vor dem Aufrufen dieser Methode [**imediadet::p UT \_ filename**](imediadet-put-filename.md) auf, um den Dateinamen festzulegen. Wenden Sie [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) an, um die Anzahl der in der Quelldatei enthaltenen Streams zu ermitteln.

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

 

 




