---
title: UtilAssembleStringsWithAlloc-Funktion (Ndattributils.h)
description: Ordnet eine Zeichenfolge zu und formatiert sie mithilfe von Zeichenfolgen, die von der Zeichenfolgentabelle bereitgestellt werden. Diese Funktion verwendet StringCchPrintf, um die formatierte Zeichenfolge zu erstellen.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc-Funktion NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38473f45e2bd4c53b964bb38ec285cdf3eea091a96d72684c1d801b949f4d0a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801730"
---
# <a name="utilassemblestringswithalloc-function"></a>UtilAssembleStringsWithAlloc-Funktion

Die **UtilAssembleStringsWithAlloc-Funktion** ordnet eine Zeichenfolge zu und formatiert sie mithilfe von Zeichenfolgen, die von der Zeichenfolgentabelle bereitgestellt werden. Diese Funktion verwendet [**StringCchPrintf,**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) um die formatierte Zeichenfolge zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Puffer* \[ out\]
</dt> <dd>

Typ: **LPWSTR \***

Der Speicherort, an dem die neu zugeordnete Zeichenfolge platziert wird. Wenn die Zeichenfolge nicht mehr benötigt wird, muss sie mit [**CoTaskMemFree freigegeben werden.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*BufferMax* \[ In\]
</dt> <dd>

Typ: **UINT**

Die maximale Anzahl von Zeichen, die in der von Buffer zugeordneten Zeichenfolge *zulässig sind.* Wenn die resultierende formatierte Zeichenfolge länger als die angegebene Anzahl von Zeichen ist, wird sie abgeschnitten und auf NULL beendet.

> [!Note]  
> Dieser Parameter darf nicht auf 0 (null) festgelegt werden.

 

</dd> <dt>

*InputFormat* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Eine Zeichenfolgenressource aus der Zeichenfolgentabelle, die einen format-Parameter darstellt, der [**an StringCchPrintf übergeben wird.**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) Sie wird mit [**MAKEINTRESOURCE erstellt.**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)

Das Format der Ressourcenzeichenfolge muss entweder einen Formatparameter angeben, der eine breite Zeichenfolge akzeptiert, oder einen Formatparameter, der eine lange und eine breite Zeichenfolge ohne Vorzeichen akzeptiert.

</dd> <dt>

*InputString* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Eine Zeichenfolgenressource aus der Zeichenfolgentabelle, die ein Argument darstellt, das an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) statt der breiten Zeichenfolge im Formatparameter übergeben wird. Sie wird mit [**MAKEINTRESOURCE erstellt.**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)

</dd> <dt>

*AdditionalArgument* \[ In\]
</dt> <dd>

Typ: **BOOLEAN**

True, *wenn AdditionalValue* als erstes Formatierungsargument an [**StringCchPrintf übergeben werden soll.**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) andernfalls false (und nur die von *InputString* identifizierte Ressourcenzeichenfolge wird übergeben).

</dd> <dt>

*AdditionalValue* \[ In\]
</dt> <dd>

Typ: **ULONG**

Der Wert, der als erstes Formatierungsargument an [**StringCchPrintf übergeben**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) werden soll, wenn *AdditionalArgument* true ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Mögliche Rückgabewerte sind u. a. folgende:



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

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> <dt>

[**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

