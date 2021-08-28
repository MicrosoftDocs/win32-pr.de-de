---
description: Die GetVTrack-Methode ruft die virtuelle Spur mit der angegebenen Priorität ab.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: IAMTimelineComp::GetVTrack-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 245f19783f7a472f86544d14f27c588e7a5938e899f2f389887d7a7817d6254e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756300"
---
# <a name="iamtimelinecompgetvtrack-method"></a>IAMTimelineComp::GetVTrack-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetVTrack` -Methode ruft die virtuelle Spur mit der angegebenen Priorität ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppVirtualTrack* \[ out\]
</dt> <dd>

Empfängt die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) der virtuellen Spur.

</dd> <dt>

*welche* 
</dt> <dd>

Priorität der abzurufenden virtuellen Spur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                  | Beschreibung                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Keine virtuelle Spur mit der angegebenen Priorität.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>    |  NULL-Zeigerargument.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Wenn die Methode erfolgreich ist, verfügt die **IAMTimelineObj-Schnittstelle,** die sie zurückgibt, über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie die -Schnittstelle wieder frei geben, wenn Sie sie nicht mehr verwenden.

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

[**IAMTimelineComp-Schnittstelle**](iamtimelinecomp.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




