---
description: Meta-Qualifizierer verfeinern die Definition von Meta-Konstrukten im CIM-Modell, indem Sie die tatsächliche Verwendung einer Klassen-oder Eigenschafts Deklaration innerhalb der MOF-Syntax verdeutlichen.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Metaqualifizierer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364056"
---
# <a name="meta-qualifiers"></a><span data-ttu-id="86c80-103">Metaqualifizierer</span><span class="sxs-lookup"><span data-stu-id="86c80-103">Meta Qualifiers</span></span>

<span data-ttu-id="86c80-104">Meta-Qualifizierer verfeinern die Definition von Meta-Konstrukten im CIM-Modell, indem Sie die tatsächliche Verwendung einer Klassen-oder Eigenschafts Deklaration innerhalb der MOF-Syntax verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="86c80-104">Meta qualifiers refine the definition of meta-constructs in the CIM model by clarifying the actual usage of a class or property declaration within the MOF syntax.</span></span>

<dt>

<span data-ttu-id="86c80-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Anwalt**</span><span class="sxs-lookup"><span data-stu-id="86c80-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span></span>
</dt> <dd>

<span data-ttu-id="86c80-106">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="86c80-106">Data type: **boolean**</span></span>

<span data-ttu-id="86c80-107">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="86c80-107">Applies to: classes</span></span>

<span data-ttu-id="86c80-108">Gibt an, ob die Klasse eine Zuordnungs Klasse ist, mit der eine Beziehung zwischen zwei anderen Klassen beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="86c80-108">Indicates whether the class is an association class used to describe a relationship between two other classes.</span></span> <span data-ttu-id="86c80-109">Das Fehlen dieses Qualifizierers gibt an, dass die Klasse keine Association-Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="86c80-109">The absence of this qualifier indicates that the class is not an association class.</span></span> <span data-ttu-id="86c80-110">Diese Qualifizierer schließen sich gegenseitig **aus.**</span><span class="sxs-lookup"><span data-stu-id="86c80-110">This qualifier is mutually exclusive with **Indication**.</span></span> <span data-ttu-id="86c80-111">Weitere Informationen finden Sie unter [Deklarieren einer Association-Klasse](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="86c80-111">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="86c80-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Aufschluss**</span><span class="sxs-lookup"><span data-stu-id="86c80-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span></span>
</dt> <dd>

<span data-ttu-id="86c80-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="86c80-113">Data type: **boolean**</span></span>

<span data-ttu-id="86c80-114">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="86c80-114">Applies to: classes</span></span>

<span data-ttu-id="86c80-115">Gibt an, ob die Objektklasse eine Angabe definiert.</span><span class="sxs-lookup"><span data-stu-id="86c80-115">Indicates whether the object class defines an indication.</span></span> <span data-ttu-id="86c80-116">Dieser Qualifizierer schließt sich gegenseitig mit **Association** aus.</span><span class="sxs-lookup"><span data-stu-id="86c80-116">This qualifier is mutually exclusive with **Association**.</span></span> <span data-ttu-id="86c80-117">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="86c80-117">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86c80-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86c80-118">Requirements</span></span>



| <span data-ttu-id="86c80-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86c80-119">Requirement</span></span> | <span data-ttu-id="86c80-120">Wert</span><span class="sxs-lookup"><span data-stu-id="86c80-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="86c80-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86c80-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86c80-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86c80-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="86c80-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86c80-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86c80-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86c80-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86c80-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86c80-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c80-126">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="86c80-126">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="86c80-127">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="86c80-127">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




