---
description: Die get \_ Invert-Methode ruft einen booleschen Wert ab, der angibt, ob der Schlüsselvorgang invertiert ist. Diese Eigenschaft gilt für alle Schlüsseltypen außer DXTKEY \_ ALPHA.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: IDxtKey::get_Invert-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c5a862e062175d3c052a5003a2ced60fe5d3cc439bff76315e046fc2153f73af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083850"
---
# <a name="idxtkeyget_invert-method"></a>IDxtKey::get \_ Invert-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `get_Invert` -Methode ruft einen booleschen Wert ab, der angibt, ob der Schlüsselvorgang invertiert ist. Diese Eigenschaft gilt für alle Schlüsseltypen außer DXTKEY \_ ALPHA.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt einen der folgenden Werte.



| Wert     | BESCHREIBUNG                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | Pixel im übermäßig großen Bild werden in Bezug auf den Standardvorgang invertiert. |
| **FALSE** | Pixel im überhändigen Bild werden standardmäßig transparent gemacht.         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDxtKey-Schnittstelle**](idxtkey.md)
</dt> <dt>

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




