---
description: 'CBaseControlWindow.CBaseControlWindow-Konstruktor : Konstruktormethode.'
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: CBaseControlWindow.CBaseControlWindow-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4944d121c4fe99ee36c893a4d51ca0cd72344dfa47dde17629f5ca2a1ce3fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660765"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>CBaseControlWindow.CBaseControlWindow-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFilter* 
</dt> <dd>

Zeiger auf das besitzende Medienfilterobjekt.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Zeiger auf den kritischen Abschnitt, der zum Sperren verwendet werden soll.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf die Objektbeschreibung.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf die steuernde **IUnknown-Schnittstelle,** wenn das Objekt Teil eines Aggregats ist; andernfalls muss NULL **sein.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen HRESULT-Wert empfängt, der den Erfolg oder Fehler der Konstruktormethode angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlWindow-Klasse**](cbasecontrolwindow.md)
</dt> </dl>

 

 




