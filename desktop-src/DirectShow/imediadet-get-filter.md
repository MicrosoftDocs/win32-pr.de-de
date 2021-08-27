---
description: Die get \_ Filter-Methode ruft einen Zeiger auf den Quellfilter ab, der derzeit von der Medienerkennung verwendet wird.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: IMediaDet::get_Filter-Methode (Qedit.h)
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
ms.openlocfilehash: c3d4622438dbb8c8dfc54183550c274fcd4555de8b75435b85bbbebfae9c2c1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083760"
---
# <a name="imediadetget_filter-method"></a>IMediaDet::get-Filtermethode \_

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `get_Filter` -Methode ruft einen Zeiger auf den Quellfilter ab, der derzeit vom Medienerkennungsgerät verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppVal* \[ out, retval\]
</dt> <dd>

Empfängt einen Zeiger auf die **IUnknown-Schnittstelle** des Filters. Wenn kein Quellfilter verwendet wird, wird der Wert auf **NULL** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn *\* ppVal* nicht **NULL** ist, verfügt die **IUnknown-Schnittstelle** über einen ausstehenden Verweiszähler, wenn die Methode zurückgegeben wird. Geben Sie die Schnittstelle frei, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 




