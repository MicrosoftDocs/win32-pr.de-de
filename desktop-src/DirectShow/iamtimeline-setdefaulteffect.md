---
description: Die setdefaulteffect-Methode legt den Standardeffekt fest. Wenn die Rendering-Engine einen Effekt nicht Renderingmodul renderten kann, ersetzt Sie den Standardeffekt
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'Iamtimeline:: setdefaulteffect-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366013"
---
# <a name="iamtimelinesetdefaulteffect-method"></a>Iamtimeline:: setdefaulteffect-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetDefaultEffect` Methode legt den Standardeffekt fest. Wenn die Rendering-Engine einen Effekt nicht Renderingmodul renderten kann, ersetzt Sie den Standardeffekt

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* 
</dt> <dd>

Ein Zeiger auf die GUID des Standard Effekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn Sie keinen Standardeffekt festlegen oder wenn der als Standard angegebene Effekt einen Fehler verursacht, verwendet des einen eigenen Standardeffekt.

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

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




