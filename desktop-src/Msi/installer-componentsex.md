---
description: Gibt ein RecordList-Objekt zurück, das installierte Komponenten auflistet.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Installer. componentsex (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372623"
---
# <a name="installercomponentsex-property"></a><span data-ttu-id="f485f-103">Installer. componentsex (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f485f-103">Installer.ComponentsEx property</span></span>

<span data-ttu-id="f485f-104">Diese Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das installierte Komponenten auflistet.</span><span class="sxs-lookup"><span data-stu-id="f485f-104">This property returns a [**RecordList**](recordlist-object.md) object that lists installed components.</span></span> <span data-ttu-id="f485f-105">Diese Eigenschaft ruft [**msienumschlag componentsex**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)auf.</span><span class="sxs-lookup"><span data-stu-id="f485f-105">This property calls [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span></span>

<span data-ttu-id="f485f-106">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f485f-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="f485f-107">Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f485f-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="f485f-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f485f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f485f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f485f-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a><span data-ttu-id="f485f-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f485f-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="f485f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f485f-111">Requirements</span></span>



| <span data-ttu-id="f485f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f485f-112">Requirement</span></span> | <span data-ttu-id="f485f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f485f-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f485f-114">Version</span><span class="sxs-lookup"><span data-stu-id="f485f-114">Version</span></span><br/> | <span data-ttu-id="f485f-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="f485f-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="f485f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f485f-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="f485f-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f485f-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="f485f-118">IID</span><span class="sxs-lookup"><span data-stu-id="f485f-118">IID</span></span><br/>     | <span data-ttu-id="f485f-119">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f485f-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f485f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f485f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f485f-121">**Msienumschlag**</span><span class="sxs-lookup"><span data-stu-id="f485f-121">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




