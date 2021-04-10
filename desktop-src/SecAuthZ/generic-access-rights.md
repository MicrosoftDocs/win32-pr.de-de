---
description: Sicherungs fähige Objekte verwenden ein Zugriffs Masken Format, in dem die vier allgemeinen Bits allgemeine Zugriffsrechte angeben.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Generische Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758250"
---
# <a name="generic-access-rights"></a><span data-ttu-id="c80aa-103">Generische Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="c80aa-103">Generic Access Rights</span></span>

<span data-ttu-id="c80aa-104">Sicherungs fähige Objekte verwenden ein [Zugriffs Masken Format](access-mask-format.md) , in dem die vier allgemeinen Bits allgemeine Zugriffsrechte angeben.</span><span class="sxs-lookup"><span data-stu-id="c80aa-104">Securable objects use an [access mask format](access-mask-format.md) in which the four high-order bits specify generic access rights.</span></span> <span data-ttu-id="c80aa-105">Jeder Typ von Sicherungs fähigen Objekten ordnet diese Bits einem Satz von Standard-und Objekt spezifischen Zugriffsrechten zu.</span><span class="sxs-lookup"><span data-stu-id="c80aa-105">Each type of securable object maps these bits to a set of its standard and object-specific access rights.</span></span> <span data-ttu-id="c80aa-106">Ein Windows-Datei Objekt ordnet z. b. das generische \_ Lesebit dem Lese Steuerelement zu \_ und synchronisiert Standard Zugriffsrechte und die Datei \_ \_ Daten lesen, Datei \_ Lese \_ -EA und Datei \_ Lese \_ Attribute objektspezifische Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="c80aa-106">For example, a Windows file object maps the GENERIC\_READ bit to the READ\_CONTROL and SYNCHRONIZE standard access rights and to the FILE\_READ\_DATA, FILE\_READ\_EA, and FILE\_READ\_ATTRIBUTES object-specific access rights.</span></span> <span data-ttu-id="c80aa-107">Andere Objekttypen ordnen das generische \_ Lesebit jedem beliebigen Satz von Zugriffsrechten zu, der für diesen Objekttyp geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c80aa-107">Other types of objects map the GENERIC\_READ bit to whatever set of access rights is appropriate for that type of object.</span></span>

<span data-ttu-id="c80aa-108">Sie können generische Zugriffsrechte verwenden, um den Typ des Zugriffs anzugeben, den Sie benötigen, wenn Sie ein Handle für ein Objekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="c80aa-108">You can use generic access rights to specify the type of access you need when you are opening a handle to an object.</span></span> <span data-ttu-id="c80aa-109">Dies ist in der Regel einfacher, als alle entsprechenden Standard-und spezifischen Rechte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c80aa-109">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span>

<span data-ttu-id="c80aa-110">In der folgenden Tabelle sind die für die generischen Zugriffsrechte definierten Konstanten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c80aa-110">The following table shows the constants defined for the generic access rights.</span></span>



| <span data-ttu-id="c80aa-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="c80aa-111">Constant</span></span>         | <span data-ttu-id="c80aa-112">Generische Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c80aa-112">Generic meaning</span></span>            |
|------------------|----------------------------|
| <span data-ttu-id="c80aa-113">generisch \_ alle</span><span class="sxs-lookup"><span data-stu-id="c80aa-113">GENERIC\_ALL</span></span>     | <span data-ttu-id="c80aa-114">Alle möglichen Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="c80aa-114">All possible access rights</span></span> |
| <span data-ttu-id="c80aa-115">generisch \_ Ausführen</span><span class="sxs-lookup"><span data-stu-id="c80aa-115">GENERIC\_EXECUTE</span></span> | <span data-ttu-id="c80aa-116">Zugriff ausführen</span><span class="sxs-lookup"><span data-stu-id="c80aa-116">Execute access</span></span>             |
| <span data-ttu-id="c80aa-117">generischer \_ Lesevorgang</span><span class="sxs-lookup"><span data-stu-id="c80aa-117">GENERIC\_READ</span></span>    | <span data-ttu-id="c80aa-118">Lesezugriff</span><span class="sxs-lookup"><span data-stu-id="c80aa-118">Read access</span></span>                |
| <span data-ttu-id="c80aa-119">generischer \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="c80aa-119">GENERIC\_WRITE</span></span>   | <span data-ttu-id="c80aa-120">Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="c80aa-120">Write access</span></span>               |



 

<span data-ttu-id="c80aa-121">Anwendungen, die private Sicherungs fähige Objekte definieren, können auch die generischen Zugriffsrechte verwenden.</span><span class="sxs-lookup"><span data-stu-id="c80aa-121">Applications that define private securable objects can also use the generic access rights.</span></span>

 

 



