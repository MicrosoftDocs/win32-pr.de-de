---
description: Die Put- \_ Ähnlichkeits Methode gibt den Bereich der Farbdaten an, der transparent wird. Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: Idxtkey::p ut_Similarity-Methode (qedit. h)
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
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366759"
---
# <a name="idxtkeyput_similarity-method"></a>Idxtkey::p UT- \_ Ähnlichkeits Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `put_Similarity` Methode gibt den Bereich der Farbdaten an, der transparent wird. Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Gibt den Ähnlichkeits Wert an. Der gültige Bereich liegt zwischen 0 und 100.

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

[**Idxtkey::p UT- \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




