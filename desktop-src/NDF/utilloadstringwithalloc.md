---
title: UtilLoadStringWithAlloc-Funktion (Ndattributils.h)
description: Ordnet eine Zeichenfolge aus der Ressourcentabelle zu und lädt sie.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc-Funktion NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca649599e2a8a29ecdab2dbbfe2c188947b40487ceb82ab4937622ce82c701a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685610"
---
# <a name="utilloadstringwithalloc-function"></a>UtilLoadStringWithAlloc-Funktion

Die **UtilLoadStringWithAlloc-Funktion** ordnet eine Zeichenfolge zu und lädt sie aus der Ressourcentabelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uID* \[ In\]
</dt> <dd>

Typ: **UINT**

Bezeichner der zu ladenden Zeichenfolge.

</dd> <dt>

*ppwzBuffer* \[ out\]
</dt> <dd>

Typ: **LPWSTR \***

Der Speicherort, an dem die neu zugeordnete Zeichenfolge platziert wird. Die Zeichenfolge muss mit [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) freigegeben werden, wenn sie nicht mehr benötigt wird.

</dd> <dt>

*cchBufferMax* \[ In\]
</dt> <dd>

Typ: **UINT**

Die maximale Anzahl von Zeichen, die aus der Ressourcentabelle geladen werden sollen. Wenn die Ressourcenzeichenfolge länger als die angegebene Anzahl von Zeichen ist, wird sie abgeschnitten und mit NULL beendet.

> [!Note]  
> Dieser Parameter kann nicht auf 0 (null) festgelegt werden.

 

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

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

