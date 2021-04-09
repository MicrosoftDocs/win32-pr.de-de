---
title: Utilloadstringwithzugsc-Funktion (ndattributils. h)
description: Ordnet eine Zeichenfolge zu und lädt Sie aus der Ressourcen Tabelle.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- Utilloadstringwithzugsc-Funktion NDF
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
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106502"
---
# <a name="utilloadstringwithalloc-function"></a>Utilloadstringwithzugsc-Funktion

Die **utilloadstringwithzucfunktion** ordnet eine Zeichenfolge zu und lädt Sie aus der Ressourcen Tabelle.

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

*UID* \[ in\]
</dt> <dd>

Typ: **uint**

Der Bezeichner der zu ladenden Zeichenfolge.

</dd> <dt>

*ppwzpuffer* \[ vorgenommen\]
</dt> <dd>

Typ: **LPWSTR \** _

Der Speicherort, an dem die neu zugewiesene Zeichenfolge platziert wird. Die Zeichenfolge muss mit [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) freigegeben werden, wenn Sie nicht mehr benötigt wird.

</dd> <dt>

*cchbuffermax* \[ in\]
</dt> <dd>

Typ: **uint**

Die maximale Anzahl von Zeichen, die aus der Ressourcen Tabelle geladen werden sollen. Wenn die Ressourcen Zeichenfolge länger als die angegebene Anzahl von Zeichen ist, wird Sie abgeschnitten und mit Null beendet.

> [!Note]  
> Dieser Parameter darf nicht auf 0 (null) festgelegt werden.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Mögliche Rückgabewerte sind u. a. die folgenden.



| Rückgabecode                                                                                  | Beschreibung                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Vorgang wurde erfolgreich ausgeführt.<br/>                                |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Utilstringcopywithzuzuweisung**](utilstringcopywithalloc.md)
</dt> <dt>

[**Utilassemlestringswithzuweisung**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

