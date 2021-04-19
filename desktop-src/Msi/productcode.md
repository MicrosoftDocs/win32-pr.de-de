---
description: Die ProductCode-Eigenschaft ist ein eindeutiger Bezeichner für die jeweilige Produktversion, die als Zeichen folgen-GUID dargestellt wird, z \# . b. &0034; {12345678-1234-1234-1234-123456789012}&\# 0034;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: ProductCode-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a714687ab49bca07d1137b3395cb19ddba0944
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372631"
---
# <a name="productcode-property"></a><span data-ttu-id="b7734-103">ProductCode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7734-103">ProductCode property</span></span>

<span data-ttu-id="b7734-104">Die **ProductCode** -Eigenschaft ist ein eindeutiger Bezeichner für die jeweilige Produktversion, die als Zeichen folgen- [GUID](guid.md)dargestellt wird, z {12345678-1234-1234-1234-123456789012} . b. "".</span><span class="sxs-lookup"><span data-stu-id="b7734-104">The **ProductCode** property is a unique identifier for the particular product release, represented as a string [GUID](guid.md), for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="b7734-105">Die in dieser GUID verwendeten Buchstaben müssen in Großbuchstaben angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b7734-105">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="b7734-106">Diese ID muss für verschiedene Versionen und Sprachen variieren.</span><span class="sxs-lookup"><span data-stu-id="b7734-106">This ID must vary for different versions and languages.</span></span>

<span data-ttu-id="b7734-107">Bei einem Produkt Upgrade, bei dem ein Produkt in ein völlig neues Produkt aktualisiert wird, muss auch der Produktcode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b7734-107">A product upgrade that updates a product into an entirely new product must also change the product code.</span></span> <span data-ttu-id="b7734-108">Den 32-Bit-und 64-Bit-Versionen des Pakets einer Anwendung müssen unterschiedliche Produktcodes zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b7734-108">The 32-bit and 64-bit versions of an application's package must be assigned different product codes.</span></span>

<span data-ttu-id="b7734-109">**ProductCode** wird als Produkt Eigenschaft angekündigt und ist die primäre Methode zum Angeben des Produkts.</span><span class="sxs-lookup"><span data-stu-id="b7734-109">The **ProductCode** is advertised as a product property, and is the primary method of specifying the product.</span></span> <span data-ttu-id="b7734-110">Diese Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b7734-110">This property is REQUIRED.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7734-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7734-111">Requirements</span></span>



| <span data-ttu-id="b7734-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7734-112">Requirement</span></span> | <span data-ttu-id="b7734-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b7734-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7734-114">Version</span><span class="sxs-lookup"><span data-stu-id="b7734-114">Version</span></span><br/> | <span data-ttu-id="b7734-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b7734-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b7734-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b7734-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b7734-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7734-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b7734-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b7734-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7734-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7734-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7734-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7734-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




