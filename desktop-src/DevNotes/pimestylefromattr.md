---
description: Ruft Stile für ein angegebenes Attribut ab.
ms.assetid: 206c69b9-981b-49ef-9f71-1c65e08637bb
title: Pimestylefromattr-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PIMEStyleFromAttr
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 27673ebb74c1dca3e686542a541735cfc515bee9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365937"
---
# <a name="pimestylefromattr-function"></a><span data-ttu-id="7778e-103">Pimestylefromattr-Funktion</span><span class="sxs-lookup"><span data-stu-id="7778e-103">PIMEStyleFromAttr function</span></span>

<span data-ttu-id="7778e-104">Ruft Stile für ein angegebenes Attribut ab.</span><span class="sxs-lookup"><span data-stu-id="7778e-104">Retrieves styles for a given attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="7778e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7778e-105">Syntax</span></span>


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a><span data-ttu-id="7778e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7778e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7778e-107">*attr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7778e-107">*attr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7778e-108">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="7778e-108">This parameter can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7778e-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**Imesattr \_ Fixedkonvertierte** (5)</span><span class="sxs-lookup"><span data-stu-id="7778e-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR\_FIXEDCONVERTED** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7778e-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**Imesattr \_ Eingabe** (0)</span><span class="sxs-lookup"><span data-stu-id="7778e-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR\_INPUT** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7778e-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**Imesattr \_ Eingabe \_ Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="7778e-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR\_INPUT\_ERROR** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7778e-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**Imesattr \_ Max** (5)</span><span class="sxs-lookup"><span data-stu-id="7778e-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR\_MAX** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7778e-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**Imesattr \_ MIN** (0)</span><span class="sxs-lookup"><span data-stu-id="7778e-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR\_MIN** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7778e-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**Imesattr \_ Ziel \_ konvertiert** (1)</span><span class="sxs-lookup"><span data-stu-id="7778e-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR\_TARGET\_CONVERTED** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7778e-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**Imesattr \_ Ziel nicht \_ konvertiert** (4)</span><span class="sxs-lookup"><span data-stu-id="7778e-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR\_TARGET\_NOTCONVERTED** (4)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7778e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7778e-116">Return value</span></span>

<span data-ttu-id="7778e-117">Gibt einen Zeiger auf eine **imestyle** -Struktur zurück, die die Farb-und die nicht-Farbeinstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="7778e-117">Returns a pointer to an **IMESTYLE** structure representing the color and non-color settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="7778e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7778e-118">Remarks</span></span>

<span data-ttu-id="7778e-119">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7778e-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="7778e-120">Die **imestyle** -Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="7778e-120">The **IMESTYLE** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    union {
        GRFSTY  grfsty;
        struct {
            UINT    fBold:1;
            UINT    fItalic:1;
            UINT    fUl:1;
            UINT    idUl:(sizeof(UINT) * 8 - 3);
        };
    };

    union {
        IMECOLORSTY colorstyText;
        struct {
            UINT    colorIdText;
            union {
                COLORREF    rgbText;
                UINT        colorWinText;
                UINT        colorSpecText;
                UINT        colorFundText;
            };
        };
    };

    union {
        IMECOLORSTY colorstyBack;
        struct {
            UINT    colorIdBack;
            union {
                COLORREF    rgbBack;
                UINT        colorWinBack;
                UINT        colorSpecBack;
                UINT        colorFundBack;
            };
        };
    };

    union {
        IMECOLORSTY colorstyUl;
        struct {
            UINT    colorIdUl;
            union {
                COLORREF    rgbUl;
                UINT        colorWinUl;
                UINT        colorSpecUl;
                UINT        colorFundUl;
            };
        };
    };
} IMESTYLE;
```

## <a name="requirements"></a><span data-ttu-id="7778e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7778e-121">Requirements</span></span>



| <span data-ttu-id="7778e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7778e-122">Requirement</span></span> | <span data-ttu-id="7778e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7778e-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7778e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7778e-124">DLL</span></span><br/> | <dl> <span data-ttu-id="7778e-125"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7778e-125"><dt>Imeshare.dll</dt></span></span> </dl> |



 

 
