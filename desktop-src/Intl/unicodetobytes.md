---
UID: ''
title: UnicodeToBytes-Funktion
description: Konvertiert Unicode-Zeichen in GB18030 Bytes.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 01109763644dc04aeb398e5fc64e221cd5f3d18870df2654fa5348bc163a277c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764726"
---
# <a name="unicodetobytes-function"></a>UnicodeToBytes-Funktion

## <a name="description"></a>Beschreibung

Veraltet. Konvertiert Unicode-Zeichen in GB18030 Bytes.

**Hinweis:**  Beim Konvertieren von Unicode-Zeichen in GB18030 Bytes sollte eine Anwendung, die unter Windows Vista und höher ausgeführt werden soll, die [WideCharToMultiByte-Funktion](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) verwenden.

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>Parameter

### <a name="lpwidecharstr-in"></a>lpWideCharStr [in]

Zeiger auf die zu konvertierende Unicode-Zeichenfolge.

### <a name="cchwidechar-in"></a>cchWideChar [in]

Zeichenanzahl der zu konvertierenden Unicode-Zeichenfolge.

### <a name="lpmultibytestr-in"></a>lpMultiByteStr [in]

Zeiger auf den Ziel-Multibytepuffer.
Wenn *lpMultiByteStr* 0 ist, wird die Byteanzahl des Gb18030-Ergebnisses zurückgegeben, und es wird keine Konvertierung durchgeführt.

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

Byteanzahl des Ziel-Multibytepuffers.
Wenn *cchMultiByte* 0 ist, wird die Byteanzahl des GB18030-Ergebnisses zurückgegeben, und es wird keine Konvertierung durchgeführt.

## <a name="returns"></a>Gibt zurück

Gibt bei Erfolg die Byteanzahl der generierten Multibytezeichen zurück.

## <a name="remarks"></a>Hinweise

## <a name="see-also"></a>Weitere Informationen

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
