---
description: Die AddProp-Methode fügt dem Eigenschaftens setter eine Eigenschaft hinzu, mit einem Array von Zeit-Wert-Paaren, die den Wert der Eigenschaft über einen bestimmten Zeitraum definieren.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: IPropertySetter::AddProp-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b2a4cf2f730d177b4eb9323e882d5030c6fc1d658ede574e74d9d222e81d677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818609"
---
# <a name="ipropertysetteraddprop-method"></a>IPropertySetter::AddProp-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode fügt dem Eigenschaftens setter eine -Eigenschaft hinzu, mit einem Array von Zeit-Wert-Paaren, die den Wert der Eigenschaft über einen bestimmten `AddProp` Zeitraum definieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param* \[ In\]
</dt> <dd>

[**DEXTER \_ PARAM-Struktur,**](dexter-param.md) die die -Eigenschaft angibt. Der **nValues-Member** der -Struktur muss der Größe des Arrays im *paValue-Parameter* entspricht.

</dd> <dt>

*paValue* \[ In\]
</dt> <dd>

Zeiger auf ein Array von [**DEXTER \_ VALUE-Strukturen,**](dexter-value.md) die Zeit-Wert-Paare enthalten. Das Array muss in aufsteigender Zeit reihenfolge sein. Die Zeiten sind relativ zur Startzeit des Effekts oder Übergangs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die erste [**DEXTER \_ VALUE-Struktur**](dexter-value.md) muss eine Bezugszeit von 0 (null) und ein Interpolationsflag (**dwInterp**) von **DEXTERF \_ JUMP** angeben, oder die Methode gibt einen Fehler zurück.

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

 

 




