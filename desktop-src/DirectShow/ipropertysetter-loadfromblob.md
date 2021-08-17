---
description: Die LoadFromBlob-Methode lädt Eigenschaftsdaten aus einem Persistenzformat.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: IPropertySetter::LoadFromBlob-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7deaae82157baf0509f82258d114638b9db501647ad74aaed3ea344c063c5875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397541"
---
# <a name="ipropertysetterloadfromblob-method"></a>IPropertySetter::LoadFromBlob-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `LoadFromBlob` -Methode lädt Eigenschaftsdaten aus einem Persistenzformat.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cSize* \[ In\]
</dt> <dd>

Größe der Daten in Bytes.

</dd> <dt>

*pb* \[ In\]
</dt> <dd>

Zeiger auf ein Bytearray, das die Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

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

[**IPropertySetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




