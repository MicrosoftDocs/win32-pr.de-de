---
title: Utilstringcopywithzuzuordnungsfunktion (ndattributils. h)
description: Ordnet eine Quell Zeichenfolge zu und kopiert sie.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Utilstringcopywithzuzuordnungsfunktion NDF
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
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340577"
---
# <a name="utilstringcopywithalloc-function"></a>Utilstringcopywithzuzuordnungsfunktion

Die Funktion " **utilstringcopywithzuzuordnungs** " weist eine Quell Zeichenfolge zu und kopiert sie.

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

*Puffer* \[ vorgenommen\]
</dt> <dd>

Typ: **LPWSTR \** _

Der Speicherort, an dem der Zeiger auf den zugeordneten Arbeitsspeicher gespeichert wird. Wenn Sie nicht mehr benötigt wird, muss Sie mit [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigegeben werden. Dieser Puffer wird immer mit Null beendet.

</dd> <dt>

*Buffermax* \[ in\]
</dt> <dd>

Typ: **uint**

Die maximale Anzahl von Zeichen, die aus der *Quelle* gelesen werden sollen.

</dd> <dt>

*Quelle* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Die zu kopierende Zeichenfolge.

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

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**Utilassemlestringswithzuweisung**](utilassemblestringswithalloc.md)
</dt> <dt>

[**Utilloadstringwithzuordc**](utilloadstringwithalloc.md)
</dt> </dl>

 

