---
description: Die GetStretchMode-Methode ruft den Stretchmodus ab. Der Stretchingmodus bestimmt, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht mit den Ausgabedimensionen übereinstimmt.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: IAMTimelineSrc::GetStretchMode-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 53be58df0315c4a03c62369f746efa510c2024fa030c3bef75eb4ff08505b1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952909"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a>IAMTimelineSrc::GetStretchMode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetStretchMode` -Methode ruft den Stretchmodus ab. Der Stretchingmodus bestimmt, wie eine Videoquelle gerendert wird, wenn ihre Größe nicht mit den Ausgabedimensionen übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnStretchMode* 
</dt> <dd>

Empfängt ein Flag, das den aktuellen Stretchmodus angibt. Eine Liste der möglichen Werte finden Sie unter Ändern der Größe von [**Flags.**](resize-flags.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




