---
description: Die productelevated-Eigenschaft des Installer-Objekts gibt true zurück, wenn das Produkt verwaltet wird, oder false, wenn das Produkt nicht verwaltet wird.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Installer::P roductelevated-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367818"
---
# <a name="installerproductelevated-property"></a><span data-ttu-id="1ae6a-103">Installer::P roductelevated-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ae6a-103">Installer::ProductElevated property</span></span>

<span data-ttu-id="1ae6a-104">Die **productelevated** -Eigenschaft des [**Installer**](installer-object.md) -Objekts gibt true zurück, wenn das Produkt verwaltet wird, oder false, wenn das Produkt nicht verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-104">The **ProductElevated** property of the [**Installer**](installer-object.md) object returns True if the product is managed or False if the product is not managed.</span></span>

<span data-ttu-id="1ae6a-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae6a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae6a-106">Syntax</span></span>


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a><span data-ttu-id="1ae6a-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1ae6a-107">Property value</span></span>

<span data-ttu-id="1ae6a-108">Die vollständige Produktcode-GUID des Produkts.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-108">The full product code GUID of the product.</span></span> <span data-ttu-id="1ae6a-109">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae6a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ae6a-110">Remarks</span></span>

<span data-ttu-id="1ae6a-111">Die **productelevated** -Eigenschaft verwendet die [**msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-111">The **ProductElevated** property uses the [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) function.</span></span> <span data-ttu-id="1ae6a-112">Bei der Rückgabe der Eigenschaft wird die [alwaysinstallerhöhten](alwaysinstallelevated.md) -Richtlinie nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-112">The return of the property does not take into account the [AlwaysInstallElevated](alwaysinstallelevated.md) policy.</span></span>

## <a name="examples"></a><span data-ttu-id="1ae6a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ae6a-113">Examples</span></span>

<span data-ttu-id="1ae6a-114">Im folgenden Beispielskript wird die Verwendung der **productelevated** -Eigenschaft veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-114">The following sample script demonstrates the use of the **ProductElevated** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a><span data-ttu-id="1ae6a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ae6a-115">Requirements</span></span>



| <span data-ttu-id="1ae6a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ae6a-116">Requirement</span></span> | <span data-ttu-id="1ae6a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1ae6a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae6a-118">Version</span><span class="sxs-lookup"><span data-stu-id="1ae6a-118">Version</span></span><br/> | <span data-ttu-id="1ae6a-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1ae6a-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1ae6a-121">Windows Installer 4,5 unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ae6a-121">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="1ae6a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1ae6a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ae6a-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ae6a-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="1ae6a-124">IID</span><span class="sxs-lookup"><span data-stu-id="1ae6a-124">IID</span></span><br/>     | <span data-ttu-id="1ae6a-125">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1ae6a-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="1ae6a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ae6a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae6a-127">**Installationsprogramm**</span><span class="sxs-lookup"><span data-stu-id="1ae6a-127">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="1ae6a-128">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ae6a-128">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




