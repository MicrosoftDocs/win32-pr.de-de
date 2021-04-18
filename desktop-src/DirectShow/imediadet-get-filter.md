---
description: Die get \_ Filter-Methode ruft einen Zeiger auf den Quell Filter ab, der derzeit vom Medien Erkennungs Modul verwendet wird.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Imediadet:: get_Filter-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352071"
---
# <a name="imediadetget_filter-method"></a>Imediadet:: get- \_ Filter Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_Filter` Methode ruft einen Zeiger auf den Quell Filter ab, der derzeit vom Medien Erkennungs Modul verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppval* \[ Out, retval\]
</dt> <dd>

Empfängt einen Zeiger auf die **IUnknown** -Schnittstelle des Filters. Wenn kein Quell Filter verwendet wird, wird der Wert auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn der Wert der-Methode zurückgegeben wird, verfügt die **IUnknown** -Schnittstelle über einen ausstehenden Verweis Zähler, wenn *\* ppval* nicht **null** ist. Geben Sie die Schnittstelle frei, wenn Sie Sie nicht mehr benötigen.

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

 

 




