---
description: 'CBaseControlVideo.CBaseControlVideo-Konstruktor : Konstruktormethode.'
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
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096348"
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

## <a name="remarks"></a>Bemerkungen

Das -Objekt implementiert die [**IBasicVideo-Steuerelementschnittstelle.**](/windows/desktop/api/Control/nn-control-ibasicvideo)

Alle Schnittstellenmethoden von [**IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo) die diese Klasse implementiert, erfordern, dass der Filter ordnungsgemäß verbunden ist. Aus diesem Grund wird der Klasse ein Pin übergeben, mit dem sie synchronisiert werden soll. Jedes Mal, wenn eine Schnittstellenmethode aufgerufen wird, bestimmt das -Objekt, dass die Stecknadel weiterhin verbunden ist.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




