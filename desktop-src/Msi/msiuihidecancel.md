---
description: Diese Windows Installer Eigenschaft gibt an, wann die interne Benutzeroberflächen Ebene festgelegt wurde, um die Schaltfläche "Abbrechen" auszublenden.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Msiuihidecancel (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359702"
---
# <a name="msiuihidecancel-property"></a><span data-ttu-id="d01ab-103">Msiuihidecancel (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d01ab-103">MsiUIHideCancel property</span></span>

<span data-ttu-id="d01ab-104">Der Installer legt die **msiuihidecancel** -Eigenschaft auf 1 fest, wenn die interne Benutzeroberflächen Ebene so festgelegt wurde, dass Sie installuilevel \_ hidecancel mit der [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) -Funktion oder die [uilevel](installer-uilevel.md)-Eigenschaft des [**Installer**](installer-object.md) -Objekts oder mithilfe von [Befehlszeilenoptionen](command-line-options.md)einschließt.</span><span class="sxs-lookup"><span data-stu-id="d01ab-104">The installer sets the **MsiUIHideCancel** property to 1 when the internal user interface level has been set to include INSTALLUILEVEL\_HIDECANCEL with the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function or the [UILevel](installer-uilevel.md)property of the [**Installer**](installer-object.md) object or by using [Command Line Options](command-line-options.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d01ab-105">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d01ab-105">Requirements</span></span>



| <span data-ttu-id="d01ab-106">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d01ab-106">Requirement</span></span> | <span data-ttu-id="d01ab-107">Wert</span><span class="sxs-lookup"><span data-stu-id="d01ab-107">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01ab-108">Version</span><span class="sxs-lookup"><span data-stu-id="d01ab-108">Version</span></span><br/> | <span data-ttu-id="d01ab-109">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d01ab-109">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d01ab-110">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d01ab-110">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d01ab-111">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d01ab-111">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d01ab-112">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d01ab-112">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d01ab-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d01ab-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01ab-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d01ab-114">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d01ab-115">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d01ab-115">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




