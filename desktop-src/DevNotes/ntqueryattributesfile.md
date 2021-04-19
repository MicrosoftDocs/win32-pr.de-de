---
description: Ruft grundlegende Attribute für das angegebene Datei Objekt ab.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Ntqueryattributesfile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351240"
---
# <a name="ntqueryattributesfile-function"></a><span data-ttu-id="76541-103">Ntqueryattributesfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="76541-103">NtQueryAttributesFile function</span></span>

<span data-ttu-id="76541-104">\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="76541-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="76541-105">Ruft grundlegende Attribute für das angegebene Datei Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="76541-105">Retrieves basic attributes for the specified file object.</span></span>

## <a name="syntax"></a><span data-ttu-id="76541-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="76541-106">Syntax</span></span>


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a><span data-ttu-id="76541-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="76541-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76541-108">*Objectattributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76541-108">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76541-109">Ein Zeiger auf eine [Objekt \_ Attribut](https://msdn.microsoft.com/library/aa491657.aspx) Struktur, die die Attribute bereitstellt, die für das Datei Objekt verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76541-109">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure that supplies the attributes to be used for the file object.</span></span>

</dd> <dt>

<span data-ttu-id="76541-110">*Fileinformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76541-110">*FileInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76541-111">Ein Zeiger auf eine [Datei \_ grundlegende \_ Informations](https://msdn.microsoft.com/library/aa491634.aspx) Struktur, um die zurückgegebenen Datei Attributinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="76541-111">A pointer to a [FILE\_BASIC\_INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) structure to receive the returned file attribute information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76541-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76541-112">Return value</span></span>

<span data-ttu-id="76541-113">Gibt den NTSTATUS-oder-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="76541-113">Returns an NTSTATUS or error code.</span></span>

<span data-ttu-id="76541-114">Die Formulare und die Bedeutung von NTSTATUS-Fehlercodes sind in der Header Datei "NTSTATUS. h" aufgeführt, die im WDK verfügbar ist, und werden in der WDK-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76541-114">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="76541-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76541-115">Remarks</span></span>

<span data-ttu-id="76541-116">Dieser Funktion ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="76541-116">This function has no associated header file.</span></span> <span data-ttu-id="76541-117">Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76541-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="76541-118">Sie können auch die [**LoadLibrary**](-loadlibrary.md) -Funktion und die [**GetProcAddress**](-getprocaddress-.md) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="76541-118">You can also use the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="76541-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76541-119">Requirements</span></span>



| <span data-ttu-id="76541-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76541-120">Requirement</span></span> | <span data-ttu-id="76541-121">Wert</span><span class="sxs-lookup"><span data-stu-id="76541-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76541-122">DLL</span><span class="sxs-lookup"><span data-stu-id="76541-122">DLL</span></span><br/> | <dl> <span data-ttu-id="76541-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76541-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




