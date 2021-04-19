---
description: Die productinfofromscript-Eigenschaft des Installer-Objekts gibt den Wert des angegebenen Attributs zurück, das in einem Ankündigungs Skript gespeichert ist.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Installer::P der Eigenschaft "roductinfofromscript"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372483"
---
# <a name="installerproductinfofromscript-property"></a><span data-ttu-id="94bfe-103">Installer::P der Eigenschaft "roductinfofromscript"</span><span class="sxs-lookup"><span data-stu-id="94bfe-103">Installer::ProductInfoFromScript property</span></span>

<span data-ttu-id="94bfe-104">Die **productinfofromscript** -Eigenschaft des [**Installer**](installer-object.md) -Objekts gibt den Wert des angegebenen Attributs zurück, das in einem Ankündigungs Skript gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="94bfe-104">The **ProductInfoFromScript** property of the [**Installer**](installer-object.md) object returns the value of the specified attribute that is stored in an advertise script.</span></span>

<span data-ttu-id="94bfe-105">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="94bfe-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="94bfe-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94bfe-106">Syntax</span></span>


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a><span data-ttu-id="94bfe-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="94bfe-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="94bfe-108">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="94bfe-108">Error codes</span></span>

<span data-ttu-id="94bfe-109">Eine Zeichenfolge oder ein ganzzahliger Wert, abhängig vom angeforderten Attribut.</span><span class="sxs-lookup"><span data-stu-id="94bfe-109">A string or integer value depending upon requested attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="94bfe-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94bfe-110">Remarks</span></span>

<span data-ttu-id="94bfe-111">Die **productinfofromscript** -Eigenschaft verwendet die [**msigetproductinfofromscript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="94bfe-111">The **ProductInfoFromScript** property uses the [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) function.</span></span>

## <a name="examples"></a><span data-ttu-id="94bfe-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94bfe-112">Examples</span></span>

<span data-ttu-id="94bfe-113">Das folgende Beispielskript veranschaulicht die Verwendung der **productinfofromscript** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="94bfe-113">The following sample script demonstrates the use of the **ProductInfoFromScript** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a><span data-ttu-id="94bfe-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94bfe-114">Requirements</span></span>



| <span data-ttu-id="94bfe-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94bfe-115">Requirement</span></span> | <span data-ttu-id="94bfe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="94bfe-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94bfe-117">Version</span><span class="sxs-lookup"><span data-stu-id="94bfe-117">Version</span></span><br/> | <span data-ttu-id="94bfe-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="94bfe-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="94bfe-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="94bfe-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="94bfe-120">Windows Installer 4,5 unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="94bfe-120">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="94bfe-121">DLL</span><span class="sxs-lookup"><span data-stu-id="94bfe-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="94bfe-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94bfe-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="94bfe-123">IID</span><span class="sxs-lookup"><span data-stu-id="94bfe-123">IID</span></span><br/>     | <span data-ttu-id="94bfe-124">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="94bfe-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="94bfe-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94bfe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94bfe-126">**Installationsprogramm**</span><span class="sxs-lookup"><span data-stu-id="94bfe-126">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="94bfe-127">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94bfe-127">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




