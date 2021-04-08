---
description: Die Funktion "-Funktion" verwendet das BLOB, das vom Finder zurückgegeben wurde, um eine NPP zu erstellen, die von der Anwendung verwendet werden kann.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Kreatenppinterface-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960027"
---
# <a name="createnppinterface-function"></a><span data-ttu-id="c0f43-103">Kreatenppinterface-Funktion</span><span class="sxs-lookup"><span data-stu-id="c0f43-103">CreateNPPInterface function</span></span>

<span data-ttu-id="c0f43-104">Die **Funktion "** -Funktion" verwendet das BLOB, das vom Finder zurückgegeben wurde, um eine NPP zu erstellen, die von der Anwendung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0f43-104">The **CreateNPPInterface** function uses the BLOB returned from the finder to create an NPP that the application can use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0f43-105">Syntax</span></span>


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="c0f43-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0f43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f43-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0f43-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f43-108">Handle für das BLOB, das vom Finder zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c0f43-108">Handle to the BLOB returned from the finder.</span></span>

</dd> <dt>

<span data-ttu-id="c0f43-109">*IID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0f43-109">*iid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f43-110">Der Bezeichner der Schnittstelle, die Sie von der NPP (z. b. "**iritc** " oder " **idelta aydc**") abrufen.</span><span class="sxs-lookup"><span data-stu-id="c0f43-110">Identifier of the interface that you call from the NPP (**IRTC** or **IDelaydC**, for example).</span></span>

</dd> <dt>

<span data-ttu-id="c0f43-111">*ppvobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c0f43-111">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f43-112">Zeiger auf den zurückgegebenen Zeiger auf die angeforderte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c0f43-112">Pointer to the returned pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f43-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0f43-113">Return value</span></span>

<span data-ttu-id="c0f43-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c0f43-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c0f43-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c0f43-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f43-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0f43-116">Requirements</span></span>



| <span data-ttu-id="c0f43-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0f43-117">Requirement</span></span> | <span data-ttu-id="c0f43-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c0f43-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f43-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0f43-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f43-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0f43-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0f43-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0f43-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f43-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0f43-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0f43-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0f43-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f43-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f43-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c0f43-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0f43-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0f43-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0f43-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0f43-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c0f43-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f43-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f43-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




