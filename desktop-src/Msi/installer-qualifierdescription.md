---
description: Die schreibgeschützte qualifierdescription-Eigenschaft gibt eine Text Zeichenfolge zurück, in der die qualifizierte Komponente beschrieben wird.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Installer. qualifierdescription (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365626"
---
# <a name="installerqualifierdescription-property"></a><span data-ttu-id="5b13d-103">Installer. qualifierdescription (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5b13d-103">Installer.QualifierDescription property</span></span>

<span data-ttu-id="5b13d-104">Die schreibgeschützte **qualifierdescription** -Eigenschaft gibt eine Text Zeichenfolge zurück, in der die qualifizierte Komponente beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5b13d-104">The read-only **QualifierDescription** property returns a text string describing the qualified component.</span></span> <span data-ttu-id="5b13d-105">Diese lokalisierbare Zeichenfolge wird in der APPDATA-Spalte der [PublishComponent-Tabelle](publishcomponent-table.md) erstellt und kann für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5b13d-105">This localizable string is authored into the AppData column of the [PublishComponent table](publishcomponent-table.md) and can be displayed to the user.</span></span> <span data-ttu-id="5b13d-106">Der Qualifizierer unterscheidet mehrere Formen derselben Komponente, z. b. eine Komponente, die in mehreren Sprachen implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="5b13d-106">The qualifier distinguishes multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span>

<span data-ttu-id="5b13d-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5b13d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b13d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b13d-108">Syntax</span></span>


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a><span data-ttu-id="5b13d-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5b13d-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5b13d-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b13d-110">Requirements</span></span>



| <span data-ttu-id="5b13d-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b13d-111">Requirement</span></span> | <span data-ttu-id="5b13d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5b13d-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b13d-113">Version</span><span class="sxs-lookup"><span data-stu-id="5b13d-113">Version</span></span><br/> | <span data-ttu-id="5b13d-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b13d-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5b13d-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b13d-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5b13d-116">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="5b13d-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5b13d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="5b13d-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b13d-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b13d-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5b13d-119">IID</span><span class="sxs-lookup"><span data-stu-id="5b13d-119">IID</span></span><br/>     | <span data-ttu-id="5b13d-120">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5b13d-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="5b13d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b13d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b13d-122">**Msienumschlag componentqualifizierer**</span><span class="sxs-lookup"><span data-stu-id="5b13d-122">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[<span data-ttu-id="5b13d-123">Qualifizierte Komponenten</span><span class="sxs-lookup"><span data-stu-id="5b13d-123">Qualified Components</span></span>](qualified-components.md)
</dt> </dl>

 

 




