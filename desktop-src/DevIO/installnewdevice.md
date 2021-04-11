---
description: Installiert ein neues Gerät. Der Benutzer wird aufgefordert, das Gerät auszuwählen.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Installnewdevice-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127289"
---
# <a name="installnewdevice-function"></a><span data-ttu-id="a8845-104">Installnewdevice-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8845-104">InstallNewDevice function</span></span>

<span data-ttu-id="a8845-105">Installiert ein neues Gerät.</span><span class="sxs-lookup"><span data-stu-id="a8845-105">Installs a new device.</span></span> <span data-ttu-id="a8845-106">Der Benutzer wird aufgefordert, das Gerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a8845-106">The user is prompted to select the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8845-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8845-107">Syntax</span></span>


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a><span data-ttu-id="a8845-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8845-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8845-109">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8845-109">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8845-110">Ein Handle für das Fenster auf oberster Ebene, das für jede erforderliche Benutzeroberfläche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8845-110">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="a8845-111">*Klassen-GUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8845-111">*ClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8845-112">Ein Zeiger auf eine Klassen- **GUID**.</span><span class="sxs-lookup"><span data-stu-id="a8845-112">A pointer to a class **GUID**.</span></span> <span data-ttu-id="a8845-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8845-113">This parameter is optional.</span></span> <span data-ttu-id="a8845-114">Wenn dieser Parameter **null** ist, wird der Benutzer auf der Seite zur Auswahl der Erkennung gestartet.</span><span class="sxs-lookup"><span data-stu-id="a8845-114">If this parameter is **NULL**, the user starts at the detection choice page.</span></span> <span data-ttu-id="a8845-115">Wenn es sich bei diesem Parameter um **GUID \_ null** oder **GUID \_ DEVCLASS \_ Unknown** handelt, wird der Benutzer auf der Seite Klassenauswahl gestartet.</span><span class="sxs-lookup"><span data-stu-id="a8845-115">If this parameter is **GUID\_NULL** or **GUID\_DEVCLASS\_UNKNOWN**, the user starts at the class selection page.</span></span>

</dd> <dt>

<span data-ttu-id="a8845-116">*vorab Start* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a8845-116">*pReboot* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8845-117">Ein Zeiger auf eine Variable, die den Neustart Status empfängt.</span><span class="sxs-lookup"><span data-stu-id="a8845-117">A pointer to a variable that receives the reboot status.</span></span> <span data-ttu-id="a8845-118">Dieser Parameter kann " **di \_ needrestart** " oder " **di \_ NEEDREBOOT**" lauten.</span><span class="sxs-lookup"><span data-stu-id="a8845-118">This parameter can be **DI\_NEEDRESTART** or **DI\_NEEDREBOOT**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8845-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8845-119">Return value</span></span>

<span data-ttu-id="a8845-120">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="a8845-120">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="a8845-121">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="a8845-121">If the function fails, the return value is zero.</span></span> <span data-ttu-id="a8845-122">Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.</span><span class="sxs-lookup"><span data-stu-id="a8845-122">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8845-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8845-123">Remarks</span></span>

<span data-ttu-id="a8845-124">Diese Funktion verfügt über keine zugeordnete Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="a8845-124">This function has no associated import library.</span></span> <span data-ttu-id="a8845-125">Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit NewDev.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a8845-125">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to NewDev.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8845-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8845-126">Requirements</span></span>



| <span data-ttu-id="a8845-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8845-127">Requirement</span></span> | <span data-ttu-id="a8845-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a8845-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8845-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8845-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8845-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8845-130">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="a8845-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8845-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8845-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8845-132">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="a8845-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a8845-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8845-134"><dt>NewDev.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8845-134"><dt>NewDev.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8845-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8845-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8845-136">Geräte Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="a8845-136">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

