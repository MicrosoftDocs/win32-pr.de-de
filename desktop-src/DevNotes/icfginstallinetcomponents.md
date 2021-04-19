---
description: Installiert die angegebenen Systemkomponenten.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Icsginstallinetcomponents-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352968"
---
# <a name="icfginstallinetcomponents-function"></a><span data-ttu-id="264a5-103">Icsginstallinetcomponents-Funktion</span><span class="sxs-lookup"><span data-stu-id="264a5-103">IcfgInstallInetComponents function</span></span>

<span data-ttu-id="264a5-104">Installiert die angegebenen Systemkomponenten.</span><span class="sxs-lookup"><span data-stu-id="264a5-104">Installs the system components specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="264a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="264a5-105">Syntax</span></span>


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a><span data-ttu-id="264a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="264a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="264a5-107">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="264a5-107">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="264a5-108">Ein Handle für das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="264a5-108">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="264a5-109">*DWF Options*</span><span class="sxs-lookup"><span data-stu-id="264a5-109">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="264a5-110">Eine Kombination der folgenden Flags, die die Installation und Konfiguration steuern.</span><span class="sxs-lookup"><span data-stu-id="264a5-110">A combination of the following flags that control the installation and configuration.</span></span>



| <span data-ttu-id="264a5-111">Wert</span><span class="sxs-lookup"><span data-stu-id="264a5-111">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="264a5-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="264a5-112">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="264a5-113"><dt>**ICFG \_ Installmail**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="264a5-113"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="264a5-114">Installieren Sie Exchange und Internet-e-Mail.</span><span class="sxs-lookup"><span data-stu-id="264a5-114">Install Exchange and Internet mail.</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="264a5-115"><dt>**ICFG \_ Installras**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="264a5-115"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="264a5-116">Installieren Sie RAS (falls erforderlich).</span><span class="sxs-lookup"><span data-stu-id="264a5-116">Install RAS (if needed).</span></span><br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="264a5-117"><dt>**ICFG \_ Installtcp**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="264a5-117"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="264a5-118">Installieren Sie TCP/IP (falls erforderlich).</span><span class="sxs-lookup"><span data-stu-id="264a5-118">Install TCP/IP (if needed).</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="264a5-119">*lpfneedsrestart*</span><span class="sxs-lookup"><span data-stu-id="264a5-119">*lpfNeedsRestart*</span></span> 
</dt> <dd>

<span data-ttu-id="264a5-120">Wenn dieser Wert ungleich **null** ist, wird bei der Rückgabe nur dann **true** angezeigt, wenn Windows neu gestartet werden muss, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="264a5-120">If this value is non-**NULL**, on return it will be **TRUE** only if Windows must be restarted to complete the installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="264a5-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="264a5-121">Return value</span></span>

<span data-ttu-id="264a5-122">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="264a5-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="264a5-123">Wenn keine Fehler auftreten, wird der **Fehler \_ Erfolgs** Code zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="264a5-123">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="264a5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="264a5-124">Remarks</span></span>

<span data-ttu-id="264a5-125">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="264a5-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="264a5-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="264a5-126">Requirements</span></span>



| <span data-ttu-id="264a5-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="264a5-127">Requirement</span></span> | <span data-ttu-id="264a5-128">Wert</span><span class="sxs-lookup"><span data-stu-id="264a5-128">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="264a5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="264a5-129">DLL</span></span><br/> | <dl> <span data-ttu-id="264a5-130"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="264a5-130"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
