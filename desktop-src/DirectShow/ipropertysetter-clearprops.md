---
description: Die ClearProps-Methode entfernt alle Eigenschaftsdaten aus dem Eigenschaftens setter. Die Anwendung kann nach dem Aufruf dieser Funktion neue Eigenschaftsdaten festlegen.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: IPropertySetter::ClearProps-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dfe5db4d7ae1f4a2d7a070a3d735264e61dfbdb621f99b9cbb2e1040213b56c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818589"
---
# <a name="ipropertysetterclearprops-method"></a>IPropertySetter::ClearProps-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `ClearProps` -Methode entfernt alle Eigenschaftsdaten aus dem Eigenschaftens setter. Die Anwendung kann nach dem Aufruf dieser Funktion neue Eigenschaftsdaten festlegen.

Durch das Löschen der Eigenschaftsdaten werden die Eigenschaften des Objekts nicht auf die ursprünglichen Werte wiederhergestellt. Dadurch wird lediglich verhindert, dass DirectShow weitere Änderungen anwenden kann. Eigenschaftswerte werden zur Laufzeit angewendet, wenn das Projekt gerendert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPropertySetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




