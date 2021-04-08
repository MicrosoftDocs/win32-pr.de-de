---
title: Utilassemlestringswithzuc-Funktion (ndattributils. h)
description: Ordnet eine Zeichenfolge zu und formatiert Sie mithilfe von Zeichen folgen, die in der Zeichen folgen Tabelle angegeben sind Diese Funktion verwendet StringCchPrintf, um die formatierte Zeichenfolge zu erstellen.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- Utilassemlestringswithzuweisung-Funktion NDF
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
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743881"
---
# <a name="utilassemblestringswithalloc-function"></a>Utilassemlestringswithzuweisung-Funktion

Die **utilassemlestringswithzuweisung** -Funktion ordnet eine Zeichenfolge zu und formatiert Sie mithilfe von Zeichen folgen, die von der Zeichen folgen Tabelle bereitgestellt werden. Diese Funktion verwendet [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) , um die formatierte Zeichenfolge zu erstellen.

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

*Puffer* \[ vorgenommen\]
</dt> <dd>

Typ: **LPWSTR \** _

Der Speicherort, an dem die neu zugewiesene Zeichenfolge platziert wird. Wenn die Zeichenfolge nicht mehr benötigt wird, muss Sie mit [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigegeben werden.

</dd> <dt>

*Buffermax* \[ in\]
</dt> <dd>

Typ: **uint**

Die maximale Anzahl von Zeichen, die in der durch den *Puffer* zugeordneten Zeichenfolge zulässig sind. Wenn die resultierende formatierte Zeichenfolge länger als die angegebene Anzahl von Zeichen ist, wird Sie abgeschnitten und mit Null beendet.

> [!Note]  
> Dieser Parameter darf nicht auf 0 (null) festgelegt werden.

 

</dd> <dt>

*Input Format* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Zeichen folgen Ressource aus der Zeichen folgen Tabelle, die einen an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)übergebenen Format Parameter darstellt. Sie wird mit [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)erstellt.

Das Format der Ressourcen Zeichenfolge muss entweder einen Format Parameter angeben, der eine Breite Zeichenfolge annimmt, oder einen Format Parameter, der eine Zeichenfolge ohne Vorzeichen und eine Breite Zeichenfolge annimmt.

</dd> <dt>

*Input String* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Zeichen folgen Ressource aus der Zeichen folgen Tabelle, die ein an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) übergebener Argument anstelle der breiten Zeichenfolge im Format-Parameter darstellt. Sie wird mit [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)erstellt.

</dd> <dt>

*Additionalargument* \[ in\]
</dt> <dd>

Typ: **Boolean**

True, wenn *additionalvalue* als erstes Formatierungs Argument an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)übergeben werden soll. andernfalls false (und nur die durch *InputString* identifizierte Ressourcen Zeichenfolge).

</dd> <dt>

*Additionalvalue* \[ in\]
</dt> <dd>

Typ: **ulong**

Der Wert, der als erstes Formatierungs Argument an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) übergeben werden soll, wenn *additionalargument* auf true festgelegt ist.

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

[**Utilloadstringwithzuordc**](utilloadstringwithalloc.md)
</dt> <dt>

[**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**Makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

