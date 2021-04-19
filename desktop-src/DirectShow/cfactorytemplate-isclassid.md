---
description: Die isclassid-Methode bestimmt, ob eine CLSID mit dieser Klassen Vorlage übereinstimmt.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Cfactorytemplate. isclassid-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367678"
---
# <a name="cfactorytemplateisclassid-method"></a>Cfactorytemplate. isclassid-Methode

Die- `IsClassID` Methode bestimmt, ob eine CLSID mit dieser Klassen Vorlage übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rclsid* 
</dt> <dd>

Verweis auf eine CLSID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn der *rclsid* -Parameter dieselbe CLSID wie die CLSID-Element Variable " [**\_ cfactorytemplate:: m**](cfactorytemplate-m-clsid.md) " ist, andernfalls wird " **false**" zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cfactorytemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




