---
description: Die effectionwappriority-Methode schaltet die Prioritäts Ebenen von zwei Effekten um.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'Iamtimelineeffectable:: effectwapprioritäten-Methode (qedit. h)'
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
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365842"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>Iamtimelineeffectable:: effeczwapprioritäten-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `EffectSwapPriorities` Methode schaltet die Prioritäts Ebenen von zwei Effekten um.

Bei zwei Prioritäts Werten vertauscht diese Methode die Auswirkungen auf diese Prioritäten. Wenn die-Methode zurückgegeben wird, liegt der Effekt, der sich auf der ersten Prioritätsstufe befand, auf der zweiten Prioritätsstufe und umgekehrt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Prioritya* 
</dt> <dd>

Die erste Prioritätsstufe, bei der die Effekte ausgetauscht werden sollen.

</dd> <dt>

*Priorityb* 
</dt> <dd>

Die zweite Prioritätsstufe, bei der die Effekte ausgetauscht werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelineeffectable-Schnittstelle**](iamtimelineeffectable.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




