---
description: Die Clone- \_ Methode des-Objekts von "taubemlasterror" gibt ein neues-Objekt zurück, das ein Klon des aktuellen "taubemlasterror"-Objekts ist.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: SWbemLastError.Clone_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358583"
---
# <a name="swbemlasterrorclone_-method"></a><span data-ttu-id="86346-103">Methode ' Swap. Clone ' \_</span><span class="sxs-lookup"><span data-stu-id="86346-103">SWbemLastError.Clone\_ method</span></span>

<span data-ttu-id="86346-104">Die **Clone \_** -Methode des-Objekts von " [**taubemlasterror**](swbemlasterror.md) " gibt ein neues-Objekt zurück, das ein Klon des aktuellen " **taubemlasterror** "-Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="86346-104">The **Clone\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a new object that is a clone of the current **SWbemLastError** object.</span></span>

<span data-ttu-id="86346-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="86346-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86346-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="86346-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="86346-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="86346-107">Parameters</span></span>

<span data-ttu-id="86346-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="86346-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86346-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86346-109">Return value</span></span>

<span data-ttu-id="86346-110">Wenn die **Klon \_** Methode erfolgreich ist, gibt Sie ein neues-Objekt mit dem Wert " [**taubemlasterror**](swbemlasterror.md) " zurück.</span><span class="sxs-lookup"><span data-stu-id="86346-110">If the **Clone\_** method is successful, it returns a new [**SWbemLastError**](swbemlasterror.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86346-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="86346-111">Error codes</span></span>

<span data-ttu-id="86346-112">Nach dem Abschluss der **Klon \_** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="86346-112">Upon the completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="86346-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="86346-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="86346-114">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="86346-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="86346-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="86346-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="86346-116">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="86346-116">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="86346-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="86346-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="86346-118">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="86346-118">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86346-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86346-119">Remarks</span></span>

<span data-ttu-id="86346-120">Verwenden Sie **die \_ Clone** -Methode, um eine Klassendefinition oder-Instanz zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="86346-120">Use the **Clone\_** method to duplicate a class definition or instance.</span></span> <span data-ttu-id="86346-121">Diese Methode ist nützlich, wenn Sie die ursprüngliche Kopie des Objekts sichern müssen, während Sie eine neue Kopie ändern.</span><span class="sxs-lookup"><span data-stu-id="86346-121">This method is useful when you need to back up the original copy of the object while you modify a new copy.</span></span> <span data-ttu-id="86346-122">Verwenden Sie diese Methode auch, um viele neue Instanzen aus einer einzelnen Quell Instanz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="86346-122">Also, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="86346-123">Verwenden Sie z [**. b. "errbeapbject. \_ SpawnInstance**](swbemobject-spawninstance-.md) ", um eine einzelne Start Instanz zu erstellen, und verwenden Sie " **taubemlasterror. Clone \_** ", um 100 Kopien der Instanz schnell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="86346-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance and use **SWbemLastError.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="86346-124">Anschließend können Sie die Objekte ändern und jedem Objekt bestimmte Werte erteilen.</span><span class="sxs-lookup"><span data-stu-id="86346-124">Subsequently, you can modify the objects, giving specific values to each object.</span></span>

<span data-ttu-id="86346-125">Es ist nicht möglich, diese Methode zu verwenden, um eine Klassendefinition in eine-Instanz zu konvertieren oder um eine Instanz in eine Klassendefinition zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="86346-125">It is not possible to use this method to convert a class definition to an instance or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="86346-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86346-126">Requirements</span></span>



| <span data-ttu-id="86346-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86346-127">Requirement</span></span> | <span data-ttu-id="86346-128">Wert</span><span class="sxs-lookup"><span data-stu-id="86346-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86346-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86346-129">Minimum supported client</span></span><br/> | <span data-ttu-id="86346-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86346-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86346-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86346-131">Minimum supported server</span></span><br/> | <span data-ttu-id="86346-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86346-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86346-133">Header</span><span class="sxs-lookup"><span data-stu-id="86346-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="86346-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="86346-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86346-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="86346-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="86346-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86346-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86346-137">DLL</span><span class="sxs-lookup"><span data-stu-id="86346-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86346-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86346-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="86346-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="86346-139">CLSID</span></span><br/>                    | <span data-ttu-id="86346-140">CLSID- \_ Austausch Fehler</span><span class="sxs-lookup"><span data-stu-id="86346-140">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="86346-141">IID</span><span class="sxs-lookup"><span data-stu-id="86346-141">IID</span></span><br/>                      | <span data-ttu-id="86346-142">IID \_ iswbemlasterror</span><span class="sxs-lookup"><span data-stu-id="86346-142">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




