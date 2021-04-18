---
description: Die Sicherheits Zusammenfassungs Eigenschaft gibt an, ob das Paket schreibgeschützt geöffnet werden soll.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Sicherheits Zusammenfassungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371714"
---
# <a name="security-summary-property"></a><span data-ttu-id="1213f-103">Sicherheits Zusammenfassungs Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1213f-103">Security Summary property</span></span>

<span data-ttu-id="1213f-104">Die **Sicherheits Zusammenfassungs** Eigenschaft gibt an, ob das Paket schreibgeschützt geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1213f-104">The **Security Summary** property conveys whether the package should be opened as read-only.</span></span> <span data-ttu-id="1213f-105">Das Tool zum Bearbeiten von Datenbanken sollte eine schreibgeschützte erzwungene Datenbank nicht ändern und sollte bei versuchen, eine schreibgeschützte Datenbank zu ändern, eine Warnung ausgeben.</span><span class="sxs-lookup"><span data-stu-id="1213f-105">The database editing tool should not modify a read-only enforced database and should issue a warning at attempts to modify a read-only recommended database.</span></span> <span data-ttu-id="1213f-106">Die folgenden Werte dieser Eigenschaft sind auf Windows Installer Dateien anwendbar.</span><span class="sxs-lookup"><span data-stu-id="1213f-106">The following values of this property are applicable to Windows Installer files.</span></span>



| <span data-ttu-id="1213f-107">Wert</span><span class="sxs-lookup"><span data-stu-id="1213f-107">Value</span></span> | <span data-ttu-id="1213f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1213f-108">Description</span></span>           |
|-------|-----------------------|
| <span data-ttu-id="1213f-109">0</span><span class="sxs-lookup"><span data-stu-id="1213f-109">0</span></span>     | <span data-ttu-id="1213f-110">Keine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="1213f-110">No restriction</span></span>        |
| <span data-ttu-id="1213f-111">2</span><span class="sxs-lookup"><span data-stu-id="1213f-111">2</span></span>     | <span data-ttu-id="1213f-112">Nur Lesen empfohlen</span><span class="sxs-lookup"><span data-stu-id="1213f-112">Read-only recommended</span></span> |
| <span data-ttu-id="1213f-113">4</span><span class="sxs-lookup"><span data-stu-id="1213f-113">4</span></span>     | <span data-ttu-id="1213f-114">Schreibgeschützt erzwungen</span><span class="sxs-lookup"><span data-stu-id="1213f-114">Read-only enforced</span></span>    |



 

<span data-ttu-id="1213f-115">Diese Eigenschaft sollte auf Read-Only empfohlen (2) für eine-Installations Datenbank und auf Schreib geschütztes erzwingen (4) für eine Transformation oder einen Patch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1213f-115">This property should be set to read-only recommended (2) for an installation database and to read-only enforced (4) for a transform or patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="1213f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1213f-116">Requirements</span></span>



| <span data-ttu-id="1213f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1213f-117">Requirement</span></span> | <span data-ttu-id="1213f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1213f-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1213f-119">Version</span><span class="sxs-lookup"><span data-stu-id="1213f-119">Version</span></span><br/> | <span data-ttu-id="1213f-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1213f-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1213f-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1213f-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1213f-122">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="1213f-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1213f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1213f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1213f-124">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1213f-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




