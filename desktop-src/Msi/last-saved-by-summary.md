---
description: Das Installationsprogramm legt die zuletzt gespeicherte Eigenschaft durch Summary auf einen Wert fest, der davon abhängt, ob es sich um ein Installationspaket, eine Transformation oder ein Patchpaket handelt. In einem Installationspaket legt das Installationsprogramm diese Eigenschaft während einer administrativen Installation auf den Wert der LogonUser-Eigenschaft fest. Entwickler von Tools zur Datenbankbearbeitung können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person zum Ändern der Installations Datenbank zu verfolgen. Diese Eigenschaft sollte in einer abschließenden Versand Datenbank auf NULL festgelegt werden. Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss Sie nicht ändern. In einer Transformation enthält diese Zusammenfassungs Eigenschaft die Plattform-und Sprach-IDs, die eine Datenbank haben sollte, nachdem Sie transformiert wurde. Die-Eigenschaft gibt an, wie die Vorlagen Zusammenfassung in der neuen Datenbank festgelegt werden soll. In einem Patchpaket enthält diese Zusammenfassungs Eigenschaft eine durch Semikolons getrennte Liste der Namen der Transformations unter Speicher in der Reihenfolge, in der Sie von diesem Patch angewendet werden.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Zuletzt durch Summary-Eigenschaft gespeichert
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366798"
---
# <a name="last-saved-by-summary-property"></a><span data-ttu-id="1bcc3-107">Zuletzt durch Summary-Eigenschaft gespeichert</span><span class="sxs-lookup"><span data-stu-id="1bcc3-107">Last Saved By Summary property</span></span>

<span data-ttu-id="1bcc3-108">Das Installationsprogramm legt die **zuletzt gespeicherte Eigenschaft durch Summary** auf einen Wert fest, der davon abhängt, ob es sich um ein Installationspaket, eine Transformation oder ein Patchpaket handelt.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-108">The installer sets the **Last Saved by Summary** Property to a value that depends on whether this is an installation package, transform, or patch package.</span></span>

<span data-ttu-id="1bcc3-109">In einem Installationspaket legt das Installationsprogramm diese Eigenschaft während einer [administrativen Installation](administrative-installation.md)auf den Wert der [**LogonUser**](logonuser.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-109">In an installation package, the installer sets this property to the value of the [**LogonUser**](logonuser.md) property during an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="1bcc3-110">Entwickler von Tools zur Datenbankbearbeitung können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person zum Ändern der Installations Datenbank zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-110">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="1bcc3-111">Diese Eigenschaft sollte in einer abschließenden Versand Datenbank auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-111">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="1bcc3-112">Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss Sie nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-112">The installer never uses this property and a user never needs to modify it.</span></span>

<span data-ttu-id="1bcc3-113">In einer Transformation enthält diese Zusammenfassungs Eigenschaft die Plattform-und Sprach-IDs, die eine Datenbank haben sollte, nachdem Sie transformiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-113">In a transform, this summary property contains the platform and language ID(s) that a database should have after it has been transformed.</span></span> <span data-ttu-id="1bcc3-114">Die-Eigenschaft gibt an, wie die [**Vorlagen Zusammenfassung**](template-summary.md) in der neuen Datenbank festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-114">The property specifies to what the [**Template Summary**](template-summary.md) should be set in the new database.</span></span>

<span data-ttu-id="1bcc3-115">In einem Patchpaket enthält diese Zusammenfassungs Eigenschaft eine durch Semikolons getrennte Liste der Namen der Transformations unter Speicher in der Reihenfolge, in der Sie von diesem Patch angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-115">In a patch package, this summary property contains a semicolon-delimited list of transform substorage names in the order they are applied by this patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bcc3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bcc3-116">Requirements</span></span>



| <span data-ttu-id="1bcc3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bcc3-117">Requirement</span></span> | <span data-ttu-id="1bcc3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1bcc3-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bcc3-119">Version</span><span class="sxs-lookup"><span data-stu-id="1bcc3-119">Version</span></span><br/> | <span data-ttu-id="1bcc3-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1bcc3-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1bcc3-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1bcc3-122">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="1bcc3-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1bcc3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bcc3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bcc3-124">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1bcc3-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




