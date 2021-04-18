---
description: Die getmediapositioninterface-Methode ruft die imediaposition-und imediaseeking-Schnittstellen Zeiger des Filters ab.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Cbaserderderer. getmediapositioninterface-Methode (renbase. h)
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
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352877"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a>Cbaserderderer. getmediapositioninterface-Methode

Die `GetMediaPositionInterface` -Methode ruft die [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstellen Zeiger des Filters ab.

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

Verweis Bezeichner der Schnittstelle.

</dd> <dt>

*PPV* 
</dt> <dd>

Adresse einer Variablen, die den Schnittstellen Zeiger empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                   | Beschreibung                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                 |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>     |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | Schnittstelle wird nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Filter delegiert alle Suchbefehle an ein [**crendererpospassthru**](crendererpospassthru.md) -Objekt, das Sie per Upstream übergibt. Diese Methode erstellt das **crendererpospassthru** -Objekt, wenn es noch nicht vorhanden ist, und fragt es nach der angeforderten Schnittstelle ab.

Die Element Variable [**cbaserenderer:: m \_ pposition**](cbaserenderer-m-pposition.md) speichert einen Zeiger auf das **crendererpospassthru** -Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




