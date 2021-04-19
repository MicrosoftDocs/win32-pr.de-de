---
description: Gibt eine Datei an, die signiert werden soll.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: SIGNER_FILE_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362926"
---
# <a name="signer_file_info-structure"></a><span data-ttu-id="78cb5-103">Struktur der Signatur Geber \_ Datei \_</span><span class="sxs-lookup"><span data-stu-id="78cb5-103">SIGNER\_FILE\_INFO structure</span></span>

<span data-ttu-id="78cb5-104">Die **Signatur Geber \_ Datei \_ Info** -Struktur gibt eine zu Signier ender Datei an.</span><span class="sxs-lookup"><span data-stu-id="78cb5-104">The **SIGNER\_FILE\_INFO** structure specifies a file to sign.</span></span>

> [!Note]  
> <span data-ttu-id="78cb5-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="78cb5-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="78cb5-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="78cb5-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="78cb5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78cb5-107">Syntax</span></span>


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a><span data-ttu-id="78cb5-108">Member</span><span class="sxs-lookup"><span data-stu-id="78cb5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="78cb5-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="78cb5-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="78cb5-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="78cb5-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="78cb5-111">**pwszFileName**</span><span class="sxs-lookup"><span data-stu-id="78cb5-111">**pwszFileName**</span></span>
</dt> <dd>

<span data-ttu-id="78cb5-112">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen der zu Signier enden Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="78cb5-112">A pointer to a null-terminated string that contains the name of the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="78cb5-113">**hFile**</span><span class="sxs-lookup"><span data-stu-id="78cb5-113">**hFile**</span></span>
</dt> <dd>

<span data-ttu-id="78cb5-114">Ein geöffnetes Handle für die Datei, die vom **pwszFileName** -Member angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="78cb5-114">An open handle to the file specified by the **pwszFileName** member.</span></span> <span data-ttu-id="78cb5-115">Wenn dieser Member ein gültiges Handle enthält, wird dieser Handle für den Zugriff auf die Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="78cb5-115">If this member contains a valid handle, this handle is used to access the file.</span></span> <span data-ttu-id="78cb5-116">Dieser Member kann auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="78cb5-116">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78cb5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78cb5-117">Requirements</span></span>



| <span data-ttu-id="78cb5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78cb5-118">Requirement</span></span> | <span data-ttu-id="78cb5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="78cb5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78cb5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78cb5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78cb5-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78cb5-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="78cb5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78cb5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="78cb5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78cb5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78cb5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78cb5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78cb5-125">**Betreff- \_ Informationen des Signatur Gebers \_**</span><span class="sxs-lookup"><span data-stu-id="78cb5-125">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 




