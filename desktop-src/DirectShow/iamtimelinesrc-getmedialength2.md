---
description: Die GetMediaLength2-Methode ruft die Medienlänge dieses Quellobjekts ab. Diese Methode entspricht IAMTimelineSrc::GetMediaLength, nimmt jedoch REFTIME-Werte an.
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: IAMTimelineSrc::GetMediaLength2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 951e7909d55517489c77190434bf677ccdd8bee8dc1238ecd247d117a551610a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131110"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a>IAMTimelineSrc::GetMediaLength2-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetMediaLength2` -Methode ruft die Medienlänge dieses Quellobjekts ab. Diese Methode entspricht [**IAMTimelineSrc::GetMediaLength,**](iamtimelinesrc-getmedialength.md)nimmt jedoch [**REFTIME-Werte**](reftime.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pLength* 
</dt> <dd>

Empfängt die Medienlänge in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                     | Beschreibung                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Erfolg.<br/>                                |
| <dl> <dt>**E \_ NOTDETERMINED**</dt> </dl> | Für dieses Objekt sind keine Medienzeiten festgelegt.<br/> |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>       |  NULL-Zeigerargument.<br/>              |



 

## <a name="remarks"></a>Hinweise

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

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




