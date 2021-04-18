---
description: Generiert einen Satz von World Wide Port Names (WWPNs).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Generatewwpn-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368115"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="48b49-103">Generatewwpn-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="48b49-103">GenerateWwpn method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="48b49-104">Generiert einen Satz von World Wide Port Names (WWPNs).</span><span class="sxs-lookup"><span data-stu-id="48b49-104">Generates a set of World Wide Port Names (WWPNs).</span></span> <span data-ttu-id="48b49-105">Die WWPNs werden aus dem vorkonfigurierten Bereich generiert, der in den Eigenschaften **minimumwwpnaddress** und **maximumwwpnaddress** der [**MSVM \_ virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md) -Klasse definiert ist.</span><span class="sxs-lookup"><span data-stu-id="48b49-105">The WWPNs are generated from within the pre-configured range defined by the **MinimumWWPNAddress** and **MaximumWWPNAddress** properties of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span> <span data-ttu-id="48b49-106">Wenn die gültige Anzahl von WWPNs, die generiert werden können, kleiner ist als die angeforderte Anzahl, haben die restlichen Einträge im *generatedwwpn* -Array den ungültigen Eintrag "0000000000000000", und der Rückgabewert gibt Erfolg (0) an.</span><span class="sxs-lookup"><span data-stu-id="48b49-106">If the valid number of WWPNs that can be generated is less than the requested number, then the remaining entries in the *GeneratedWwpn* array will have the invalid entry of "0000000000000000" and the return value will indicate success (0).</span></span>

## <a name="syntax"></a><span data-ttu-id="48b49-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b49-107">Syntax</span></span>


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a><span data-ttu-id="48b49-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="48b49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b49-109">*Anzahl der WWPNs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48b49-109">*NumberOfWwpns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b49-110">Die Anzahl der zu generierenden WWPNs.</span><span class="sxs-lookup"><span data-stu-id="48b49-110">The number of WWPNs to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="48b49-111">*Generatedwwpn* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="48b49-111">*GeneratedWwpn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48b49-112">Ein Array von Zeichen folgen, von denen jede einen generierten WWPN enthält.</span><span class="sxs-lookup"><span data-stu-id="48b49-112">An array of strings, each of which will contain a generated WWPN.</span></span> <span data-ttu-id="48b49-113">Er wird im Zeichen folgen Format als "01:23:45:67:89: ab: CD: EF" formatiert.</span><span class="sxs-lookup"><span data-stu-id="48b49-113">It will be formatted in string form as "01:23:45:67:89:ab:cd:ef".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b49-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48b49-114">Return value</span></span>

<span data-ttu-id="48b49-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="48b49-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="48b49-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="48b49-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="48b49-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="48b49-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="48b49-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="48b49-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="48b49-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="48b49-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="48b49-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="48b49-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="48b49-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="48b49-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="48b49-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="48b49-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="48b49-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b49-128">Requirements</span></span>



| <span data-ttu-id="48b49-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b49-129">Requirement</span></span> | <span data-ttu-id="48b49-130">Wert</span><span class="sxs-lookup"><span data-stu-id="48b49-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48b49-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b49-131">Minimum supported client</span></span><br/> | <span data-ttu-id="48b49-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b49-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="48b49-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b49-133">Minimum supported server</span></span><br/> | <span data-ttu-id="48b49-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b49-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48b49-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="48b49-135">Namespace</span></span><br/>                | <span data-ttu-id="48b49-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="48b49-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="48b49-137">MOF</span><span class="sxs-lookup"><span data-stu-id="48b49-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48b49-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48b49-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48b49-139">DLL</span><span class="sxs-lookup"><span data-stu-id="48b49-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48b49-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48b49-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48b49-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b49-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b49-142">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="48b49-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




