---
description: Die QuerySupported-Methode bestimmt, ob ein Objekt einen angegebenen Eigenschaftensatz unterstützt.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: IKsPropertySet::QuerySupported-Methode (Ks.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 7c79e81171349e2c481535eeab212717de072b17778b052dac3fc377cea0e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792320"
---
# <a name="ikspropertysetquerysupported-method"></a>IKsPropertySet::QuerySupported-Methode

Die `QuerySupported` -Methode bestimmt, ob ein Objekt einen angegebenen Eigenschaftensatz unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guidPropSet* \[ In\]
</dt> <dd>

Guid des Eigenschaftensatzes.

</dd> <dt>

*dwPropID* \[ In\]
</dt> <dd>

Bezeichner der Eigenschaft innerhalb des Eigenschaftensatzes.

</dd> <dt>

*pTypeSupport* \[ out\]
</dt> <dd>

Zeiger auf einen Wert, in dem Flags gespeichert werden sollen, die die vom Treiber bereitgestellte Unterstützung angeben. Folgende Flags werden unterstützt.



| Wert                    | Beschreibung                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| KSPROPERTY-UNTERSTÜTZUNG \_ \_ GET | Sie können die Eigenschaft abrufen, indem Sie die [**IKsPropertySet::Get-Methode**](ikspropertyset-get.md) aufrufen. |
| \_KSPROPERTY-SUPPORTSATZ \_ | Sie können die Eigenschaft ändern, indem Sie [**IKsPropertySet::Set aufrufen.**](ikspropertyset-set.md)              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Die angegebene Kombination aus Eigenschaftensatz und Eigenschaften-ID wird unterstützt.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                | Der Eigenschaftensatz wird nicht unterstützt.<br/>                                       |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | Die Eigenschaften-ID wird für den angegebenen Eigenschaftensatz nicht unterstützt.<br/>         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | Der Eigenschaftensatz wird nicht unterstützt.<br/>                                       |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Eine weitere Schnittstelle mit diesem Namen ist in der Headerdatei dsound.h vorhanden. Die beiden Schnittstellen sind nicht kompatibel. Die **IKsControl-Schnittstelle,** die im DirectShow DDK dokumentiert ist, ist jetzt die empfohlene Schnittstelle zum Übergeben von Eigenschaftensätzen zwischen WDM-Treibern und Benutzermoduskomponenten.

 

Sie müssen Ks.h vor Ksproxy.h einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                             |
| Header<br/>                   | <dl> <dt>Ks.h; </dt> <dt>Ksproxy.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet-Schnittstelle**](ikspropertyset.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




