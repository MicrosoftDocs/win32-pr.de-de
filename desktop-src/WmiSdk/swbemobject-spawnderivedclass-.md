---
description: Verwenden Sie die spawnderivedclass- \_ Methode des errbemubject-Objekts, um ein abgeleitetes Klassenobjekt aus dem aktuellen-Objekt zu erstellen. Das-Objekt muss eine Klassendefinition sein, die zur übergeordneten Klasse des erzeugten Objekts wird.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: SWbemObject.SpawnDerivedClass_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215320"
---
# <a name="swbemobjectspawnderivedclass_-method"></a><span data-ttu-id="6229d-104">Errbemubject. spawnderivedclass- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="6229d-104">SWbemObject.SpawnDerivedClass\_ method</span></span>

<span data-ttu-id="6229d-105">Verwenden Sie die **spawnderivedclass \_** -Methode des [**errbemubject**](swbemobject.md) -Objekts, um ein abgeleitetes Klassenobjekt aus dem aktuellen-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6229d-105">Use the **SpawnDerivedClass\_** method of the [**SWbemObject**](swbemobject.md) object to create a derived class object from the current object.</span></span> <span data-ttu-id="6229d-106">Das-Objekt muss eine Klassendefinition sein, die zur übergeordneten Klasse des erzeugten Objekts wird.</span><span class="sxs-lookup"><span data-stu-id="6229d-106">The object must be a class definition that becomes the parent class of the spawned object.</span></span>

<span data-ttu-id="6229d-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6229d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6229d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6229d-108">Syntax</span></span>


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6229d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6229d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6229d-110">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="6229d-110">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6229d-111">Reserviert und muss 0 (null) sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="6229d-111">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6229d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6229d-112">Return value</span></span>

<span data-ttu-id="6229d-113">Wenn der-Befehl erfolgreich ausgeführt wurde, enthält das " [**errbemubject**](swbemobject.md) "-Objekt das neue Klassen Definitions Objekt.</span><span class="sxs-lookup"><span data-stu-id="6229d-113">If the call is successful, the [**SWbemObject**](swbemobject.md) object contains the new class definition object.</span></span> <span data-ttu-id="6229d-114">Wenn ein Fehler auftritt, wird kein Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6229d-114">No object returns when there is an error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6229d-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6229d-115">Error codes</span></span>

<span data-ttu-id="6229d-116">Nach dem Abschluss der **spawnderivedclass \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="6229d-116">After the completion of the **SpawnDerivedClass\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6229d-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6229d-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6229d-118">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6229d-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6229d-119">**wbemErrIllegalOperation** -2147749918 (0x8004101e)</span><span class="sxs-lookup"><span data-stu-id="6229d-119">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="6229d-120">Der Benutzer hat einen ungültigen Vorgang angefordert, z. b. das Abrufen einer Klasse aus einer Instanz.</span><span class="sxs-lookup"><span data-stu-id="6229d-120">User requested an illegal operation, such as spawning a class from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="6229d-121">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="6229d-121">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="6229d-122">Die Quell Klasse wurde nicht vollständig definiert oder bei WMI registriert, sodass eine neue abgeleitete Klasse nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6229d-122">Source class was not completely defined or registered with WMI, so a new derived class is not permitted.</span></span>

</dd> <dt>

<span data-ttu-id="6229d-123">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6229d-123">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6229d-124">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6229d-124">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6229d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6229d-125">Remarks</span></span>

<span data-ttu-id="6229d-126">Das zurückgegebene Objekt wird automatisch zu einer Unterklasse des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6229d-126">The object that is returned automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="6229d-127">Dieses Verhalten kann nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6229d-127">This behavior cannot be overridden.</span></span> <span data-ttu-id="6229d-128">Es gibt keine andere Methode, mit der abgeleitete Klassen erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="6229d-128">There is no other method by which you can create derived classes.</span></span>

<span data-ttu-id="6229d-129">Eine abgeleitete Klasse kann nicht von einer Klasse erstellt werden, die für Ihren eigenen Client Prozess lokal ist.</span><span class="sxs-lookup"><span data-stu-id="6229d-129">You cannot create a derived class from a class that is local to your own client process.</span></span> <span data-ttu-id="6229d-130">Bevor Sie diese Methode zum Erstellen einer abgeleiteten Klasse verwenden, müssen Sie die Basisklasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="6229d-130">Before use this method to create a derived class, you must create the base class.</span></span> <span data-ttu-id="6229d-131">Rufen Sie zum Erstellen der Basisklasse die Datei " [**errbemubject. Put \_**](swbemobject-put-.md)" auf, und rufen Sie die Basisklasse mithilfe von " [**Swap Services. Get**](swbemservices-get.md)" ab.</span><span class="sxs-lookup"><span data-stu-id="6229d-131">To create the base class, call [**SWbemObject.Put\_**](swbemobject-put-.md), and retrieve the base class using [**SWbemServices.Get**](swbemservices-get.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6229d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6229d-132">Requirements</span></span>



| <span data-ttu-id="6229d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6229d-133">Requirement</span></span> | <span data-ttu-id="6229d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6229d-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6229d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6229d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6229d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6229d-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6229d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6229d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6229d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6229d-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6229d-139">Header</span><span class="sxs-lookup"><span data-stu-id="6229d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6229d-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6229d-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6229d-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6229d-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="6229d-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6229d-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6229d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6229d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6229d-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6229d-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6229d-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="6229d-145">CLSID</span></span><br/>                    | <span data-ttu-id="6229d-146">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="6229d-146">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="6229d-147">IID</span><span class="sxs-lookup"><span data-stu-id="6229d-147">IID</span></span><br/>                      | <span data-ttu-id="6229d-148">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="6229d-148">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




