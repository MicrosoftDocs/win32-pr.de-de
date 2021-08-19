---
description: Die EffectInsBefore-Methode fügt einen Effekt auf der angegebenen Prioritätsebene in das -Objekt ein.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: IAMTimelineEffectable::EffectInsBefore-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0eca93a6c1837b8a7a8f5a95a6cdbf9e87f99191c0911a82e6fd7a3586eb8c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052750"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>IAMTimelineEffectable::EffectInsBefore-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `EffectInsBefore` -Methode fügt einen Effekt auf der angegebenen Prioritätsebene in das -Objekt ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfx* 
</dt> <dd>

Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Effekts.

</dd> <dt>

*Priority* 
</dt> <dd>

Prioritätsebene, auf der der Effekt eingefügt werden soll. Verwenden Sie den Wert –1, um den Effekt am Ende der Prioritätsliste einzufügen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder E \_ NOTIMPL, wenn das Objekt kein Effekt ist. Andernfalls wird ein anderer **HRESULT-Wert** zurückgegeben, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Die Start- und Beendigungszeiten des Effekts werden bei Bedarf innerhalb der Grenzen des Zeitbereichs des Objekts abgeschnitten. Wenn bereits ein Effekt auf der angegebenen Prioritätsebene vorhanden ist, werden alle Auswirkungen von diesem Zeitpunkt an in der Prioritätsliste nach unten verschoben, um Platz für den neuen Effekt zu schaffen.

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

[**IAMTimelineEffectable-Schnittstelle**](iamtimelineeffectable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




