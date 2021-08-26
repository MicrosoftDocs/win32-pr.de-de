---
description: 'CBaseControlVideo.CBaseControlVideo-Konstruktor: Konstruktormethode.'
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: CBaseControlVideo.CBaseControlVideo-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbd9ed452dbf0c0091c3f1813f6f671c476dfa52e31b402440a3b1d19db2d3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057370"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>CBaseControlVideo.CBaseControlVideo-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
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

## <a name="remarks"></a>Hinweise

Das -Objekt implementiert die [**IBasicVideo-Steuerelementschnittstelle.**](/windows/desktop/api/Control/nn-control-ibasicvideo)

Alle Schnittstellenmethoden von [**IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo) die diese Klasse implementiert, erfordern, dass der Filter ordnungsgemäß verbunden ist. Aus diesem Grund wird der Klasse ein Pin übergeben, mit dem sie synchronisiert werden soll. Jedes Mal, wenn eine Schnittstellenmethode aufgerufen wird, bestimmt das -Objekt, dass die Stecknadel weiterhin verbunden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




