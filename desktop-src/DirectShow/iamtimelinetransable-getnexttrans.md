---
description: Die GetNextTrans-Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: IAMTimelineTransable::GetNextTrans-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 892f8e0f4af39250d62da9ed662c22867f98ebfc32baeaa0f341ead2eef665a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131080"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>IAMTimelineTransable::GetNextTrans-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetNextTrans` -Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppTrans* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Übergangsobjekts.

</dd> <dt>

*Pinout* 
</dt> <dd>

Zeiger auf eine Variable, die die Zeit in Einheiten von 100 Nanosekunden angibt. Bei der Eingabe gibt dieser Wert die Zeit an, ab der der Übergang zu finden ist. Wenn bei der Ausgabe ein Übergang abgerufen wird, wird dieser Wert auf die Stoppzeit des Übergangs festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode einen Übergang abruft, oder S FALSE, wenn \_ sie keinen Übergang findet. Andernfalls gibt einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Die Startzeit des Übergangs kann kleiner als die Zeit sein, die Sie in *pInOut* angeben, wenn der Übergang die angegebene Zeit überdauert.

Wenn die Methode S \_ OK zurückgibt, verfügt [**die IAMTimelineObj-Schnittstelle,**](iamtimelineobj.md) die sie zurückgibt, über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie die -Schnittstelle wieder frei geben, wenn Sie sie nicht mehr verwenden.

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

[**IAMTimelineTransable-Schnittstelle**](iamtimelinetransable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




