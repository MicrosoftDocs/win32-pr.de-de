---
description: Die get \_ Invert-Methode ruft einen booleschen Wert ab, der angibt, ob der Schlüssel Vorgang invertiert wird. Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Idxtkey:: get_Invert-Methode (qedit. h)'
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
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359316"
---
# <a name="idxtkeyget_invert-method"></a>Idxtkey:: get \_ Invert-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_Invert` Methode ruft einen booleschen Wert ab, der angibt, ob der Schlüssel Vorgang invertiert wird. Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt einen der folgenden Werte.



| Wert     | BESCHREIBUNG                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | Pixel im überlappenden Bild werden in Bezug auf den Standard Vorgang invertiert. |
| **FALSE** | Pixel im überliegenden Bild werden standardmäßig transparent gemacht.         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

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

[**Idxtkey-Schnittstelle**](idxtkey.md)
</dt> <dt>

[**Idxtkey:: get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




