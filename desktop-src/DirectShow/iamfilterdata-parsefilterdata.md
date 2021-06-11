---
description: Erfahren Sie mehr über die IAMFilterData::P arseFilterData-Methode, entpackt die binären Registrierungsdaten für einen Filter. Diese Schnittstelle ist veraltet.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: IAMFilterData::P arseFilterData-Methode (File \_ Data.h)
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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989445"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IAMFilterData::P arseFilterData-Methode

> [!Note]  
> Diese Schnittstelle ist veraltet. Neue Anwendungen sollten sie nicht verwenden.

 

Die `ParseFilterData` -Methode entpackt die binären Registrierungsdaten für einen Filter.

Es gibt in der Regel keinen Grund, warum eine Anwendung diese Methode aufruft. Die [**IFilterMapper2::EnumMatchingFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) bietet eine bequemere Möglichkeit, auf die Filterregistrierungsdaten zu zugreifen.

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

*rgbFilterData* \[ In\]
</dt> <dd>

Zeiger auf die binären Registrierungsdaten. Sie können diese Daten abrufen, indem Sie die Eigenschaft "FilterData" aus dem Filtermoniker abrufen. Die Daten werden als **SAFEARRAY von** Bytes (VT \_ UI1 \| VT \_ ARRAY) gespeichert.

</dd> <dt>

*cb* \[ In\]
</dt> <dd>

Gibt die Größe der Binärdaten in Bytes an.

</dd> <dt>

*prgbRegFilter2* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die entpackten Daten empfängt. Wenn die Methode zurückgegeben wird, casten Sie diesen Zeiger in einen [**REGFILTER2-Typ,**](/windows/desktop/api/strmif/ns-strmif-regfilter2) um auf die Filterdaten zu zugreifen. Der Aufrufer muss den Arbeitsspeicher durch Aufrufen der **CoTaskMemFree-Methode** frei geben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Bei einem Fehler wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Der Header Header \_ "data.h" befindet sich im [Verzeichnis Mapper Sample (Mapperbeispiel)](mapper-sample.md) im Windows SDK.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Datei \_ "data.h"</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMFilterData-Schnittstelle**](iamfilterdata.md)
</dt> </dl>

 

 




