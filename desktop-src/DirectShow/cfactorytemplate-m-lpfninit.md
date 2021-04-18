---
description: Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird. Kann den Wert NULL haben.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Cfactoriytemplate:: m_lpfnInit Member (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365508"
---
# <a name="cfactorytemplatem_lpfninit-member"></a>Cfactoriytemplate:: m \_ lpfninit-Member

Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird. Kann **null** sein.

## <a name="syntax"></a>Syntax


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a>Bemerkungen

Der Funktions Zeigertyp ist " [**lpfninitroutine**](lpfninitroutine.md)". Wenn Sie diese Funktion in der DLL bereitstellen, ruft die DLL-Einstiegspunkt Funktion Sie mit den folgenden Parametern auf:

-   *bloading*: **true** , wenn die dll geladen wird, **false** , wenn die DLL entladen wird.
-   *rclsid*: Zeiger auf das CLISD des Objekts, das in der [**cfactorytemplate:: m \_ CLSID**](cfactorytemplate-m-clsid.md) -Element Variablen angegeben ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cfactorytemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




