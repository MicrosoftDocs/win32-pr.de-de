---
description: Die put \_ Filter-Methode gibt einen Quellfilter an, der von der Medienerkennung verwendet werden soll.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: IMediaDet::p ut_Filter-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a118baae251bd4456dfe0097afa091e0084e41ad96d96c9847006b8ce9c58d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398117"
---
# <a name="imediadetput_filter-method"></a>IMediaDet::p ut-Filtermethode \_

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `put_Filter` -Methode gibt einen Quellfilter für die zu verwendende Medienerkennung an.

> [!IMPORTANT]
> Fügen Sie den Quellfilter nicht Ihrem eigenen Filterdiagramm hinzu, oder verwenden Sie keinen Filter, der sich bereits in einem Filterdiagramm befindet. Das Medienerkennungsobjekt erstellt automatisch einen internen Filtergraphen, und das Setzen des Filters in ein anderes Diagramm kann zu unerwarteten Ergebnissen führen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle** des Quellfilters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *newVal* verweist nicht auf einen Filter.<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | **NULL-Zeigerargument.**<br/>           |



 

## <a name="remarks"></a>Hinweise

Für die meisten Anwendungen ist es einfacher, die [**Methode IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) mit dem Namen einer Quelldatei aufzurufen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




