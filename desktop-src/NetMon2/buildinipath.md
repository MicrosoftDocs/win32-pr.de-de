---
description: Die buildinipath-Funktion gibt einen voll qualifizierten Pfad zu einer INI-Datei zurück, die den von Ihnen eingegebenen Informationen entspricht.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Buildinipath-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368023"
---
# <a name="buildinipath-function"></a><span data-ttu-id="b5019-103">Buildinipath-Funktion</span><span class="sxs-lookup"><span data-stu-id="b5019-103">BuildINIPath function</span></span>

<span data-ttu-id="b5019-104">Die **buildinipath** -Funktion gibt einen voll qualifizierten Pfad zu einer INI-Datei zurück, die den von Ihnen eingegebenen Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b5019-104">The **BuildINIPath** function returns a fully qualified path to an INI file that corresponds to information you enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5019-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5019-105">Syntax</span></span>


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a><span data-ttu-id="b5019-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5019-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5019-107">*FullPath*</span><span class="sxs-lookup"><span data-stu-id="b5019-107">*FullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="b5019-108">Puffer, der den voll qualifizierten Namen der INI-Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="b5019-108">Buffer that receives the fully qualified INI file name.</span></span>

</dd> <dt>

<span data-ttu-id="b5019-109">*Dateiname*</span><span class="sxs-lookup"><span data-stu-id="b5019-109">*IniFileName*</span></span> 
</dt> <dd>

<span data-ttu-id="b5019-110">Name der INI-Datei (der vollständige Dateiname abzüglich der Dateinamenerweiterung).</span><span class="sxs-lookup"><span data-stu-id="b5019-110">Name of the INI file (the full file name minus the filename extension).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5019-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5019-111">Return value</span></span>

<span data-ttu-id="b5019-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den voll qualifizierten Namen der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="b5019-112">If the function is successful, the return value is a pointer to the fully qualified INI file name.</span></span>

<span data-ttu-id="b5019-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="b5019-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5019-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5019-114">Remarks</span></span>

<span data-ttu-id="b5019-115">Der von dieser Funktion zurückgegebene Pfad ist ein voll qualifizierter Pfad zu einer INI-Datei, die den von Ihnen eingegebenen Informationen entspricht.</span><span class="sxs-lookup"><span data-stu-id="b5019-115">The path that this function returns is a fully qualified path to an INI file that corresponds to information you enter.</span></span> <span data-ttu-id="b5019-116">Wenn Sie z. b. XNS oder TCP eingeben, generiert die Funktion einen Pfad zu Xns.ini bzw. Tcp.ini.</span><span class="sxs-lookup"><span data-stu-id="b5019-116">For example, if you enter XNS or TCP, the function generates a path to Xns.ini or Tcp.ini, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5019-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5019-117">Requirements</span></span>



| <span data-ttu-id="b5019-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5019-118">Requirement</span></span> | <span data-ttu-id="b5019-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b5019-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5019-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5019-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5019-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5019-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b5019-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5019-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5019-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5019-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5019-124">Header</span><span class="sxs-lookup"><span data-stu-id="b5019-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5019-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5019-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5019-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b5019-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5019-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5019-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5019-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b5019-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5019-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5019-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




