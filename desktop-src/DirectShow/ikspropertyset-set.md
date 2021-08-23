---
description: Die Set-Methode legt eine Eigenschaft fest, die durch eine Eigenschaftensatz-GUID und eine Eigenschaften-ID identifiziert wird.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: IKsPropertySet::Set-Methode (Ksproxy.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f3669acb7f2d3049b909a4dc2c24363bf478c9b44ad0a91528e1e8ea466399fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639190"
---
# <a name="ikspropertysetset-method"></a>IKsPropertySet::Set-Methode

Die `Set` -Methode legt eine Eigenschaft fest, die durch eine Eigenschaftensatz-GUID und eine Eigenschaften-ID identifiziert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
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

*pInstanceData* \[ In\]
</dt> <dd>

Zeiger auf einen Puffer, der Instanzdaten für die Eigenschaft enthält.

</dd> <dt>

*cbInstanceData* \[ In\]
</dt> <dd>

Größe des *pInstanceData-Puffers* in Bytes.

</dd> <dt>

*pPropData* \[ In\]
</dt> <dd>

Zeiger auf einen Puffer, der den Wert der Eigenschaft enthält.

</dd> <dt>

*cbPropData* \[ In\]
</dt> <dd>

Sise des *pPropData-Puffers* in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Erfolg.<br/>                                                         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | Der Eigenschaftensatz wird nicht unterstützt.<br/>                               |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | Die Eigenschaften-ID wird für den angegebenen Eigenschaftensatz nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Eine weitere Schnittstelle mit diesem Namen ist in der Headerdatei dsound.h vorhanden. Die beiden Schnittstellen sind nicht kompatibel. Die **IKsControl-Schnittstelle,** die im DirectShow DDK dokumentiert ist, ist jetzt die empfohlene Schnittstelle zum Übergeben von Eigenschaftensätzen zwischen WDM-Treibern und Benutzermoduskomponenten.

 

Sie müssen Ks.h vor Ksproxy.h einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet-Schnittstelle**](ikspropertyset.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




