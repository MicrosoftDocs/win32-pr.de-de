---
description: Die GetMediaPositionInterface-Methode ruft die Schnittstellenzeiger IMediaPosition und IMediaSeeking des Filters ab.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: CBaseRenderer.GetMediaPositionInterface-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12e15b297f78b3386ae9ad31e749858bad14b87e59e938ac02a3cf3a9ca002a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872330"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>CBaseRenderer.GetMediaPositionInterface-Methode

Die `GetMediaPositionInterface` -Methode ruft die [**Schnittstellenzeiger IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) und [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) des Filters ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* 
</dt> <dd>

Verweisbezeichner der Schnittstelle.

</dd> <dt>

*Ppv* 
</dt> <dd>

Adresse einer Variablen, die den Schnittstellenzeiger empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                   | Beschreibung                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>     |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | Die Schnittstelle wird nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Filter delegiert alle Suchbefehle an ein [**CRendererPosPassThru-Objekt,**](crendererpospassthru.md) das sie upstreamübergibt. Diese Methode erstellt das **CRendererPosPassThru-Objekt,** sofern es noch nicht vorhanden ist, und fragt es nach der angeforderten Schnittstelle ab.

Die [**CBaseRenderer::m \_ pPosition-Membervariable**](cbaserenderer-m-pposition.md) speichert einen Zeiger auf das **CRendererPosPassThru-Objekt.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




