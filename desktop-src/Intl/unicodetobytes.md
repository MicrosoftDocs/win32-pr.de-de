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
# <a name="unicodetobytes-function"></a><span data-ttu-id="dba35-103">Unicodeto Bytes-Funktion</span><span class="sxs-lookup"><span data-stu-id="dba35-103">UnicodeToBytes function</span></span>

## <a name="description"></a><span data-ttu-id="dba35-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dba35-104">Description</span></span>

<span data-ttu-id="dba35-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="dba35-105">Deprecated.</span></span> <span data-ttu-id="dba35-106">Konvertiert Unicode-Zeichen in GB18030 bytes.</span><span class="sxs-lookup"><span data-stu-id="dba35-106">Converts Unicode characters to GB18030 bytes.</span></span>

<span data-ttu-id="dba35-107">**Hinweis**  Beim Umrechnen von Unicode-Zeichen in GB18030 Bytes sollte eine Anwendung, die unter Windows Vista und höher ausgeführt werden soll, die [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="dba35-107">**Note**  When converting Unicode characters to GB18030 bytes, an application to run on Windows Vista and later should use the [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function.</span></span>

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a><span data-ttu-id="dba35-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dba35-108">Parameters</span></span>

### <a name="lpwidecharstr-in"></a><span data-ttu-id="dba35-109">lpwidecharstr [in]</span><span class="sxs-lookup"><span data-stu-id="dba35-109">lpWideCharStr [in]</span></span>

<span data-ttu-id="dba35-110">Zeiger auf die zu konvertierende Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dba35-110">Pointer to the Unicode string to convert.</span></span>

### <a name="cchwidechar-in"></a><span data-ttu-id="dba35-111">cchwidechar [in]</span><span class="sxs-lookup"><span data-stu-id="dba35-111">cchWideChar [in]</span></span>

<span data-ttu-id="dba35-112">Zeichen Anzahl der zu konvertierenden Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dba35-112">Character count of the Unicode string to convert.</span></span>

### <a name="lpmultibytestr-in"></a><span data-ttu-id="dba35-113">lpmultibytestr [in]</span><span class="sxs-lookup"><span data-stu-id="dba35-113">lpMultiByteStr [in]</span></span>

<span data-ttu-id="dba35-114">Zeiger auf den Ziel-multibytepuffer.</span><span class="sxs-lookup"><span data-stu-id="dba35-114">Pointer to the target multibyte buffer.</span></span>
<span data-ttu-id="dba35-115">Wenn *lpmultibytestr* den Wert 0 hat, wird die Byte Anzahl des GB18030-Ergebnisses zurückgegeben, und es wird keine Konvertierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="dba35-115">If *lpMultiByteStr* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

### <a name="cchmultibyte-in"></a><span data-ttu-id="dba35-116">cchmultibyte [in]</span><span class="sxs-lookup"><span data-stu-id="dba35-116">cchMultiByte [in]</span></span>

<span data-ttu-id="dba35-117">Byte Anzahl des Ziel-multibytepuffers.</span><span class="sxs-lookup"><span data-stu-id="dba35-117">Byte count of the target multibyte buffer.</span></span>
<span data-ttu-id="dba35-118">Wenn *cchmultibyte* den Wert 0 hat, wird die Byte Anzahl des GB18030-Ergebnisses zurückgegeben, und es wird keine Konvertierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="dba35-118">If *cchMultiByte* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

## <a name="returns"></a><span data-ttu-id="dba35-119">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="dba35-119">Returns</span></span>

<span data-ttu-id="dba35-120">Gibt die Byte Anzahl der Multibytezeichen zurück, die generiert werden, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dba35-120">Returns the byte count of the multibyte characters that are generated, if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba35-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dba35-121">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="dba35-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dba35-122">See also</span></span>

[<span data-ttu-id="dba35-123">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="dba35-123">WideCharToMultiByte</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[<span data-ttu-id="dba35-124">MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="dba35-124">MultiByteToWideChar</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
