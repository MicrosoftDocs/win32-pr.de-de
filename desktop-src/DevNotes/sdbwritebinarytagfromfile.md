---
description: Schreibt Binärdaten aus der angegebenen Datei in die angegebene Datenbank.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: Sdbschreitebinarytagfromfile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958280"
---
# <a name="sdbwritebinarytagfromfile-function"></a><span data-ttu-id="18b88-103">Sdbschreitebinarytagfromfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="18b88-103">SdbWriteBinaryTagFromFile function</span></span>

<span data-ttu-id="18b88-104">Schreibt Binärdaten aus der angegebenen Datei in die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="18b88-104">Writes binary data from the specified file to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b88-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18b88-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a><span data-ttu-id="18b88-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18b88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b88-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18b88-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b88-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="18b88-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="18b88-109">*ttag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18b88-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b88-110">Das-Tag für den Eintrag.</span><span class="sxs-lookup"><span data-stu-id="18b88-110">The TAG for the entry.</span></span> <span data-ttu-id="18b88-111">Dieses Tag muss vom Typ " **Tag \_ Type \_ Binary**" sein.</span><span class="sxs-lookup"><span data-stu-id="18b88-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="18b88-112">*pwszpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18b88-112">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b88-113">Der Pfad zu der Datei, die die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="18b88-113">The path to the file that contains the data.</span></span> <span data-ttu-id="18b88-114">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="18b88-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b88-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18b88-115">Return value</span></span>

<span data-ttu-id="18b88-116">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="18b88-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b88-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18b88-117">Requirements</span></span>



| <span data-ttu-id="18b88-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18b88-118">Requirement</span></span> | <span data-ttu-id="18b88-119">Wert</span><span class="sxs-lookup"><span data-stu-id="18b88-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18b88-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18b88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="18b88-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18b88-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18b88-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18b88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="18b88-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18b88-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="18b88-124">DLL</span><span class="sxs-lookup"><span data-stu-id="18b88-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18b88-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18b88-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b88-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18b88-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b88-127">**Sdbschreitebinarytag**</span><span class="sxs-lookup"><span data-stu-id="18b88-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> </dl>

 

 




