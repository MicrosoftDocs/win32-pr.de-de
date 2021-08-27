---
description: Ruft einen Schnittstellenzeiger ab und erhöht die Verweisanzahl. Diese Methode implementiert die INonDelegatingUnknown::NonDelegatingQueryInterface-Methode.
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: CUnknown.NonDelegatingQueryInterface-Methode (Combase.h)
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
ms.openlocfilehash: 26e13d9d30c3da208bb702427ee99a9648a7f538ba0d5a6a1b359db41e2cd155
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076010"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>CUnknown.NonDelegatingQueryInterface-Methode

Ruft einen Schnittstellenzeiger ab und erhöht die Verweisanzahl. Diese Methode implementiert die **INonDelegatingUnknown::NonDelegatingQueryInterface-Methode.**

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

Bezeichner der Schnittstelle.

</dd> <dt>

*Ppv* 
</dt> <dd>

Adresse eines Zeigers zum Empfangen der Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | Das -Objekt unterstützt diese Schnittstelle nicht.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     |  NULL-Zeigerargument.<br/>              |



 

## <a name="remarks"></a>Hinweise

Die **CUnknown-Klasse** macht nur die **IUknown-Schnittstelle** verfügbar. Überschreiben Sie diese Methode, um zusätzliche Schnittstellen verfügbar zu machen. Informationen zum Überschreiben dieser Methode finden Sie unter [Implementieren von IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




