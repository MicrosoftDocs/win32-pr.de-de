---
description: Gibt ein RecordList-Objekt zurück, das den vollständigen Pfad einer angegebenen installierten Komponente enthält.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Installer. componentpathex-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368467"
---
# <a name="installercomponentpathex-property"></a><span data-ttu-id="a18f5-103">Installer. componentpathex-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a18f5-103">Installer.ComponentPathEx property</span></span>

<span data-ttu-id="a18f5-104">Diese Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das den vollständigen Pfad einer angegebenen installierten Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="a18f5-104">This property returns a [**RecordList**](recordlist-object.md) object that gives the full path of a specified installed component.</span></span> <span data-ttu-id="a18f5-105">Diese Eigenschaft ruft [**msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)auf.</span><span class="sxs-lookup"><span data-stu-id="a18f5-105">This property calls [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span></span>

<span data-ttu-id="a18f5-106">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a18f5-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="a18f5-107">Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a18f5-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="a18f5-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a18f5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a18f5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a18f5-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a><span data-ttu-id="a18f5-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a18f5-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a18f5-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a18f5-111">Requirements</span></span>



| <span data-ttu-id="a18f5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a18f5-112">Requirement</span></span> | <span data-ttu-id="a18f5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a18f5-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a18f5-114">Version</span><span class="sxs-lookup"><span data-stu-id="a18f5-114">Version</span></span><br/> | <span data-ttu-id="a18f5-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="a18f5-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="a18f5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a18f5-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="a18f5-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a18f5-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="a18f5-118">IID</span><span class="sxs-lookup"><span data-stu-id="a18f5-118">IID</span></span><br/>     | <span data-ttu-id="a18f5-119">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a18f5-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="a18f5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a18f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18f5-121">**Msigetcomponentpathex**</span><span class="sxs-lookup"><span data-stu-id="a18f5-121">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




