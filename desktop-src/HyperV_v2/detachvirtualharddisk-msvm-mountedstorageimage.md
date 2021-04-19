---
description: Trennt das bereitgestellte Speicher Abbild, das dieser Klasse zugeordnet ist.
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Detachvirtualharddisk-Methode der Msvm_MountedStorageImage-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0d411134d85fe70163b2e08eebed0ff0d4b88e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356929"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a><span data-ttu-id="387ea-103">Detachvirtualharddisk-Methode der MSVM \_ mountedstorageimage-Klasse</span><span class="sxs-lookup"><span data-stu-id="387ea-103">DetachVirtualHardDisk method of the Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="387ea-104">Trennt das bereitgestellte Speicher Abbild, das dieser Klasse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="387ea-104">Detaches the mounted storage image that is associated with this class.</span></span>

## <a name="syntax"></a><span data-ttu-id="387ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="387ea-105">Syntax</span></span>


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a><span data-ttu-id="387ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="387ea-106">Parameters</span></span>

<span data-ttu-id="387ea-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="387ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="387ea-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="387ea-108">Return value</span></span>

<span data-ttu-id="387ea-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="387ea-109">Type: **uint32**</span></span>

<span data-ttu-id="387ea-110">Diese Methode kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="387ea-110">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="387ea-111">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="387ea-111">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="387ea-112">Fehler **(1** )</span><span class="sxs-lookup"><span data-stu-id="387ea-112">**Failed** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="387ea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="387ea-113">Remarks</span></span>

<span data-ttu-id="387ea-114">Der Zugriff auf die [**MSVM \_ mountedstorageimage**](msvm-mountedstorageimage.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="387ea-114">Access to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="387ea-115">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="387ea-115">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="387ea-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="387ea-116">Examples</span></span>

<span data-ttu-id="387ea-117">Im folgenden c#-Beispiel wird gezeigt, wie Sie eine virtuelle Festplatten Datei trennen.</span><span class="sxs-lookup"><span data-stu-id="387ea-117">The following C# example shows how to detach a virtual hard disk file.</span></span> <span data-ttu-id="387ea-118">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="387ea-118">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="387ea-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="387ea-119">Requirements</span></span>



| <span data-ttu-id="387ea-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="387ea-120">Requirement</span></span> | <span data-ttu-id="387ea-121">Wert</span><span class="sxs-lookup"><span data-stu-id="387ea-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="387ea-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="387ea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="387ea-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="387ea-123">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="387ea-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="387ea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="387ea-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="387ea-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="387ea-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="387ea-126">Namespace</span></span><br/>                | <span data-ttu-id="387ea-127">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="387ea-127">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="387ea-128">MOF</span><span class="sxs-lookup"><span data-stu-id="387ea-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="387ea-129"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="387ea-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="387ea-130">DLL</span><span class="sxs-lookup"><span data-stu-id="387ea-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="387ea-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="387ea-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="387ea-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="387ea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387ea-133">**MSVM \_ mountedstorageimage**</span><span class="sxs-lookup"><span data-stu-id="387ea-133">**Msvm\_MountedStorageImage**</span></span>](msvm-mountedstorageimage.md)
</dt> </dl>

 

