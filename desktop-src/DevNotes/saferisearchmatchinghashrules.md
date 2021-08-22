---
description: Ruft die Ebene einer Hashidentifikationsregel ab, die dem angegebenen Hash entspricht.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: c8b76d2bfbea8b106ea01d5ab4a939c1ebd33048eb5e4654c2a64746895c0df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541480"
---
# <a name="saferisearchmatchinghashrules-function"></a>SaferiSearchMatchingHashRules-Funktion

Ruft die Ebene einer Hashidentifikationsregel ab, die dem angegebenen Hash entspricht.

Diese Funktion verfügt über keine zugeordnete Importbibliothek und wird nicht in einem öffentlichen Header deklariert. Sie müssen einen Funktionszeiger mit der Signatur dieser Funktion definieren, und Sie müssen die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit der Advapi32.dll.

Es wird empfohlen, die [**SaferIdentifyLevel-Funktion zum**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) Auswerten von Richtlinien für Softwareeinschränkungen zu verwenden.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HashAlgorithm* \[ in, optional\]
</dt> <dd>

Der Bezeichner des Algorithmus, der zum Erstellen des Hashs verwendet wird.

</dd> <dt>

*pHashBytes* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das den Hash enthält.

</dd> <dt>

*dwHashSize* \[ In\]
</dt> <dd>

Die Größe des *pHashBytes-Arrays* in Bytes.

</dd> <dt>

*dwOriginalImageSize* \[ in, optional\]
</dt> <dd>

Die Größe des ursprünglichen Bilds in Bytes, aus dem der Hash berechnet wurde.

</dd> <dt>

*pdwFoundLevel* \[ out\]
</dt> <dd>

Ein Zeiger auf den Levelbezeichner für die übereinstimmende Hashidentifikationsregel.

</dd> <dt>

*pdwSaferFlags* 
</dt> <dd>

Reserviert. Legen Sie diesen Wert auf 0 (null) fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn die Funktion erfolgreich ist; andernfalls **FALSE**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
