---
description: Die CreatePosPassThru-Funktion erstellt ein CPosPassThru-Objekt oder ein CRendererPosPassThru-Objekt.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: CreatePosPassThru-Funktion (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0118299bd328d09d77ccbb8d5258b25c0ac57bdc21fc7a47f642374e8be12357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908750"
---
# <a name="createpospassthru-function"></a>CreatePosPassThru-Funktion

Die `CreatePosPassThru` Funktion erstellt ein [**CPosPassThru-Objekt**](cpospassthru.md) oder [**ein CRendererPosPassThru-Objekt.**](crendererpospassthru.md)

## <a name="syntax"></a>Syntax


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAgg* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts. Legen Sie andernfalls diesen Parameter auf **NULL fest.**

</dd> <dt>

*bRenderer* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Filter ein Renderer ist. Verwenden Sie den Wert **TRUE,** wenn der Filter ein Renderer ist, **andernfalls FALSE.** Wenn der Wert **TRUE ist,** erstellt diese Methode eine Instanz der [**CRendererPosPassThru-Klasse.**](crendererpospassthru.md) Wenn der Wert **FALSE ist,** erstellt die Methode eine Instanz der **CPosPassThru-Klasse.**

</dd> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) auf dem Eingabepin des Filters.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die **IUnknown-Schnittstelle** des Objekts empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich. Andernfalls gibt einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode verwendet die [**ISeekingPassThru-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) um das -Objekt zu erstellen. Das -Objekt wird dynamisch aus dem Quartz.dll.

Wenn die Funktion erfolgreich ist, verfügt die zurückgegebene **IUnknown-Schnittstelle** über eine ausstehende Verweisanzahl. Der Aufrufer muss die Schnittstelle frei geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




