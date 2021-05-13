---
description: Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt. AutoPlay verwendet diese Funktion, um Anwendungen die Verwendung von AutoPlay-Ereignissen zu ermöglichen.
title: CreateHardwareEventMoniker-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: c22f01835f9c526e95a4330e6ad35d370421e604
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841241"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="0fd52-104">CreateHardwareEventMoniker-Funktion</span><span class="sxs-lookup"><span data-stu-id="0fd52-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="0fd52-105">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0fd52-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="0fd52-106">Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="0fd52-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0fd52-107">Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fd52-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="0fd52-108">AutoPlay verwendet diese Funktion, um Anwendungen die Verwendung von AutoPlay-Ereignissen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0fd52-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd52-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd52-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="0fd52-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fd52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd52-111">*clsid* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0fd52-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd52-112">Typ: **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="0fd52-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="0fd52-113">Die ID der Klasse, an die der Moniker gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="0fd52-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="0fd52-114">*pszEventHandler* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0fd52-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd52-115">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="0fd52-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="0fd52-116">Der Name des Ereignishandlers.</span><span class="sxs-lookup"><span data-stu-id="0fd52-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="0fd52-117">*ppmoniker* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0fd52-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd52-118">Typ: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="0fd52-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="0fd52-119">Die Adresse einer Zeigervariablen, die den [**IMoniker-Schnittstellenzeiger**](/windows/win32/api/objidl/nn-objidl-imoniker) empfängt.</span><span class="sxs-lookup"><span data-stu-id="0fd52-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd52-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fd52-120">Return value</span></span>

<span data-ttu-id="0fd52-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0fd52-121">Type: **HRESULT**</span></span>

<span data-ttu-id="0fd52-122">Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="0fd52-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0fd52-123">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0fd52-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd52-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0fd52-124">Remarks</span></span>

<span data-ttu-id="0fd52-125">Verwenden Sie **CreateHardwareEventMoniker,** wenn Sie ausgeführte Anwendungen registrieren, damit diese Anwendungen Zugriff auf AutoPlay-Ereignisse haben.</span><span class="sxs-lookup"><span data-stu-id="0fd52-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="0fd52-126">Um AutoPlay-Ereignisse in ausgeführten Anwendungen zu verwenden, müssen Sie zunächst eine neue Komponente erstellen, die die [**IHWEventHandler-Schnittstelle**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) implementiert.</span><span class="sxs-lookup"><span data-stu-id="0fd52-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="0fd52-127">Initialisieren Sie diese Schnittstelle mit dem InitCmdLine-Wert aus dem Eintrag des **jeweiligen** Handlers unter dem Handlerschlüssel, da autoPlay die [**Initialize-Methode**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) nicht aufruft.</span><span class="sxs-lookup"><span data-stu-id="0fd52-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="0fd52-128">Sie sollten **CreateHardwareEventMoniker** aufrufen, um einen Moniker abzurufen, der Ihre Komponente und ihren Ereignishandler darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fd52-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="0fd52-129">Verwenden Sie dann den wert, der im *ppmoniker-Parameter* zurückgegeben wird, um Ihre Komponente in der laufenden Objekttabelle (ROT) zu registrieren, wie im Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0fd52-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="0fd52-130">Beachten Sie, dass **CreateHardwareEventMoniker** nicht in einer Headerdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0fd52-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="0fd52-131">Um sie in Ihrem Code zu verwenden, müssen Sie ein Handle für die Shsvcs.dll-Datei über einen Aufruf von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)abrufen.</span><span class="sxs-lookup"><span data-stu-id="0fd52-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="0fd52-132">Anschließend verwenden Sie dieses Handle in einem Aufruf von [**GetProcAddress,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) um eine Instanz der **CreateHardwareEventMoniker-Funktion** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0fd52-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="0fd52-133">Für den Aufruf von [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) müssen Sie die folgenden **AppID-Informationen** in die Registrierung eingeben.</span><span class="sxs-lookup"><span data-stu-id="0fd52-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a><span data-ttu-id="0fd52-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fd52-134">Requirements</span></span>



| <span data-ttu-id="0fd52-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fd52-135">Requirement</span></span> | <span data-ttu-id="0fd52-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0fd52-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd52-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fd52-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd52-138">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fd52-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0fd52-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fd52-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd52-140">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fd52-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fd52-141">Header</span><span class="sxs-lookup"><span data-stu-id="0fd52-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd52-142"><dt>Keine</dt></span><span class="sxs-lookup"><span data-stu-id="0fd52-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="0fd52-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd52-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd52-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd52-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 
