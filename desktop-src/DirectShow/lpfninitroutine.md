---
description: Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: LPFNInitRoutine-Funktionszeiger (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: c07f22b9dc261fe9d7b073a1f1ab93aa49e482fb70c53288aeaf606e6be9aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685080"
---
# <a name="lpfninitroutine-function-pointer"></a>LPFNInitRoutine-Funktionszeiger

Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bLoading* 
</dt> <dd>

**TRUE,** wenn die DLL geladen wird, **FALSE,** wenn die DLL entladen wird.

</dd> <dt>

*rclsid* 
</dt> <dd>

Zeiger auf die CLISD des Objekts, angegeben in der [**CFactoryTemplate::m \_ ClsID-Membervariable.**](cfactorytemplate-m-clsid.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Funktionszeiger gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Combase.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CFactoryTemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




