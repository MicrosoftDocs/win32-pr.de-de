---
description: 'Ruft einen Schnittstellen Zeiger ab und erhöht den Verweis Zähler. Diese Methode implementiert die inondelegatingunknown:: nondelegatingqueryinterface-Methode.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Cunknown. nondelegatingqueryinterface-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362057"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>Cunknown. nondelegatingqueryinterface-Methode

Ruft einen Schnittstellen Zeiger ab und erhöht den Verweis Zähler. Diese Methode implementiert die **inondelegatingunknown:: nondelegatingqueryinterface** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* 
</dt> <dd>

Der Bezeichner der Schnittstelle.

</dd> <dt>

*PPV* 
</dt> <dd>

Adresse eines Zeigers, der die Schnittstelle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | Diese Schnittstelle wird vom Objekt nicht unterstützt.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument.<br/>              |



 

## <a name="remarks"></a>Bemerkungen

Die **cunknown** -Klasse macht nur die **iuknown** -Schnittstelle verfügbar. Überschreiben Sie diese Methode, um zusätzliche Schnittstellen bereitzustellen Informationen dazu, wie Sie diese Methode überschreiben, finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




