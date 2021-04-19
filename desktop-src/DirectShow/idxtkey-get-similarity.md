---
description: Die \_ Methode Get Ähnlichkeits Methode ruft den Bereich der Farbdaten ab, der transparent wird. Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Idxtkey:: get_Similarity-Methode (qedit. h)'
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
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366975"
---
# <a name="idxtkeyget_similarity-method"></a>Idxtkey:: get- \_ Ähnlichkeits Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `get_Similarity` Methode ruft den Bereich der Farbdaten ab, der transparent wird. Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt den Ähnlichkeits Wert.

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

 

 




