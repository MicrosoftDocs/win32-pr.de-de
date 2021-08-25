---
description: Die EffectSwapPriorities-Methode schaltet die Prioritätsebenen von zwei Effekten um.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: IAMTimelineEffectable::EffectSwapPriorities-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e79f3f83422290600b4b6e75dbf15daff161f5e913a0300645254cdf94e7c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928230"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>IAMTimelineEffectable::EffectSwapPriorities-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `EffectSwapPriorities` -Methode schaltet die Prioritätsebenen von zwei Effekten um.

Bei zwei Prioritätswerten tauscht diese Methode die Auswirkungen bei diesen Prioritäten aus. Wenn die Methode zurückgegeben wird, liegt der Effekt, der auf der ersten Prioritätsebene lag, auf der zweiten Prioritätsebene und umgekehrt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PriorityA* 
</dt> <dd>

Erste Prioritätsstufe, bei der Effekte ausgetauscht werden sollen.

</dd> <dt>

*PriorityB* 
</dt> <dd>

Zweite Prioritätsebene, bei der Effekte ausgetauscht werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineEffectable-Schnittstelle**](iamtimelineeffectable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




