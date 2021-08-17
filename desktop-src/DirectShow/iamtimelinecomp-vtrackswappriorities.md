---
description: Die VTrackSwapPriorities-Methode schaltet die Prioritätsebenen von zwei Spuren um.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: IAMTimelineComp::VTrackSwapPriorities-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eb67e07f96ec2e8377690a5cd5233ba6cdb40242870da6d5f23b5f404b77b890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999283"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>IAMTimelineComp::VTrackSwapPriorities-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `VTrackSwapPriorities` -Methode wechselt die Prioritätsebenen von zwei Spuren.

Bei zwei Prioritätsebenen wechselt diese Methode die virtuellen Spuren zu diesen Prioritäten. Wenn die Methode zurückgegeben wird, befindet sich die Spur, die sich auf der ersten Prioritätsebene befand, jetzt auf der zweiten Prioritätsebene und umgekehrt.

## <a name="syntax"></a>Syntax


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VirtualTrackA* 
</dt> <dd>

Erste Prioritätsstufe, auf der virtuelle Spuren ausgetauscht werden sollen.

</dd> <dt>

*VirtualTrackB* 
</dt> <dd>

Zweite Prioritätsebene, bei der virtuelle Spuren ausgetauscht werden sollen.

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

[**IAMTimelineComp-Schnittstelle**](iamtimelinecomp.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




