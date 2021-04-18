---
description: Öffnet ein Handle für ein Thread Objekt mit dem angegebenen Zugriff.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Ntopenthread-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372059"
---
# <a name="ntopenthread-function"></a><span data-ttu-id="1ae26-103">Ntopenthread-Funktion</span><span class="sxs-lookup"><span data-stu-id="1ae26-103">NtOpenThread function</span></span>

<span data-ttu-id="1ae26-104">\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1ae26-104">\[This function may be changed or removed from Windows without further notice.</span></span> <span data-ttu-id="1ae26-105">Verwenden Sie stattdessen die [**openthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) -Funktion.\]</span><span class="sxs-lookup"><span data-stu-id="1ae26-105">Use the [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function instead.\]</span></span>

<span data-ttu-id="1ae26-106">Öffnet ein Handle für ein Thread Objekt mit dem angegebenen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="1ae26-106">Opens a handle to a thread object with the access specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae26-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae26-107">Syntax</span></span>


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a><span data-ttu-id="1ae26-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ae26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae26-109">*Threadhandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1ae26-109">*ThreadHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae26-110">Ein Zeiger auf eine Variable, die das Thread Objekt Handle empfängt.</span><span class="sxs-lookup"><span data-stu-id="1ae26-110">A pointer to a variable that receives the thread object handle.</span></span>

</dd> <dt>

<span data-ttu-id="1ae26-111">*DesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae26-111">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae26-112">Ein [**Zugriffs \_ Masken**](../secauthz/access-mask-format.md) Datentyp, der die gewünschten Zugriffs Typen für das Thread Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1ae26-112">An [**ACCESS\_MASK**](../secauthz/access-mask-format.md) data type that provides the desired types of access for the thread object.</span></span>

</dd> <dt>

<span data-ttu-id="1ae26-113">*Objectattributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae26-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae26-114">Ein Zeiger auf eine [Objekt \_ Attribut](https://msdn.microsoft.com/library/aa491657.aspx) Struktur.</span><span class="sxs-lookup"><span data-stu-id="1ae26-114">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure.</span></span> <span data-ttu-id="1ae26-115">Der **objectName** -Member dieser Struktur muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1ae26-115">The **ObjectName** member of this structure must be NULL.</span></span>

<span data-ttu-id="1ae26-116">**Windows Server 2003 und Windows XP:** Der **objectName** -Member dieser Struktur kann auf einen Objektnamen zeigen.</span><span class="sxs-lookup"><span data-stu-id="1ae26-116">**Windows Server 2003 and Windows XP:** The **ObjectName** member of this structure can point to an object name.</span></span> <span data-ttu-id="1ae26-117">Wenn **objectName** nicht NULL ist, muss der *ClientID-* Parameter NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1ae26-117">If **ObjectName** is not NULL, the *ClientId* parameter must be NULL.</span></span>

</dd> <dt>

<span data-ttu-id="1ae26-118">*ClientID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae26-118">*ClientId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae26-119">Ein Zeiger auf eine **Client- \_ ID** -Struktur, die den Thread identifiziert, dessen Thread geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ae26-119">A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span>

<span data-ttu-id="1ae26-120">**Windows Server 2003 und Windows XP:** Ein Zeiger auf eine **Client- \_ ID** -Struktur, die den Thread identifiziert, dessen Thread geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ae26-120">**Windows Server 2003 and Windows XP:** A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span> <span data-ttu-id="1ae26-121">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1ae26-121">This parameter can be NULL.</span></span> <span data-ttu-id="1ae26-122">Wenn dieser Parameter nicht NULL ist, muss der **objectName** -Member der Struktur, auf die durch den *objectattributes* -Parameter verwiesen wird, NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1ae26-122">If this parameter is not NULL, the **ObjectName** member of the structure pointed to by the *ObjectAttributes* parameter must be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae26-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ae26-123">Return value</span></span>

<span data-ttu-id="1ae26-124">Gibt den **NTSTATUS** -oder-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="1ae26-124">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="1ae26-125">Die Formulare und die Bedeutung von **NTSTATUS** -Fehlercodes sind in der Header Datei "NTSTATUS. h" aufgeführt, die im WDK verfügbar ist, und werden in der WDK-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ae26-125">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae26-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ae26-126">Remarks</span></span>

<span data-ttu-id="1ae26-127">Dieser Funktion ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1ae26-127">This function has no associated header file.</span></span> <span data-ttu-id="1ae26-128">Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ae26-128">The associated import library, Ntdll.lib is available in the WDK.</span></span> <span data-ttu-id="1ae26-129">Sie können auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1ae26-129">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae26-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ae26-130">Requirements</span></span>



| <span data-ttu-id="1ae26-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ae26-131">Requirement</span></span> | <span data-ttu-id="1ae26-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1ae26-132">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae26-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1ae26-133">DLL</span></span><br/> | <dl> <span data-ttu-id="1ae26-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ae26-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
