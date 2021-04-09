---
description: Jeder Typ von Sicherungs fähigen Objekten verfügt über einen Satz von Zugriffsrechten, die den für diesen Objekttyp spezifischen Vorgängen entsprechen.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Standard Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863003"
---
# <a name="standard-access-rights"></a><span data-ttu-id="faa68-103">Standard Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="faa68-103">Standard Access Rights</span></span>

<span data-ttu-id="faa68-104">Jeder Typ von Sicherungs fähigen Objekten verfügt über einen Satz von Zugriffsrechten, die den für diesen Objekttyp spezifischen Vorgängen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="faa68-104">Each type of securable object has a set of access rights that correspond to operations specific to that type of object.</span></span> <span data-ttu-id="faa68-105">Zusätzlich zu diesen Objekt spezifischen Zugriffsrechten gibt es einen Satz von Standard Zugriffsrechten, die den meisten Typen von Sicherungs fähigen Objekten gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="faa68-105">In addition to these object-specific access rights, there is a set of standard access rights that correspond to operations common to most types of securable objects.</span></span>

<span data-ttu-id="faa68-106">Das [Zugriffs Masken Format](access-mask-format.md) enthält einen Satz von Bits für die Standard Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="faa68-106">The [access mask format](access-mask-format.md) includes a set of bits for the standard access rights.</span></span> <span data-ttu-id="faa68-107">Die folgenden Windows-Konstanten für Standard Zugriffsrechte werden in "Winnt. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="faa68-107">The following Windows constants for standard access rights are defined in Winnt.h.</span></span>



| <span data-ttu-id="faa68-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="faa68-108">Constant</span></span>      | <span data-ttu-id="faa68-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="faa68-109">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa68-110">Delete</span><span class="sxs-lookup"><span data-stu-id="faa68-110">DELETE</span></span>        | <span data-ttu-id="faa68-111">Das Recht, das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="faa68-111">The right to delete the object.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="faa68-112">Lese \_ Steuerelement</span><span class="sxs-lookup"><span data-stu-id="faa68-112">READ\_CONTROL</span></span> | <span data-ttu-id="faa68-113">Das Recht, die Informationen in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)des Objekts zu lesen, ohne die Informationen in der [*System-Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="faa68-113">The right to read the information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), not including the information in the [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> |
| <span data-ttu-id="faa68-114">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="faa68-114">SYNCHRONIZE</span></span>   | <span data-ttu-id="faa68-115">Das Recht, das Objekt für die Synchronisierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="faa68-115">The right to use the object for synchronization.</span></span> <span data-ttu-id="faa68-116">Dadurch kann ein Thread warten, bis sich das Objekt im signalisierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="faa68-116">This enables a thread to wait until the object is in the signaled state.</span></span> <span data-ttu-id="faa68-117">Einige Objekttypen unterstützen dieses Zugriffsrecht nicht.</span><span class="sxs-lookup"><span data-stu-id="faa68-117">Some object types do not support this access right.</span></span>                                                                                                                                                                |
| <span data-ttu-id="faa68-118">\_DAC schreiben</span><span class="sxs-lookup"><span data-stu-id="faa68-118">WRITE\_DAC</span></span>    | <span data-ttu-id="faa68-119">Das Recht, die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) in der Sicherheits Beschreibung des Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="faa68-119">The right to modify the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) in the object's security descriptor.</span></span>                                                                                                                    |
| <span data-ttu-id="faa68-120">\_Besitzer schreiben</span><span class="sxs-lookup"><span data-stu-id="faa68-120">WRITE\_OWNER</span></span>  | <span data-ttu-id="faa68-121">Das Recht, in der Sicherheitsbeschreibung des Objekts den Besitzer zu ändern.</span><span class="sxs-lookup"><span data-stu-id="faa68-121">The right to change the owner in the object's security descriptor.</span></span>                                                                                                                                                                                                                                                                           |



 

<span data-ttu-id="faa68-122">"Winnt. h" definiert auch die folgenden Kombinationen der standardmäßigen Zugriffsrechte Konstanten.</span><span class="sxs-lookup"><span data-stu-id="faa68-122">Winnt.h also defines the following combinations of the standard access rights constants.</span></span>



| <span data-ttu-id="faa68-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="faa68-123">Constant</span></span>                   | <span data-ttu-id="faa68-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="faa68-124">Meaning</span></span>                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="faa68-125">\_alle Standard Rechte \_</span><span class="sxs-lookup"><span data-stu-id="faa68-125">STANDARD\_RIGHTS\_ALL</span></span>      | <span data-ttu-id="faa68-126">Kombiniert Lösch-, Lese- \_ und Schreib Steuerung, Schreiben von \_ DAC, Schreiben von \_ Besitzern und Synchronisieren des Zugriffs.</span><span class="sxs-lookup"><span data-stu-id="faa68-126">Combines DELETE, READ\_CONTROL, WRITE\_DAC, WRITE\_OWNER, and SYNCHRONIZE access.</span></span> |
| <span data-ttu-id="faa68-127">Standard \_ Rechte \_ Ausführen</span><span class="sxs-lookup"><span data-stu-id="faa68-127">STANDARD\_RIGHTS\_EXECUTE</span></span>  | <span data-ttu-id="faa68-128">Wird derzeit für das Read-Steuerelement definiert \_ .</span><span class="sxs-lookup"><span data-stu-id="faa68-128">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="faa68-129">Standard \_ Rechte \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="faa68-129">STANDARD\_RIGHTS\_READ</span></span>     | <span data-ttu-id="faa68-130">Wird derzeit für das Read-Steuerelement definiert \_ .</span><span class="sxs-lookup"><span data-stu-id="faa68-130">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="faa68-131">Standard \_ Rechte \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="faa68-131">STANDARD\_RIGHTS\_REQUIRED</span></span> | <span data-ttu-id="faa68-132">Kombiniert Lösch-, Lese- \_ \_ und Schreibzugriff, DAC und Schreib \_ Zugriff.</span><span class="sxs-lookup"><span data-stu-id="faa68-132">Combines DELETE, READ\_CONTROL, WRITE\_DAC, and WRITE\_OWNER access.</span></span>              |
| <span data-ttu-id="faa68-133">Standard \_ Rechte \_ Schreibvorgänge</span><span class="sxs-lookup"><span data-stu-id="faa68-133">STANDARD\_RIGHTS\_WRITE</span></span>    | <span data-ttu-id="faa68-134">Wird derzeit für das Read-Steuerelement definiert \_ .</span><span class="sxs-lookup"><span data-stu-id="faa68-134">Currently defined to equal READ\_CONTROL.</span></span>                                         |



 

 

 
