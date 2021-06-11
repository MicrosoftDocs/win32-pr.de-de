---
description: Erfahren Sie mehr über die IAMFilterData::CreateFilterData-Methode, die binäre Registrierungsdaten für einen Filter erstellt. Diese Schnittstelle ist veraltet.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: IAMFilterData::CreateFilterData-Methode (Eigenschaft \_ data.h)
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
ms.openlocfilehash: 0a0126266fc33dca030abad65ccf9f0d35f6e195
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989455"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>IAMFilterData::CreateFilterData-Methode

> [!Note]  
> Diese Schnittstelle ist veraltet. Neue Anwendungen sollten sie nicht verwenden.

 

Die `CreateFilterData` -Methode erstellt binäre Registrierungsdaten für einen Filter. Diese Daten können als REG BINARY-Unterschlüssel namens FilterData unter dem CLSID-Schlüssel des Filters in die \_ Registrierung geschrieben werden.

Es gibt in der Regel keinen Grund, warum eine Anwendung diese Methode aufruft. Die [**IFilterMapper2::RegisterFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) erstellt automatisch die Binärdaten und fügt sie dem richtigen Speicherort in der Registrierung hinzu. Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)

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

Adresse einer Variablen, die einen Zeiger auf die Binärdaten empfängt. Die -Methode weist den Arbeitsspeicher für die Daten zu. Der Aufrufer muss den Arbeitsspeicher durch Aufrufen der **CoTaskMemFree-Methode** frei geben.

</dd> <dt>

*( )* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Größe der Binärdaten in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Bei einem Fehler wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die HeaderDatei \_ data.h befindet sich im [Verzeichnis Mapper Sample (Mapper-Beispiel)](mapper-sample.md) im Windows SDK.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Datei \_ "Data.h"</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMFilterData-Schnittstelle**](iamfilterdata.md)
</dt> </dl>

 

 




