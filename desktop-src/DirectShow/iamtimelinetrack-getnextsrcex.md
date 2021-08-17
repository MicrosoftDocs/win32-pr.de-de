---
description: Die GetNextSrcEx-Methode ruft die nächste Quelle nach der angegebenen Quelle ab.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: IAMTimelineTrack::GetNextSrcEx-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 438fcdbf4f95406994f5bf0cc63ebf5b5f600a9908419b63c4ceace65dfa9659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952799"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a>IAMTimelineTrack::GetNextSrcEx-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetNextSrcEx` -Methode ruft die nächste Quelle nach der angegebenen Quelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Plast* 
</dt> <dd>

Zeiger auf das vorherige Quellobjekt oder **NULL,** um die erste Quelle in der Spur abzurufen.

</dd> <dt>

*ppNext* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des nächsten Quellobjekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode eine Quelle abruft, andernfalls S \_ FALSE.

## <a name="remarks"></a>Hinweise

Wenn die Methode S \_ OK zurückgibt, verfügt **die IAMTimelineObj-Schnittstelle,** die sie zurückgibt, über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie die -Schnittstelle wieder frei geben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineTrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




