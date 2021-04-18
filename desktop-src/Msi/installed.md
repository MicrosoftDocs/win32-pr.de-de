---
description: Die installierte Eigenschaft wird nur festgelegt, wenn das Produkt pro Computer oder für den aktuellen Benutzer installiert ist.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Installierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358648"
---
# <a name="installed-property"></a><span data-ttu-id="4750f-103">Installierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4750f-103">Installed property</span></span>

<span data-ttu-id="4750f-104">Die **installierte** Eigenschaft wird nur festgelegt, wenn das Produkt pro Computer oder für den aktuellen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4750f-104">The **Installed** property is set only if the product is installed per-machine or for the current user.</span></span> <span data-ttu-id="4750f-105">Diese Eigenschaft ist nicht festgelegt, wenn das Produkt für einen anderen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4750f-105">This property is not set if the product is installed for a different user.</span></span>

<span data-ttu-id="4750f-106">Die **installierte** Eigenschaft kann in bedingten Ausdrücken verwendet werden, um zu bestimmen, ob ein Produkt pro Computer oder für den aktuellen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4750f-106">The **Installed** property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="4750f-107">Beispielsweise kann die-Eigenschaft in der Bedingungs Spalte einer Sequenz Tabelle oder zur Unterscheidung zwischen einer ersten Installation und einer Wartungs Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4750f-107">For example, the property can be used in the conditional column of a sequence table or to differentiate between a first installation and a maintenance installation.</span></span>

<span data-ttu-id="4750f-108">Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) , um zu bestimmen, ob das Produkt für einen anderen Benutzer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4750f-108">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="4750f-109">Der Wert der [**ProductVersion**](productversion.md) -Eigenschaft ist die Version des Produkts im Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="4750f-109">The value of the [**ProductVersion**](productversion.md) property is the version of the product in string format.</span></span>

## <a name="requirements"></a><span data-ttu-id="4750f-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4750f-110">Requirements</span></span>



| <span data-ttu-id="4750f-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4750f-111">Requirement</span></span> | <span data-ttu-id="4750f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4750f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4750f-113">Version</span><span class="sxs-lookup"><span data-stu-id="4750f-113">Version</span></span><br/> | <span data-ttu-id="4750f-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4750f-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4750f-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4750f-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4750f-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4750f-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4750f-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4750f-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4750f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4750f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4750f-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4750f-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




