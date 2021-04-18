---
description: Ruft den Mac-Typ aus der Kategorie networkinfo des NPP-Abschnitts des BLOBs ab und konvertiert die Typdaten in eine Mac-Typnummer.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Getnppmactybäuernumber-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525133"
---
# <a name="getnppmactypeasnumber-function"></a><span data-ttu-id="1c93a-103">Getnppmactybäuernumber-Funktion</span><span class="sxs-lookup"><span data-stu-id="1c93a-103">GetNPPMacTypeAsNumber function</span></span>

<span data-ttu-id="1c93a-104">Die **getnppmactybäuernumber** -Funktion Ruft den Mac-Typ aus der Kategorie networkinfo des NPP-Abschnitts des BLOBs ab und konvertiert die Typdaten in eine Mac-Typnummer.</span><span class="sxs-lookup"><span data-stu-id="1c93a-104">The **GetNPPMacTypeAsNumber** function retrieves the MAC type from the NetworkInfo category of the NPP section of the BLOB and converts the type data into a MAC type number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c93a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c93a-105">Syntax</span></span>


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a><span data-ttu-id="1c93a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c93a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c93a-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c93a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c93a-108">Ein Handle für das angegebene BLOB.</span><span class="sxs-lookup"><span data-stu-id="1c93a-108">A handle to the specified BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="1c93a-109">*lpmactype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1c93a-109">*lpMacType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c93a-110">Ein Zeiger auf den Mac-Typ.</span><span class="sxs-lookup"><span data-stu-id="1c93a-110">A pointer to the MAC type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c93a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c93a-111">Return value</span></span>

<span data-ttu-id="1c93a-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1c93a-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1c93a-113">Wenn das Tag nicht verfügbar ist, lautet der Rückgabewert "Mac- \_ Typ \_ unbekannt".</span><span class="sxs-lookup"><span data-stu-id="1c93a-113">If the tag is unavailable, the return value is MAC\_TYPE\_UNKNOWN.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c93a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c93a-114">Remarks</span></span>

<span data-ttu-id="1c93a-115">Diese Funktion ordnet das Tag **NPP: networkinfo: MacType** dem Mac- **\_ Typ \_ \*** zu, wie in der Datei npptypes. h definiert.</span><span class="sxs-lookup"><span data-stu-id="1c93a-115">This function maps the tag, **NPP:NetworkInfo:MacType** to the **MAC\_TYPE\_\*** as defined in the Npptypes.h file.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c93a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c93a-116">Requirements</span></span>



| <span data-ttu-id="1c93a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c93a-117">Requirement</span></span> | <span data-ttu-id="1c93a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1c93a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c93a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c93a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c93a-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c93a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1c93a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c93a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c93a-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c93a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c93a-123">Header</span><span class="sxs-lookup"><span data-stu-id="1c93a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c93a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c93a-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1c93a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1c93a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c93a-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c93a-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1c93a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1c93a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c93a-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c93a-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




