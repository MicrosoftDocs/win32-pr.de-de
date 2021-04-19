---
description: 'Die SetProperties-Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. Diese Methode implementiert die imemzuzucator:: SetProperties-Methode.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Cbasezucator. SetProperties-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359743"
---
# <a name="cbaseallocatorsetproperties-method"></a>Cbasezucator. SetProperties-Methode

Die `SetProperties` -Methode gibt die Anzahl der zuzuordnenden Puffer und die Größe der einzelnen Puffer an. Diese Methode implementiert die [**imemzuzucator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) -Methode.

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

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                                 | Beschreibung                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Erfolg.<br/>                                                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                   | **Null** -Zeigerargument.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ \_ hat bereits ein Commit ausgeführt**</dt> </dl>   | Der zugewiesene Arbeitsspeicher kann nicht geändert werden, solange der Filter aktiv ist.<br/> |
| <dl> <dt>**VFW \_ E \_ badalign**</dt> </dl>             | Es wurde eine ungültige Ausrichtung angegeben.<br/>                        |
| <dl> <dt>**ausstehende VFW \_ E- \_ Puffer \_**</dt> </dl> | Mindestens ein Puffer ist noch aktiv.<br/>                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die Puffer Anforderungen an, weist jedoch keine Puffer zu. Nennen Sie die [**cbaseallocator:: Commit**](cbaseallocator-commit.md) -Methode, um Puffer zuzuweisen.

Der Aufrufer ordnet zwei \_ zuordnereigenschafts-Strukturen zu. Der *pRequest* -Parameter enthält die Puffer Anforderungen des Aufrufers, einschließlich der Anzahl der Puffer und der Größe der einzelnen Puffer. Wenn die Methode zurückgibt, enthält der *pactual* -Parameter die tatsächlichen Puffer Eigenschaften, wie von der Zuweisung festgelegt. In der Basisklasse entsprechen die tatsächlichen Eigenschaften immer den angeforderten Eigenschaften, wenn Sie davon ausgehen, dass die Methode erfolgreich ist. Abgeleitete Klassen können dieses Verhalten überschreiben.

Für die Zuweisung darf kein Commit ausgeführt werden, und es dürfen keine ausstehenden Puffer vorhanden sein. In der Basisklasse muss die Ausrichtung gleich 1 sein. Die [**cmemzuordcator**](cmemallocator.md) -Klasse überschreibt diese Anforderung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




