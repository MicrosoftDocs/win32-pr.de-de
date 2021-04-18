---
description: Beachten Sie, dass diese Schnittstelle veraltet ist.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Iamfilterdata::P Ardie FilterData-Methode (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364898"
---
# <a name="iamfilterdataparsefilterdata-method"></a>Iamfilterdata::P Ardie FilterData-Methode

> [!Note]  
> Diese Schnittstelle ist veraltet. Diese sollten von neuen Anwendungen nicht verwendet werden.

 

Die- `ParseFilterData` Methode entpackt die binären Registrierungsdaten für einen Filter.

Es gibt in der Regel keinen Grund dafür, dass eine Anwendung diese Methode aufruft. Die [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode bietet eine bequeme Möglichkeit, auf die Filter Registrierungsdaten zuzugreifen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rgbfilterdata* \[ in\]
</dt> <dd>

Zeiger auf die binären Registrierungsdaten. Sie können diese Daten abrufen, indem Sie die Eigenschaft "FilterData" aus dem filtermoniker abrufen. Die Daten werden als **SAFEARRAY** von Bytes (VT \_ UI1 \| VT \_ Array) gespeichert.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Gibt die Größe der Binärdaten in Bytes an.

</dd> <dt>

*prgbRegFilter2* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die entpackten Daten empfängt. Wenn die Methode zurückgegeben wird, wandeln Sie diesen Zeiger in einen [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) -Typ um, um auf die Filterdaten zuzugreifen. Der Aufrufer muss den Speicher freigeben, indem er die **CoTaskMemFree** -Methode aufruft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Bei einem Fehler wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Der Header "fil \_ Data. h" befindet sich im Verzeichnis " [Mapper Sample](mapper-sample.md) " in der Windows SDK.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Fil- \_ Daten. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamfilterdata-Schnittstelle**](iamfilterdata.md)
</dt> </dl>

 

 




