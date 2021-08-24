---
description: Die SetDefaultTransitionB-Methode legt den Standardübergang fest. Diese Methode entspricht IAMTimeline::SetDefaultTransition, verwendet jedoch einen BSTR-Wert anstelle eines Zeigers auf eine GUID.
ms.assetid: 1998fd31-2ab8-477e-89ee-93ca92dc10ec
title: IAMTimeline::SetDefaultTransitionB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2a6ab2205c1d86c747ffcabbe69a88de8898fa1315ec98f9b816a5f5983dee59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905250"
---
# <a name="iamtimelinesetdefaulttransitionb-method"></a>IAMTimeline::SetDefaultTransitionB-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetDefaultTransitionB` -Methode legt den Standardübergang fest. Diese Methode entspricht [**IAMTimeline::SetDefaultTransition,**](iamtimeline-setdefaulttransition.md)verwendet jedoch einen BSTR-Wert anstelle eines Zeigers auf eine GUID.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefaultTransitionB(
   BSTR pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* 
</dt> <dd>

BSTR-Wert, der die GUID des Standardübergangs darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




