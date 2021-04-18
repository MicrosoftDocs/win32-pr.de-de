---
description: Die SetProperties-Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Cmemzuzucator. SetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357708"
---
# <a name="cmemallocatorsetproperties-method"></a>Cmemzuzucator. SetProperties-Methode

Die `SetProperties` -Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pRequest* 
</dt> <dd>

Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) -Struktur, die die Puffer Anforderungen enthält.

</dd> <dt>

*pactual* 
</dt> <dd>

Ein Zeiger auf eine **\_ zuordnereigenschafts** -Struktur, die die tatsächlichen Puffer Eigenschaften empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                 | Beschreibung                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Erfolg.<br/>                                                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                   | **Null** -Zeigerargument.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ \_ hat bereits ein Commit ausgeführt**</dt> </dl>   | Der zugewiesene Arbeitsspeicher kann nicht geändert werden, solange der Filter aktiv ist.<br/> |
| <dl> <dt>**VFW \_ E \_ badalign**</dt> </dl>             | Es wurde eine ungültige Ausrichtung angegeben.<br/>                        |
| <dl> <dt>**ausstehende VFW \_ E- \_ Puffer \_**</dt> </dl> | Mindestens ein Puffer ist noch aktiv.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode.

Die Puffer Ausrichtung, die vom **cbalign** -Member der **Zuweisungs \_ Eigenschafts** Struktur angegeben wird, muss eine selbst Potenz von zwei sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmemzuordcator-Klasse**](cmemallocator.md)
</dt> </dl>

 

 




