---
description: Registriert die shelldienste (shelldynamischer Datenaustausch) im aktuellen Prozess und benachrichtigt das System, dass der aktuelle Prozess DDE-Objekte hosten möchte.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: Shellddeingeit-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980441"
---
# <a name="shellddeinit-function"></a><span data-ttu-id="54232-103">Shellddeingeit-Funktion</span><span class="sxs-lookup"><span data-stu-id="54232-103">ShellDDEInit function</span></span>

<span data-ttu-id="54232-104">Registriert die shelldienste (shelldynamischer Datenaustausch) im aktuellen Prozess und benachrichtigt das System, dass der aktuelle Prozess DDE-Objekte hosten möchte.</span><span class="sxs-lookup"><span data-stu-id="54232-104">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="54232-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54232-105">Syntax</span></span>


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a><span data-ttu-id="54232-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54232-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54232-107">*Init* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54232-107">*init* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54232-108">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="54232-108">Type: **BOOL**</span></span>

<span data-ttu-id="54232-109">**True** , wenn der aktuelle Prozess als DDE-Host registriert werden soll. " **False** ", um die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="54232-109">**TRUE** to register the current process as DDE host; **FALSE** to unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54232-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54232-110">Return value</span></span>

<span data-ttu-id="54232-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54232-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54232-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54232-112">Remarks</span></span>

<span data-ttu-id="54232-113">Der Prozess, der diese Funktion aufruft, fungiert als Shell und wird verwendet, um den Inhalt der Ordner anzuzeigen, die mit dem [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) -Verb geöffnet wurden.</span><span class="sxs-lookup"><span data-stu-id="54232-113">The process that calls this function acts as the Shell and is used to view the content of folders opened with the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open' verb.</span></span>

<span data-ttu-id="54232-114">Diese Funktion verfügt über keine zugeordnete Header-oder Bibliotheksdatei, sodass Sie von Ordinalwerten aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="54232-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="54232-115">Rufen Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem DLL-Namen (Shdocvw.dll) auf, um ein Modul Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="54232-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Shdocvw.dll) to obtain a module handle.</span></span> <span data-ttu-id="54232-116">Anschließend können Sie [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mit diesem Modul Handle und der Ordnungszahl 118 der Funktion aufrufen, um die Adresse der Funktion abzurufen.</span><span class="sxs-lookup"><span data-stu-id="54232-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the function ordinal number 118 to get the address of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="54232-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="54232-117">Requirements</span></span>



| <span data-ttu-id="54232-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54232-118">Requirement</span></span> | <span data-ttu-id="54232-119">Wert</span><span class="sxs-lookup"><span data-stu-id="54232-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54232-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54232-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54232-121">Nur Windows XP, Windows 2000 Professional \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54232-121">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54232-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54232-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54232-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54232-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="54232-124">DLL</span><span class="sxs-lookup"><span data-stu-id="54232-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54232-125"><dt>Shdocvw.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="54232-125"><dt>Shdocvw.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
