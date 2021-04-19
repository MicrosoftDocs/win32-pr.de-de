---
description: Die addprop-Methode fügt dem Eigenschaften Setter eine Eigenschaft mit einem Array von Zeit-Wert-Paaren hinzu, das den Wert der Eigenschaft für einen Zeitraum definiert.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Ipropertysetter:: addprop-Methode (qedit. h)'
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
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372259"
---
# <a name="ipropertysetteraddprop-method"></a>Ipropertysetter:: addprop-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `AddProp` Methode fügt dem Eigenschaften Setter eine Eigenschaft mit einem Array von Zeit-Wert-Paaren hinzu, das den Wert der-Eigenschaft für einen Zeitraum definiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Param* \[ in\]
</dt> <dd>

[**Dexter \_ Param**](dexter-param.md) -Struktur, die die Eigenschaft angibt. Der **nvalues** -Member der-Struktur muss der Größe des Arrays entsprechen *, das im Parameter "* Parameter" angegeben ist.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Zeiger auf ein Array von [**Dexter- \_ Wert**](dexter-value.md) -Strukturen, die Zeit Wert Paare enthalten. Das Array muss sich in aufsteigender Zeitreihen Folge befinden. Die Uhrzeiten sind relativ zur Startzeit des Effekts oder Übergangs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die erste [**\_ Wert**](dexter-value.md) Struktur von "Dexter" muss eine Verweis Zeit von 0 (null) und ein Interpolations Flag (**dwinterp**) von **dexterf \_**, oder die Methode gibt einen Fehler zurückgeben.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipropertysetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




