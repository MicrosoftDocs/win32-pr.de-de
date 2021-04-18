---
description: Lädt die Monitor-DLL.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Onloadingdll-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357394"
---
# <a name="onloadingdll-function"></a><span data-ttu-id="54805-103">Onloadingdll-Funktion</span><span class="sxs-lookup"><span data-stu-id="54805-103">OnLoadingDLL function</span></span>

<span data-ttu-id="54805-104">Die **onloadingdll** -Funktion lädt die Monitor-DLL.</span><span class="sxs-lookup"><span data-stu-id="54805-104">The **OnLoadingDLL** function loads the monitor DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="54805-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54805-105">Syntax</span></span>


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a><span data-ttu-id="54805-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54805-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54805-107">*hfilterblob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54805-107">*hFilterBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54805-108">Ein BLOB, das von mcsvc verwendet wird, um einen Monitor mit verfügbaren NICs abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="54805-108">A BLOB that the MCSVC uses to match a monitor with available NICs.</span></span> <span data-ttu-id="54805-109">Dieser Parameter enthält immer eine Anforderung für eine [untc](irtc.md) -Schnittstelle, sodass die meisten Monitore dem BLOB keine Einträge hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="54805-109">This parameter always contains a request for an [IRTC](irtc.md) interface, so most monitors do not need to add any entries to the BLOB.</span></span> <span data-ttu-id="54805-110">Ein benutzerdefinierter Monitor kann jedoch zusätzliche Filterkriterien hinzufügen (z. b., dass der Mac-Typ Ethernet lauten muss).</span><span class="sxs-lookup"><span data-stu-id="54805-110">However, a custom monitor can add additional filter criteria (for example, that the MAC type must be Ethernet).</span></span>

</dd> <dt>

<span data-ttu-id="54805-111">*pkreateflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54805-111">*pCreateFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54805-112">Die Flags, die angeben, wie mcsvc die Erstellung eines Monitors steuert.</span><span class="sxs-lookup"><span data-stu-id="54805-112">The flags that indicate how the MCSVC controls the creation of a monitor.</span></span> <span data-ttu-id="54805-113">Dieser Parameter muss einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="54805-113">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="54805-114">Wert</span><span class="sxs-lookup"><span data-stu-id="54805-114">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="54805-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="54805-115">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <span data-ttu-id="54805-116"><dt>**MCS \_ Create \_ One \_ per \_ Netcard**</dt></span><span class="sxs-lookup"><span data-stu-id="54805-116"><dt>**MCS\_CREATE\_ONE\_PER\_NETCARD**</dt></span></span> </dl>          | <span data-ttu-id="54805-117">Mcsvc stellt sicher, dass nur eine Instanz dieses Monitors für jede NIC vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="54805-117">The MCSVC ensures that only one instance of this monitor exists for each NIC.</span></span> <span data-ttu-id="54805-118">Eine zweite Instanz kann nur erstellt werden, wenn die erste Instanz zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="54805-118">A second instance can be created only if the first one is destroyed.</span></span><br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <span data-ttu-id="54805-119"><dt>**MCS \_ Erstellen \_ von Konfigurationen \_ \_ standardmäßig**</dt></span><span class="sxs-lookup"><span data-stu-id="54805-119"><dt>**MCS\_CREATE\_CONFIGS\_BY\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="54805-120">Wenn der Monitor über eine interne Standardkonfiguration verfügt, muss der Benutzer von mcsvc nicht konfiguriert werden, bevor die Instanz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="54805-120">If the monitor has a default internal configuration, the MCSVC does not require the user to configure the monitor before the instance is created.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="54805-121">*ppdefaultname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54805-121">*ppDefaultName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54805-122">Ein Zeiger auf einen Zeiger auf die Adresse des Standard namens des Monitors.</span><span class="sxs-lookup"><span data-stu-id="54805-122">A pointer to a pointer to the address of the default name of the monitor.</span></span> <span data-ttu-id="54805-123">Der mcsvc verwendet beim Erstellen von Instanzen des Monitors den Standardnamen.</span><span class="sxs-lookup"><span data-stu-id="54805-123">The MCSVC uses the default name when creating instances of the monitor.</span></span>

<span data-ttu-id="54805-124">Wenn der zurückgegebene Standardname beispielsweise "Router Monitor" lautet, ist die erste Monitor Instanz "Router Monitor 1", die zweite "RouterMonitor2" usw.</span><span class="sxs-lookup"><span data-stu-id="54805-124">For example, if the returned default name is "Router Monitor", the first monitor instance would be "Router Monitor 1", the second would be "RouterMonitor2, and so on.</span></span> <span data-ttu-id="54805-125">Wenn **null** zurückgegeben wird, verwendet mcsvc den Namen der dll.</span><span class="sxs-lookup"><span data-stu-id="54805-125">If **NULL** is returned, the MCSVC uses the name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="54805-126">*ppdescription* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54805-126">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54805-127">Ein Zeiger auf einen Zeiger auf die Adresse der Beschreibung des Monitors.</span><span class="sxs-lookup"><span data-stu-id="54805-127">A pointer to a pointer to the address of the description of the monitor.</span></span> <span data-ttu-id="54805-128">Die Beschreibung wird an das Monitor-Steuerungs Tool übermittelt, das die Beschreibung verwendet, um dem Benutzer mitzuteilen, dass der Monitor vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="54805-128">The description is passed to the Monitor Control Tool, which uses the description to indicate to the user that the monitor exists.</span></span> <span data-ttu-id="54805-129">Dieser Parameter kann **null** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="54805-129">This parameter can return **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54805-130">*ppdefaultscript* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54805-130">*ppDefaultScript* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54805-131">Ein Zeiger auf einen Zeiger auf die Adresse des standardmäßigen HTML-Formular Skripts, das zum Konfigurieren des Monitors verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54805-131">A pointer to a pointer to the address of the default HTML Form script used to configure the monitor.</span></span> <span data-ttu-id="54805-132">Obwohl die Instanzen des Monitors Ihr eigenes Skript ändern können, laden die meisten Monitore das Skript einfach einmal aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="54805-132">Although the instances of the monitor can alter their own script, most monitors simply load their script once, from a file.</span></span> <span data-ttu-id="54805-133">Der Wert von *ppdefaultscript* kann **null** sein. der Monitor kann jedoch nicht extern konfiguriert werden, oder er muss später ein Skript bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="54805-133">The value of *ppDefaultScript* can be **NULL**; however, then either the monitor cannot be externally configured, or it must supply a script later.</span></span> <span data-ttu-id="54805-134">Es ist effizienter, hier ein Standardskript bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="54805-134">It is more efficient to supply a default script here.</span></span>

</dd> <dt>

<span data-ttu-id="54805-135">*ppdefaultconfig* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="54805-135">*ppDefaultConfig* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54805-136">Die Adresse der Standard Zeichenfolge, die verwendet wird, um den Monitor zu konfigurieren, wenn er erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="54805-136">The address of the default string used to configure the monitor when it is created.</span></span> <span data-ttu-id="54805-137">Dieser Parameter kann auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="54805-137">This parameter can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54805-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54805-138">Return value</span></span>

<span data-ttu-id="54805-139">Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK. Dies entspricht noError.</span><span class="sxs-lookup"><span data-stu-id="54805-139">If the function is successful, the return value is S\_OK; which is the same as NOERROR.</span></span>

<span data-ttu-id="54805-140">Wenn die Funktion nicht erfolgreich ist, wird der angegebene Monitor von der mcsvc aus allen Listen ausgelassen. nach kann kein Monitor dieses Typs erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="54805-140">If the function is unsuccessful, the MCSVC omits the specified monitor from all its lists; after, no monitor of this type can be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="54805-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54805-141">Remarks</span></span>

<span data-ttu-id="54805-142">Die **onloadingdll** -Funktion wird von mcsvc einmal aufgerufen, wenn die dll zum ersten Mal geladen wird.</span><span class="sxs-lookup"><span data-stu-id="54805-142">The **OnLoadingDLL** function is called once by the MCSVC, when it first loads the DLL.</span></span> <span data-ttu-id="54805-143">Die dll stellt dann die Standardwerte bereit, die von mcsvc beim Erstellen einer Instanz eines Monitors verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54805-143">The DLL then provides the default values that will be used by the MCSVC when creating an instance of a monitor.</span></span>

<span data-ttu-id="54805-144">Der Monitor muss den gesamten erforderlichen Arbeitsspeicher für die Zeichen folgen zuordnen, die an mcsvc zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54805-144">The monitor must allocate all the necessary memory for the strings returned to the MCSVC.</span></span> <span data-ttu-id="54805-145">Bei der Rückgabe werden von mcsvc Kopien aller Zeichen folgen erstellt, und es wird nicht versucht, die zurückgegebenen Zeichen folgen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="54805-145">On return, the MCSVC makes copies of all the strings and will not attempt to free the returned strings.</span></span>

<span data-ttu-id="54805-146">Der Monitor sollte BLOB-Hilfsobjekte verwenden, um das filterblob zu ändern.</span><span class="sxs-lookup"><span data-stu-id="54805-146">The monitor should use BLOB helper functions to alter the filter BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="54805-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54805-147">Requirements</span></span>



| <span data-ttu-id="54805-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54805-148">Requirement</span></span> | <span data-ttu-id="54805-149">Wert</span><span class="sxs-lookup"><span data-stu-id="54805-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="54805-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54805-150">Minimum supported client</span></span><br/> | <span data-ttu-id="54805-151">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54805-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="54805-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54805-152">Minimum supported server</span></span><br/> | <span data-ttu-id="54805-153">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54805-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="54805-154">Header</span><span class="sxs-lookup"><span data-stu-id="54805-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="54805-155"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="54805-155"><dt>Netmon.h</dt></span></span> </dl> |



 

 




