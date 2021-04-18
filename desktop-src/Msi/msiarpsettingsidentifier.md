---
description: Die msiarpsettingsidentifier-Eigenschaft enthält eine durch Semikolons getrennte Liste der Registrierungs Speicherorte, an denen die Anwendung die Einstellungen und Einstellungen des Benutzers speichert.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Msiarpsettingsidentifier (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360976"
---
# <a name="msiarpsettingsidentifier-property"></a><span data-ttu-id="d6fb8-103">Msiarpsettingsidentifier (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d6fb8-103">MSIARPSETTINGSIDENTIFIER property</span></span>

<span data-ttu-id="d6fb8-104">Die **msiarpsettingsidentifier** -Eigenschaft enthält eine durch Semikolons getrennte Liste der Registrierungs Speicherorte, an denen die Anwendung die Einstellungen und Einstellungen des Benutzers speichert.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-104">The **MSIARPSETTINGSIDENTIFIER** property contains a semi-colon delimited list of the registry locations where the application stores a user's settings and preferences.</span></span> <span data-ttu-id="d6fb8-105">Während eines Upgrades des Betriebssystems kann das Setup diese Informationen verwenden, um die Benutzeroberflächen zu verbessern, die Anwendungen migrieren.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-105">During an operating system upgrade, setup can use this information to improve the experience of users who are migrating applications.</span></span>

<span data-ttu-id="d6fb8-106">Der Wert der Eigenschaft **msiarpsettingsidentifier** ist Literaltext, der die Liste der Registrierungs Orte enthält, in denen die Anwendung die Einstellungen speichert.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-106">The value of the **MSIARPSETTINGSIDENTIFIER** property is literal text that contains the list of registry locations where the application stores its settings.</span></span> <span data-ttu-id="d6fb8-107">Der Wert kann mehrere mögliche Registrierungs Speicherorte angeben.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-107">The value can specify multiple possible registry locations.</span></span> <span data-ttu-id="d6fb8-108">Trennen Sie mehrere Registrierungs Speicherorte mithilfe von Semikolons.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-108">Separate multiple registry locations by using semi-colons.</span></span> <span data-ttu-id="d6fb8-109">Anwendungseinstellungen werden in der Regel in den **HKCU** -oder **HKLM** -Registrierungs Strukturen in der Form gespeichert: *Unternehmens \\ Anwendungs \\ Version*.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-109">Application settings are typically stored in the **HKCU** or **HKLM** registry hives in the form: *Company\\Application\\Version*.</span></span> <span data-ttu-id="d6fb8-110">Das folgende Beispiel ist ein möglicher Wert für die **msiarpsettingsidentifier** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-110">The following example is a possible value for the **MSIARPSETTINGSIDENTIFIER** property.</span></span>

<span data-ttu-id="d6fb8-111">*MyCompany \\ appsuite \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ App2 \\ 1,0*</span><span class="sxs-lookup"><span data-stu-id="d6fb8-111">*MyCompany\\AppSuite\\1.0;MyCompany\\App1\\1.0;MyCompany\\App2\\1.0*</span></span>

<span data-ttu-id="d6fb8-112">Diese Eigenschaft ist optional und kann in der [Eigenschaften](property-table.md) Tabelle festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-112">This property is optional and can be set in the [Property](property-table.md) table.</span></span> <span data-ttu-id="d6fb8-113">Wenn diese Eigenschaft in der Eigenschaften Tabelle angezeigt wird, darf der Wert nicht auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-113">If this property appears in the Property table, the value must not be set to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6fb8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6fb8-114">Requirements</span></span>



| <span data-ttu-id="d6fb8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6fb8-115">Requirement</span></span> | <span data-ttu-id="d6fb8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d6fb8-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fb8-117">Version</span><span class="sxs-lookup"><span data-stu-id="d6fb8-117">Version</span></span><br/> | <span data-ttu-id="d6fb8-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6fb8-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6fb8-120">Windows Installer 4,5 unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-120">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d6fb8-121">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d6fb8-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6fb8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6fb8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fb8-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6fb8-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d6fb8-124">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6fb8-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




