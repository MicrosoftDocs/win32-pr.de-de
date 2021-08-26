---
description: Die GetEffect-Methode ruft den Effekt auf der angegebenen Prioritätsebene ab.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: IAMTimelineEffectable::GetEffect-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d53ecc7c3d5291ddb6b894b24835eeb236f036e94eb166383da907a9f469c960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905180"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>IAMTimelineEffectable::GetEffect-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die **GetEffect-Methode** ruft den Effekt auf der angegebenen Prioritätsebene ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppFX* \[ out\]
</dt> <dd>

Empfängt die [**IAMTimelineObj-Schnittstelle des**](iamtimelineobj.md) Effekts.

</dd> <dt>

*welche* 
</dt> <dd>

Prioritätsebene des abzurufenden Effekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen HRESULT-Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                               | Beschreibung                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Keine Auswirkung mit der angegebenen Priorität,<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                             |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> |  NULL-Zeigerargument.<br/>           |



 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineEffectable-Schnittstelle**](iamtimelineeffectable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




