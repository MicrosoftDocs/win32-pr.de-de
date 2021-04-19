---
description: Die setstretchmode-Methode legt den streckungs Modus fest. Der streckungs Modus bestimmt, wie eine Videoquelle gerendert wird, wenn deren Größe nicht den Ausgabe Dimensionen entspricht.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Iamtimelinesrc:: setstretchmode-Methode (qedit. h)'
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
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366896"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>Iamtimelinesrc:: setstretchmode-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetStretchMode` Methode legt den streckungs Modus fest. Der streckungs Modus bestimmt, wie eine Videoquelle gerendert wird, wenn deren Größe nicht den Ausgabe Dimensionen entspricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nstretchmode* 
</dt> <dd>

Flag, das den aktuellen streckungs Modus angibt. Eine Liste möglicher Werte finden Sie unter [**Resize Flags**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

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

[**Iamtimelinesrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




