---
description: Die SetProps-Methode legt die Eigenschaften des Zielobjekts für die angegebene Zeit auf den entsprechenden Zustand fest.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: IPropertySetter::SetProps-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3b5a1832897b52d21c57e26595b7d66c4fc9a53f2bcbee0090c53d00f8fe832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767210"
---
# <a name="ipropertysettersetprops-method"></a>IPropertySetter::SetProps-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetProps` -Methode legt die Eigenschaften des Zielobjekts für die angegebene Zeit auf den entsprechenden Zustand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTarget* \[ In\]
</dt> <dd>

Zeiger auf das Zielobjekt, für das die Eigenschaften festgelegt werden.

</dd> <dt>

*rtNow* \[ In\]
</dt> <dd>

Die Zeit, zu der die Eigenschaften in Einheiten von 100 Nanosekunden oder –1 festgelegt werden, um statische Eigenschaften (die im Laufe der Zeit nicht variieren) zu setzen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird von DES aufgerufen, um die Eigenschaften für einen Übergang oder Effekt festlegen. Eine Anwendung wird diese Methode normalerweise nicht aufrufen.

Das von *pTarget angegebene Objekt* muss die **IDispatch-Schnittstelle** implementieren.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPropertySetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




