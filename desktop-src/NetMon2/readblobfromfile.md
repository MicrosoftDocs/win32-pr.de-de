---
description: Die Funktion "leseblobfromfile" liest ein BLOB in einer Datei.
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: Funktion "infoblobfromfile" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355449"
---
# <a name="readblobfromfile-function"></a><span data-ttu-id="43796-103">Read blobfromfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="43796-103">ReadBlobFromFile function</span></span>

<span data-ttu-id="43796-104">Die Funktion " **leseblobfromfile** " liest ein BLOB in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="43796-104">The **ReadBlobFromFile** function reads a BLOB in a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="43796-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43796-105">Syntax</span></span>


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="43796-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43796-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43796-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43796-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43796-108">Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="43796-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="43796-109">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43796-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43796-110">Zeiger auf den Namen der Datei, die das BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="43796-110">Pointer to the name of the file that contains the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43796-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43796-111">Return value</span></span>

<span data-ttu-id="43796-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="43796-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="43796-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="43796-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="43796-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43796-114">Requirements</span></span>



| <span data-ttu-id="43796-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43796-115">Requirement</span></span> | <span data-ttu-id="43796-116">Wert</span><span class="sxs-lookup"><span data-stu-id="43796-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43796-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43796-117">Minimum supported client</span></span><br/> | <span data-ttu-id="43796-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43796-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="43796-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43796-119">Minimum supported server</span></span><br/> | <span data-ttu-id="43796-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43796-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43796-121">Header</span><span class="sxs-lookup"><span data-stu-id="43796-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="43796-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="43796-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="43796-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43796-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="43796-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43796-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="43796-125">DLL</span><span class="sxs-lookup"><span data-stu-id="43796-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43796-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43796-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




