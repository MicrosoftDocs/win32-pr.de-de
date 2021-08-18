---
description: Die SetStretchMode-Methode legt den Stretchmodus fest. Der Streckungsmodus bestimmt, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht mit den Ausgabedimensionen übereinstimmen soll.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: IAMTimelineSrc::SetStretchMode-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c12d14edf665bb3257b627a194923c267ee9e8bd25027e40a7a975a15c10025f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148543"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>IAMTimelineSrc::SetStretchMode-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetStretchMode` -Methode legt den Stretchmodus fest. Der Streckungsmodus bestimmt, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht mit den Ausgabedimensionen übereinstimmen soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nStretchMode* 
</dt> <dd>

Flag, das den aktuellen Stretchmodus angibt. Eine Liste der möglichen Werte finden Sie unter [**Größenvergrößerungen für Flags.**](resize-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




