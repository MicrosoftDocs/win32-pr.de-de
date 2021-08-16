---
description: Die put \_ Similarity-Methode gibt den Bereich der Farbdaten an, der transparent wird. Bei höheren Werten ist ein größerer Bereich ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ RGB oder DXTKEY \_ NONRED ist.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: IDxtKey::p ut_Similarity-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5dbd14b2791441f5c09a7242d6f8c1e343413f8c3cd94fc0519ac6487857b7d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399130"
---
# <a name="idxtkeyput_similarity-method"></a>IDxtKey::p ut \_ Similarity-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_Similarity` -Methode gibt den Bereich der Farbdaten an, der transparent wird. Bei höheren Werten ist ein größerer Bereich ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ RGB oder DXTKEY \_ NONRED ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Gibt den Ähnlichkeitswert an. Der gültige Bereich liegt zwischen 0 und 100.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDxtKey-Schnittstelle**](idxtkey.md)
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




