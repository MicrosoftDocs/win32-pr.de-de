---
description: Die Funktion "Write-blobdefile" schreibt ein BLOB in eine Datei.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: Funktion "Write-blobdefile" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349552"
---
# <a name="writeblobtofile-function"></a><span data-ttu-id="8c118-103">Funktion "Write-blobdefile"</span><span class="sxs-lookup"><span data-stu-id="8c118-103">WriteBlobToFile function</span></span>

<span data-ttu-id="8c118-104">Die Funktion " **Write-blobdefile** " schreibt ein BLOB in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="8c118-104">The **WriteBlobToFile** function writes a BLOB to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c118-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c118-105">Syntax</span></span>


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="8c118-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c118-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c118-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c118-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c118-108">Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="8c118-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="8c118-109">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c118-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c118-110">Zeiger auf den Namen der Datei, in der das BLOB gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="8c118-110">Pointer to the name of the file, in which the BLOB is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c118-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c118-111">Return value</span></span>

<span data-ttu-id="8c118-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8c118-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8c118-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="8c118-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c118-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c118-114">Requirements</span></span>



| <span data-ttu-id="8c118-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c118-115">Requirement</span></span> | <span data-ttu-id="8c118-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8c118-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c118-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c118-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c118-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c118-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8c118-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c118-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c118-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c118-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c118-121">Header</span><span class="sxs-lookup"><span data-stu-id="8c118-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c118-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c118-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="8c118-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c118-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c118-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c118-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c118-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8c118-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c118-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c118-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




