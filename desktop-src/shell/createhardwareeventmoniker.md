---
description: Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt. Die automatische Wiedergabe verwendet diese Funktion, damit Anwendungen AutoPlay-Ereignisse verwenden können.
title: Funktion "kreatehardwareeventmoniker"
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
ms.openlocfilehash: 59100ab20cd997cc4ab35602698268ec6d76dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977336"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="bd075-104">Funktion "kreatehardwareeventmoniker"</span><span class="sxs-lookup"><span data-stu-id="bd075-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="bd075-105">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd075-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="bd075-106">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bd075-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bd075-107">Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd075-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="bd075-108">Die automatische Wiedergabe verwendet diese Funktion, damit Anwendungen AutoPlay-Ereignisse verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bd075-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd075-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd075-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="bd075-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd075-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd075-111">*CLSID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd075-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd075-112">Typ: **ref-sid**</span><span class="sxs-lookup"><span data-stu-id="bd075-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="bd075-113">Die ID der Klasse, an die der Moniker gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="bd075-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="bd075-114">*pszeventhandler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd075-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd075-115">Typ: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="bd075-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="bd075-116">Der Name des Ereignis Handlers.</span><span class="sxs-lookup"><span data-stu-id="bd075-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="bd075-117">*ppmoniker* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd075-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd075-118">Typ: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="bd075-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="bd075-119">Die Adresse einer Zeiger Variablen, die den [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Schnittstellen Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="bd075-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd075-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd075-120">Return value</span></span>

<span data-ttu-id="bd075-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bd075-121">Type: **HRESULT**</span></span>

<span data-ttu-id="bd075-122">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bd075-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd075-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd075-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd075-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd075-124">Remarks</span></span>

<span data-ttu-id="bd075-125">Verwenden Sie beim Registrieren ausgelaufeigener Anwendungen den Wert von " **kreatehardwareeventmoniker** ", damit diese Anwendungen auf AutoPlay-Ereignisse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="bd075-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="bd075-126">Zum Verwenden von AutoPlay-Ereignissen in laufenden Anwendungen müssen Sie zuerst eine neue Komponente erstellen, die die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="bd075-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="bd075-127">Initialisieren Sie diese Schnittstelle mit dem initcmdline-Wert aus dem Eintrag eines bestimmten **Handlers** unter dem Handler-Schlüssel, da AutoPlay nicht die [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="bd075-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="bd075-128">Sie sollten " **whatehardwareeventmoniker** " aufrufen, um einen Moniker zu erhalten, der die Komponente und ihren Ereignishandler darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd075-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="bd075-129">Verwenden Sie dann den im *ppmoniker* -Parameter zurückgegebenen Wert, um die Komponente in der laufenden Objekttabelle (rot) zu registrieren, wie im Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd075-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="bd075-130">Beachten Sie, dass " **kreatehardwareeventmoniker** " nicht in einer Header Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bd075-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="bd075-131">Um es in Ihrem Code zu verwenden, müssen Sie durch einen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)-Aufrufvorgang ein Handle für die Shsvcs.dll Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="bd075-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="bd075-132">Anschließend verwenden Sie dieses Handle in einem Aufruf von [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) , um eine Instanz der Funktion " **featehardwareeventmoniker** " zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd075-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="bd075-133">Für den Aufrufen von " [**iriunningobjec\:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) " müssen Sie die folgenden **AppID** -Informationen in die Registrierung eingeben.</span><span class="sxs-lookup"><span data-stu-id="bd075-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="bd075-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bd075-134">Requirements</span></span>



| <span data-ttu-id="bd075-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd075-135">Requirement</span></span> | <span data-ttu-id="bd075-136">Wert</span><span class="sxs-lookup"><span data-stu-id="bd075-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd075-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd075-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bd075-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd075-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bd075-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd075-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bd075-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd075-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd075-141">Header</span><span class="sxs-lookup"><span data-stu-id="bd075-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd075-142"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="bd075-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="bd075-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bd075-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd075-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd075-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 
