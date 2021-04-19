---
description: Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Lpfninitroutine-Funktionszeiger (ComBase. h)
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
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352958"
---
# <a name="lpfninitroutine-function-pointer"></a>Lpfninitroutine-Funktionszeiger

Ein Zeiger auf eine Funktion, die vom DLL-Einstiegspunkt aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bloading* 
</dt> <dd>

**True** , wenn die dll geladen wird, **false** , wenn die DLL entladen wird.

</dd> <dt>

*rclsid* 
</dt> <dd>

Zeiger auf das CLISD des Objekts, das in der [**cfactorytemplate:: m \_ CLSID**](cfactorytemplate-m-clsid.md) -Element Variablen angegeben ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Funktionszeiger gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cfactorytemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




