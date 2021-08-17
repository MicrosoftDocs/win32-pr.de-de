---
description: Erfahren Sie mehr über die IAMFilterData::CreateFilterData-Methode, die binäre Registrierungsdaten für einen Filter erstellt. Diese Schnittstelle ist veraltet.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: IAMFilterData::CreateFilterData-Methode (File \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 81c2ba3a56ba9c09a2ce7b23bcad1a83880e61256402c291b5aebde9988218c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428670"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>IAMFilterData::CreateFilterData-Methode

> [!Note]  
> Diese Schnittstelle ist veraltet. Neue Anwendungen sollten sie nicht verwenden.

 

Die `CreateFilterData` -Methode erstellt binäre Registrierungsdaten für einen Filter. Diese Daten können als REG \_ BINARY-Unterschlüssel mit dem Namen FilterData unter dem CLSID-Schlüssel des Filters in die Registrierung geschrieben werden.

Es gibt in der Regel keinen Grund für eine Anwendung, diese Methode aufzurufen. Die [**IFilterMapper2::RegisterFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) erstellt automatisch die Binärdaten und fügt sie dem richtigen Speicherort in der Registrierung hinzu. Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prf2* \[ In\]
</dt> <dd>

Zeiger auf eine [**REGFILTER2-Struktur,**](/windows/desktop/api/strmif/ns-strmif-regfilter2) die die Filterinformationen enthält.

</dd> <dt>

*prgbFilterData* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die Binärdaten empfängt. Die -Methode ordnet den Arbeitsspeicher für die Daten zu. Der Aufrufer muss den Arbeitsspeicher freigeben, indem er die **CoTaskMemFree-Methode aufruft.**

</dd> <dt>

*- und -N* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Größe der Binärdaten in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Bei einem Fehler wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Der Header Fil \_ data.h befindet sich im [Verzeichnis Mapper Sample](mapper-sample.md) im Windows SDK.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMFilterData-Schnittstelle**](iamfilterdata.md)
</dt> </dl>

 

 




