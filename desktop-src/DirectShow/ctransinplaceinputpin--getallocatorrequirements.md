---
description: 'Die getallocatorrequirements-Methode ruft die von der PIN angeforderten zuordnereigenschaften ab. Diese Methode implementiert die IMemInputPin:: getallo. Requirements-Methode.'
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Ctransinplaceinputpin. getallocatorrequirements-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365556"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>Ctransinplaceinputpin. getalloerrequirements-Methode

Die- `GetAllocatorRequirements` Methode ruft die von der PIN angeforderten zuordnereigenschaften ab. Diese Methode implementiert die [**IMemInputPin:: getallo. Requirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*p-Eigenschaften* 
</dt> <dd>

Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die mit den Anforderungen ausgefüllt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                               | Beschreibung                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                                                                                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Die Ausgabe-PIN ist nicht verbunden, oder die downstreameingabepin unterstützt die-Methode nicht.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument<br/>                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Ausgabe-PIN verbunden ist, übergibt diese Methode den-Befehl an die downstreameingabepin. Andernfalls wird E \_ notimpl zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplaceinputpin-Klasse**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




