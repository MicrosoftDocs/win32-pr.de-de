---
UID: ''
title: Unicodeto Bytes-Funktion
description: Konvertiert Unicode-Zeichen in GB18030 bytes.
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
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "103719952"
---
# <a name="unicodetobytes-function"></a>Unicodeto Bytes-Funktion

## <a name="description"></a>BESCHREIBUNG

Veraltet. Konvertiert Unicode-Zeichen in GB18030 bytes.

**Hinweis**  Beim Umrechnen von Unicode-Zeichen in GB18030 Bytes sollte eine Anwendung, die unter Windows Vista und höher ausgeführt werden soll, die [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) -Funktion verwenden.

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>Parameter

### <a name="lpwidecharstr-in"></a>lpwidecharstr [in]

Zeiger auf die zu konvertierende Unicode-Zeichenfolge.

### <a name="cchwidechar-in"></a>cchwidechar [in]

Zeichen Anzahl der zu konvertierenden Unicode-Zeichenfolge.

### <a name="lpmultibytestr-in"></a>lpmultibytestr [in]

Zeiger auf den Ziel-multibytepuffer.
Wenn *lpmultibytestr* den Wert 0 hat, wird die Byte Anzahl des GB18030-Ergebnisses zurückgegeben, und es wird keine Konvertierung durchgeführt.

### <a name="cchmultibyte-in"></a>cchmultibyte [in]

Byte Anzahl des Ziel-multibytepuffers.
Wenn *cchmultibyte* den Wert 0 hat, wird die Byte Anzahl des GB18030-Ergebnisses zurückgegeben, und es wird keine Konvertierung durchgeführt.

## <a name="returns"></a>Gibt zurück

Gibt die Byte Anzahl der Multibytezeichen zurück, die generiert werden, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

## <a name="see-also"></a>Siehe auch

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
