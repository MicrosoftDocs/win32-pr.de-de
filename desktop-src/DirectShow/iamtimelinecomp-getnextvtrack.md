---
description: Die GetNextVTrack-Methode ruft die nächste virtuelle Spur nach einer angegebenen virtuellen Spur ab.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: IAMTimelineComp::GetNextVTrack-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dbeaf5d7987f1baf2b3df9804c4abd3049c38042a29f4177f83abec6855140a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401051"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a>IAMTimelineComp::GetNextVTrack-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetNextVTrack` -Methode ruft die nächste virtuelle Spur nach einer angegebenen virtuellen Spur ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Zeiger auf die vorherige virtuelle Spur oder **NULL,** um die erste virtuelle Spur in der Komposition abzurufen.

</dd> <dt>

*ppNextVirtualTrack* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) der nächsten virtuellen Spur in der Reihenfolge der Priorität.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode eine virtuelle Spur abruft, \_ andernfalls S FALSE.

## <a name="remarks"></a>Hinweise

Wenn die Methode erfolgreich ist, verfügt die **zurückgegebene IAMTimelineObj-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

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

[**IAMTimelineComp-Schnittstelle**](iamtimelinecomp.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




