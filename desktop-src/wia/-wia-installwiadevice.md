---
description: Die installwiadevice-Funktion installiert ein Windows-Abbild Erfassungsgerät (WIA) als von der Stamm-Enumeration erfasste Geräte. Möglicherweise wird eine Sicherheitswarnung angezeigt, wenn eine Installationsdatei oder ein installiertes Coinstaller nicht digital signiert und vertrauenswürdig ist.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Installwiadevice-Funktion (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752864"
---
# <a name="installwiadevice-function"></a><span data-ttu-id="c1606-104">Installwiadevice-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1606-104">InstallWiaDevice function</span></span>

<span data-ttu-id="c1606-105">Die **installwiadevice** -Funktion installiert ein Windows-Abbild Erfassungsgerät (WIA) als von der Stamm-Enumeration erfasste Geräte.</span><span class="sxs-lookup"><span data-stu-id="c1606-105">The **InstallWiaDevice** function installs a Windows Image Acquisition (WIA) device as root-enumerated device.</span></span> <span data-ttu-id="c1606-106">Möglicherweise wird eine Sicherheitswarnung angezeigt, wenn eine Installationsdatei oder ein installiertes Coinstaller nicht digital signiert und vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="c1606-106">It may popup a security warning if any installing file or coinstaller is not digitally signed and trusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1606-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1606-107">Syntax</span></span>


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a><span data-ttu-id="c1606-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1606-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1606-109">*pwiadeviceingestall* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1606-109">*pWiaDeviceInstall* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1606-110">Geben Sie Folgendes ein: \**pwiadeviceinstall \** _</span><span class="sxs-lookup"><span data-stu-id="c1606-110">Type: \**PWIADEVICEINSTALL\** _</span></span>

<span data-ttu-id="c1606-111">Zeiger auf eine wiadeviceingestall-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c1606-111">Pointer to a WIADEVICEINSTALL structure.</span></span> <span data-ttu-id="c1606-112">Der _szFriendlyName \*-Member der-Struktur muss auf den tatsächlichen Geräte FriendlyName festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c1606-112">The _szFriendlyName\* member of the structure must be set to the actual device FriendlyName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1606-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1606-113">Return value</span></span>

<span data-ttu-id="c1606-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c1606-114">Type: **DWORD**</span></span>

<span data-ttu-id="c1606-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c1606-115">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c1606-116">Wenn die Funktion fehlschlägt, wird ein Win32-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1606-116">If the function fails, it returns a Win32 error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1606-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1606-117">Requirements</span></span>



| <span data-ttu-id="c1606-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1606-118">Requirement</span></span> | <span data-ttu-id="c1606-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c1606-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1606-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1606-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1606-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1606-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c1606-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1606-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1606-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1606-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1606-124">Header</span><span class="sxs-lookup"><span data-stu-id="c1606-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1606-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1606-125"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="c1606-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1606-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1606-127"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1606-127"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




