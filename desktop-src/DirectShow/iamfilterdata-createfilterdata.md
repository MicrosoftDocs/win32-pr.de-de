---
description: Beachten Sie, dass diese Schnittstelle veraltet ist.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Iamfilterdata:: deatefilterdata-Methode (fil \_ Data. h)'
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
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370034"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>Iamfilterdata:: kreatefilterdata-Methode

> [!Note]  
> Diese Schnittstelle ist veraltet. Diese sollten von neuen Anwendungen nicht verwendet werden.

 

Die- `CreateFilterData` Methode erstellt binäre Registrierungsdaten für einen Filter. Diese Daten können als reg \_ Binary-Unterschlüssel namens "FilterData" unter dem CLSID-Schlüssel des Filters in die Registrierung geschrieben werden.

Es gibt in der Regel keinen Grund dafür, dass eine Anwendung diese Methode aufruft. Die [**IFilterMapper2:: registerfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) -Methode erstellt automatisch die Binärdaten und fügt Sie der richtigen Position in der Registrierung hinzu. Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).

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

*prf2* \[ in\]
</dt> <dd>

Zeiger auf eine [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) -Struktur, die die Filter Informationen enthält.

</dd> <dt>

*prgbfilterdata* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die Binärdaten empfängt. Die-Methode ordnet den Arbeitsspeicher für die Daten zu. Der Aufrufer muss den Speicher freigeben, indem er die **CoTaskMemFree** -Methode aufruft.

</dd> <dt>

*Platine* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Binärdaten empfängt (in Bytes).

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

 

 




