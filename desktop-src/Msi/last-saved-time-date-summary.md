---
description: Die zuletzt gespeicherte Zeit-/uhrzeitzusammenfassungs-Eigenschaft gibt den Zeitpunkt an, zu dem das Installationspaket, das Transform-oder das Patchpaket modified.Ini, und ein Autor sollte den Wert der zuletzt gespeicherten Datums-/uhrzeitzusammenfassungs-Eigenschaft auf NULL festlegen, um anzugeben, dass noch keine Änderungen am Paket vorgenommen wurden. Ein Autor sollte dann die zuletzt gespeicherte Zeit-/uhrzeitzusammenfassungs-Eigenschaft auf die aktuelle Systemzeit/das aktuelle Datum aktualisieren, wenn eine geänderte Installations Datenbank, eine geänderte Transformation oder ein Patchpaket gespeichert wird.
ms.assetid: be3957fa-463a-4eb2-8b9d-93a16e95a8cf
title: Zuletzt gespeicherte Zeit-/datzusammenfassungs-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfe2300640434a52a78575221dc69e0f7263883
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373879"
---
# <a name="last-saved-timedate-summary-property"></a><span data-ttu-id="55a1c-104">Zuletzt gespeicherte Zeit-/datzusammenfassungs-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55a1c-104">Last Saved Time/Date Summary property</span></span>

<span data-ttu-id="55a1c-105">Die **zuletzt gespeicherte Zeit-/uhrzeitzusammenfassungs-** Eigenschaft gibt den Zeitpunkt an, zu dem das Installationspaket, die Transformation oder das Patchpaket zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="55a1c-105">The **Last Saved Time/Date Summary** property conveys the last time when this installation package, transform, or patch package was modified.</span></span>

<span data-ttu-id="55a1c-106">Anfänglich sollte ein Autor den Wert der **zuletzt gespeicherten Zeit-/datezusammenfassungs-** Eigenschaft auf NULL festlegen, um anzugeben, dass noch keine Änderungen am Paket vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="55a1c-106">Initially, an author should set the value of the **Last Saved Time/Date Summary** property to Null to indicate that no changes have yet been made to the package.</span></span> <span data-ttu-id="55a1c-107">Ein Autor sollte dann die **zuletzt gespeicherte Zeit-/uhrzeitzusammenfassungs-** Eigenschaft auf die aktuelle Systemzeit/das aktuelle Datum aktualisieren, wenn eine geänderte Installations Datenbank, eine geänderte Transformation oder ein Patchpaket gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="55a1c-107">An author should then update the **Last Saved Time/Date Summary** property to the current system time/date each time a modified installation database, transform, or patch package is saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a1c-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55a1c-108">Requirements</span></span>



| <span data-ttu-id="55a1c-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55a1c-109">Requirement</span></span> | <span data-ttu-id="55a1c-110">Wert</span><span class="sxs-lookup"><span data-stu-id="55a1c-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a1c-111">Version</span><span class="sxs-lookup"><span data-stu-id="55a1c-111">Version</span></span><br/> | <span data-ttu-id="55a1c-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="55a1c-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="55a1c-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="55a1c-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="55a1c-114">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="55a1c-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55a1c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55a1c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a1c-116">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55a1c-116">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




