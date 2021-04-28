---
description: 'IAMTimeline::GetDirtyRange-Methode: Wird nicht unterstützt.'
ms.assetid: 6e45b542-be3f-4da8-808a-6aa8b4299519
title: IAMTimeline::GetDirtyRange-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cb0ecbd8a93698d36354c251f0381c35acf288a2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119598"
---
# <a name="iamtimelinegetdirtyrange-method"></a>IAMTimeline::GetDirtyRange-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Wird nicht unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Reserviert.

</dd> <dt>

*Pstop* 
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Headerdatei Qedit.h ist mit Direct3D-Headern nach Version 7 nicht kompatibel.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> </dl>

 

 




