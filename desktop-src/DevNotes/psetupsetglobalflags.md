---
description: Deaktiviert Funktionen.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: psetupsetglobalflags-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370799"
---
# <a name="psetupsetglobalflags-function"></a><span data-ttu-id="8b795-103">psetupsetglobalflags-Funktion</span><span class="sxs-lookup"><span data-stu-id="8b795-103">pSetupSetGlobalFlags function</span></span>

<span data-ttu-id="8b795-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="8b795-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="8b795-105">Deaktiviert Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8b795-105">Disables features.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b795-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b795-106">Syntax</span></span>


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="8b795-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b795-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b795-108">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b795-108">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b795-109">Die Flags, mit denen die Benutzeroberfläche oder die automatische Sicherung deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="8b795-109">The flags used to disable user interface or automatic backup.</span></span>



| <span data-ttu-id="8b795-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8b795-110">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="8b795-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8b795-111">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <span data-ttu-id="8b795-112"><dt>**Pspgf \_ Nicht interaktives**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="8b795-112"><dt>**PSPGF\_NONINTERACTIVE**</dt> <dt>0x004</dt></span></span> </dl> | <span data-ttu-id="8b795-113">Legen Sie zum Deaktivieren der Benutzeroberfläche fest.</span><span class="sxs-lookup"><span data-stu-id="8b795-113">Set to disable user interface.</span></span><br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <span data-ttu-id="8b795-114"><dt>**Pspgf \_ Keine \_ Sicherung**</dt> <dt>0x002</dt></span><span class="sxs-lookup"><span data-stu-id="8b795-114"><dt>**PSPGF\_NO\_BACKUP**</dt> <dt>0x002</dt></span></span> </dl>               | <span data-ttu-id="8b795-115">Legen Sie zum Deaktivieren der automatischen Sicherung fest.</span><span class="sxs-lookup"><span data-stu-id="8b795-115">Set to disable automatic backup.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b795-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b795-116">Return value</span></span>

<span data-ttu-id="8b795-117">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8b795-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b795-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b795-118">Remarks</span></span>

<span data-ttu-id="8b795-119">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b795-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b795-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b795-120">Requirements</span></span>



| <span data-ttu-id="8b795-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b795-121">Requirement</span></span> | <span data-ttu-id="8b795-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8b795-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b795-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8b795-123">DLL</span></span><br/> | <dl> <span data-ttu-id="8b795-124"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b795-124"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
