---
description: Die TransAdd-Methode fügt dem -Objekt einen Übergang hinzu. Ein Objekt kann mehrere Übergänge aufweisen, darf sich jedoch nicht zeitlich überschneiden. Übergänge müssen innerhalb der Zeitgrenzen des Objekts liegen.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: IAMTimelineTransable::TransAdd-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 930c3ff43e11cfb71ffce6c7257d0124fe87aeaaf4ae065433f11b860020eeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952749"
---
# <a name="iamtimelinetransabletransadd-method"></a>IAMTimelineTransable::TransAdd-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `TransAdd` -Methode fügt dem -Objekt einen Übergang hinzu. Ein Objekt kann mehrere Übergänge aufweisen, darf sich jedoch nicht zeitlich überschneiden. Übergänge müssen innerhalb der Zeitgrenzen des Objekts liegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTrans* 
</dt> <dd>

Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des übergangs, der hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                   | Beschreibung                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der Übergang kann nicht eingefügt werden.<br/>              |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *pTrans* ist kein Zeiger auf einen Übergang.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn der Übergang einen vorhandenen Übergang überlappt, gibt die Methode E \_ INVALIDARG zurück.

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

[**IAMTimelineTransable-Schnittstelle**](iamtimelinetransable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




