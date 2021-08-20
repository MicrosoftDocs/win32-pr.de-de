---
description: Die get \_ Similarity-Methode ruft den Bereich der Farbdaten ab, die transparent werden. Bei höheren Werten ist ein größerer Bereich ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ RGB oder DXTKEY \_ NONRED ist.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: IDxtKey::get_Similarity-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dda31145fe28f0b428189eafd3105ae56120fbc19e0c611ad0df8d9f511130a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399140"
---
# <a name="idxtkeyget_similarity-method"></a>IDxtKey::get \_ Similarity-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `get_Similarity` -Methode ruft den Bereich der Farbdaten ab, der transparent wird. Bei höheren Werten ist ein größerer Bereich ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ RGB oder DXTKEY \_ NONRED ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt den Ähnlichkeitswert.

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

[**IDxtKey-Schnittstelle**](idxtkey.md)
</dt> <dt>

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




