---
description: 'CRendererPosPassThru.CRendererPosPassThru-Konstruktor : Konstruktormethode.'
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: CRendererPosPassThru.CRendererPosPassThru-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59972f12f0f746ef68c267e3fbd0d071d54193c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085408"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a>CRendererPosPassThru.CRendererPosPassThru-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen des Objekts zu Debugzwecken. Ordnen Sie diesen Parameter im statischen Speicher zu.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL** fest.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Ignoriert.

</dd> <dt>

*pPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins des Filters.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




