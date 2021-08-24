---
title: UtilStringCopyWithAlloc-Funktion (Ndattributils.h)
description: Ordnet eine Quellzeichenfolge zu und kopiert sie.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc-Funktion NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3654fa5eefd45a51d963325e10fbcba765420afe25a5c47a058bbaf4e4093ef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801530"
---
# <a name="utilstringcopywithalloc-function"></a>UtilStringCopyWithAlloc-Funktion

Die **UtilStringCopyWithAlloc-Funktion** ordnet eine Quellzeichenfolge zu und kopiert sie.

## <a name="syntax"></a>Syntax


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Puffer* \[ out\]
</dt> <dd>

Typ: **LPWSTR \***

Der Speicherort, an dem der Zeiger auf den belegten Arbeitsspeicher gespeichert wird. Wenn sie nicht mehr benötigt wird, muss sie mit [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigegeben werden. Dieser Puffer ist immer NULL-terminiert.

</dd> <dt>

*BufferMax* \[ In\]
</dt> <dd>

Typ: **UINT**

Die maximale Anzahl von Zeichen, die aus *der Quelle* gelesen werden sollen.

</dd> <dt>

*Quelle* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Die zu kopierende Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Mögliche Rückgabewerte sind u. a. folgende.



| Rückgabecode                                                                                  | Beschreibung                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde erfolgreich ausgeführt.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

