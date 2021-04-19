---
description: Konstruktormethode.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Cbasecontrolvideo. cbasecontrolvideo-Konstruktor (ctlutil. h)
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
ms.openlocfilehash: dea0548079f8eb703f0c17557cab6a5e634cf242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356457"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>Cbasecontrolvideo. cbasecontrolvideo-Konstruktor

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

Zeiger auf das besitzende Medienfilter Objekt.

</dd> <dt>

*pinterfakelock* 
</dt> <dd>

Zeiger auf den kritischen Abschnitt, der zum Sperren verwendet werden soll.

</dd> <dt>

*pName* 
</dt> <dd>

Zeiger auf die Objektbeschreibung.

</dd> <dt>

*Kro* 
</dt> <dd>

Ein Zeiger auf die steuernde **IUnknown** -Schnittstelle, wenn das Objekt Teil eines Aggregats ist. Andernfalls muss **null** sein.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen HRESULT-Wert empfängt, der angibt, ob die Konstruktormethode erfolgreich war oder fehlgeschlagen ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das-Objekt implementiert die [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) -Steuerelement Schnittstelle.

Alle Schnittstellen Methoden aus [**ibasicvideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , die von dieser Klasse implementiert werden, erfordern, dass der Filter ordnungsgemäß verbunden ist. Aus diesem Grund wird der Klasse eine PIN übergeben, mit der Sie synchronisiert werden soll. Wenn eine Schnittstellen Methode aufgerufen wird, bestimmt das Objekt, dass die PIN noch verbunden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




