---
description: Die Clone- \_ Methode des "errbemubject"-Objekts gibt ein neues-Objekt zurück, das ein Klon des aktuellen-Objekts ist.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: SWbemObject.Clone_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050344"
---
# <a name="swbemobjectclone_-method"></a><span data-ttu-id="98ea4-103">Errbemubject. Clone- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="98ea4-103">SWbemObject.Clone\_ method</span></span>

<span data-ttu-id="98ea4-104">Die **Clone \_** -Methode des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein neues-Objekt zurück, das ein Klon des aktuellen-Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="98ea4-104">The **Clone\_** method of the [**SWbemObject**](swbemobject.md) object returns a new object that is a clone of the current object.</span></span>

<span data-ttu-id="98ea4-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="98ea4-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="98ea4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="98ea4-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="98ea4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="98ea4-107">Parameters</span></span>

<span data-ttu-id="98ea4-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="98ea4-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98ea4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98ea4-109">Return value</span></span>

<span data-ttu-id="98ea4-110">Wenn der [**Vorgang**](swbemobject.md) erfolgreich ist, gibt diese Methode ein neues-Objekt vom Metadatenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="98ea4-110">If successful, this method returns a new [**SWbemObject**](swbemobject.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="98ea4-111">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="98ea4-111">Error codes</span></span>

<span data-ttu-id="98ea4-112">Nach Abschluss der **Klon \_** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.</span><span class="sxs-lookup"><span data-stu-id="98ea4-112">After completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="98ea4-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="98ea4-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="98ea4-114">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="98ea4-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="98ea4-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="98ea4-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="98ea4-116">Es wurde **nichts** als Parameter angegeben, und es ist in dieser Verwendung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="98ea4-116">**Nothing** was specified as a parameter, and it is not acceptable in this usage.</span></span>

</dd> <dt>

<span data-ttu-id="98ea4-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="98ea4-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="98ea4-118">Nicht genügend Arbeitsspeicher zum Klonen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="98ea4-118">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98ea4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98ea4-119">Remarks</span></span>

<span data-ttu-id="98ea4-120">Verwenden Sie **die \_ Clone** -Methode, um eine Klassendefinition oder eine-Instanz zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="98ea4-120">Use the **Clone\_** method to duplicate a class definition or an instance.</span></span> <span data-ttu-id="98ea4-121">Dies ist hilfreich, wenn Sie die ursprüngliche Kopie des Objekts zu Sicherungszwecken benötigen, während Sie eine neue Kopie ändern.</span><span class="sxs-lookup"><span data-stu-id="98ea4-121">This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy.</span></span> <span data-ttu-id="98ea4-122">Verwenden Sie diese Methode ebenso, um viele neue Instanzen aus einer einzelnen Quell Instanz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="98ea4-122">Likewise, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="98ea4-123">Verwenden Sie z [**. b. "errbemubject. \_ SpawnInstance**](swbemobject-spawninstance-.md) ", um eine einzelne Start Instanz zu erstellen, und verwenden Sie " **errbemubject. Clone \_** ", um 100 Kopien der Instanz schnell zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="98ea4-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance, and use **SWbemObject.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="98ea4-124">Anschließend können Sie die Objekte ändern und jedem einzelnen bestimmte Werte geben.</span><span class="sxs-lookup"><span data-stu-id="98ea4-124">Subsequently, you can modify the objects, giving each one specific values.</span></span>

<span data-ttu-id="98ea4-125">Es ist nicht möglich, diese Methode zu verwenden, um eine Klassendefinition in eine-Instanz zu konvertieren oder um eine Instanz in eine Klassendefinition zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="98ea4-125">It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ea4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98ea4-126">Requirements</span></span>



| <span data-ttu-id="98ea4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98ea4-127">Requirement</span></span> | <span data-ttu-id="98ea4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="98ea4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98ea4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98ea4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="98ea4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98ea4-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98ea4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98ea4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="98ea4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98ea4-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98ea4-133">Header</span><span class="sxs-lookup"><span data-stu-id="98ea4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ea4-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="98ea4-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="98ea4-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="98ea4-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="98ea4-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98ea4-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98ea4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="98ea4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98ea4-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98ea4-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="98ea4-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="98ea4-139">CLSID</span></span><br/>                    | <span data-ttu-id="98ea4-140">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="98ea4-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="98ea4-141">IID</span><span class="sxs-lookup"><span data-stu-id="98ea4-141">IID</span></span><br/>                      | <span data-ttu-id="98ea4-142">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="98ea4-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




