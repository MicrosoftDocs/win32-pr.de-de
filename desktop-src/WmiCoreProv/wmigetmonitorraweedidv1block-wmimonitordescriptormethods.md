---
description: Ruft die unformatierten Daten für eine angegebene (durch VESA) erweiterte, erweiterte Display Identification Data (E-EDID)-Struktur (Video Electronics Standard Association) ab, die die optimalen Einstellungen für die Konfiguration eines Monitors definiert.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: WmiGetMonitorRawEEdidV1Block-Methode der wmimonitordescriptormethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364158"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a><span data-ttu-id="20e96-103">WmiGetMonitorRawEEdidV1Block-Methode der wmimonitordescriptormethods-Klasse</span><span class="sxs-lookup"><span data-stu-id="20e96-103">WmiGetMonitorRawEEdidV1Block method of the WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="20e96-104">Die **WmiGetMonitorRawEEdidV1Block** -Methode ruft die unformatierten Daten für eine angegebene (VESA) erweiterte, erweiterte Anzeige Identifikationsdaten (etedid)-Struktur (Video Electronics Standard Association) ab, die die optimalen Einstellungen für die Konfiguration eines Monitors definiert.</span><span class="sxs-lookup"><span data-stu-id="20e96-104">The **WmiGetMonitorRawEEdidV1Block** method gets the raw data for a specified Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure that defines optimal settings for configuring a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20e96-105">Syntax</span></span>


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a><span data-ttu-id="20e96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20e96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20e96-107">*Blockid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20e96-107">*BlockId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20e96-108">Die Datenblock Identität.</span><span class="sxs-lookup"><span data-stu-id="20e96-108">The data block identity.</span></span>

</dd> <dt>

<span data-ttu-id="20e96-109">*BlockType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="20e96-109">*BlockType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20e96-110">Der Typ des Datenblocks.</span><span class="sxs-lookup"><span data-stu-id="20e96-110">Type of data block.</span></span> <span data-ttu-id="20e96-111">In der folgenden Tabelle sind mögliche Rückgabewerte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="20e96-111">The following table lists possible return values.</span></span>



| <span data-ttu-id="20e96-112">Wert</span><span class="sxs-lookup"><span data-stu-id="20e96-112">Value</span></span>                                                                                 | <span data-ttu-id="20e96-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="20e96-113">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="20e96-114"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="20e96-114"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="20e96-115">Uninitialized</span><span class="sxs-lookup"><span data-stu-id="20e96-115">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="20e96-116"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="20e96-116"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="20e96-117">EDID-Basisblock</span><span class="sxs-lookup"><span data-stu-id="20e96-117">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="20e96-118"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="20e96-118"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="20e96-119">EDID-Block Zuordnung</span><span class="sxs-lookup"><span data-stu-id="20e96-119">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="20e96-120"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="20e96-120"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="20e96-121">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="20e96-121">Other</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="20e96-122">*Blockcontent* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="20e96-122">*BlockContent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20e96-123">Ein 128-Byte-Array, das den Rohdaten Block Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="20e96-123">A 128-byte array that contains the raw block content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20e96-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20e96-124">Return value</span></span>

<span data-ttu-id="20e96-125">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="20e96-125">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="20e96-126">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="20e96-126">Any other number indicates an error.</span></span> <span data-ttu-id="20e96-127">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="20e96-127">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="20e96-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20e96-128">Examples</span></span>

<span data-ttu-id="20e96-129">Im folgenden Codebeispiel werden die EDID-Blöcke jeder Anzeige als RAW-128-Bit-Arrays abgerufen.</span><span class="sxs-lookup"><span data-stu-id="20e96-129">The following code example retrieves the EDID blocks of any display as raw 128 bit arrays.</span></span>


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="20e96-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20e96-130">Requirements</span></span>



| <span data-ttu-id="20e96-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20e96-131">Requirement</span></span> | <span data-ttu-id="20e96-132">Wert</span><span class="sxs-lookup"><span data-stu-id="20e96-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20e96-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20e96-133">Minimum supported client</span></span><br/> | <span data-ttu-id="20e96-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20e96-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="20e96-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20e96-135">Minimum supported server</span></span><br/> | <span data-ttu-id="20e96-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20e96-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="20e96-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="20e96-137">Namespace</span></span><br/>                | <span data-ttu-id="20e96-138">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="20e96-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="20e96-139">MOF</span><span class="sxs-lookup"><span data-stu-id="20e96-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20e96-140"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="20e96-140"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="20e96-141">DLL</span><span class="sxs-lookup"><span data-stu-id="20e96-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20e96-142"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20e96-142"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20e96-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20e96-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e96-144">**Wmimonitordescriptormethods**</span><span class="sxs-lookup"><span data-stu-id="20e96-144">**WmiMonitorDescriptorMethods**</span></span>](wmimonitordescriptormethods.md)
</dt> <dt>

[<span data-ttu-id="20e96-145">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="20e96-145">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

