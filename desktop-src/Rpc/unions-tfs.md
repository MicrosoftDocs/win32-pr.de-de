---
title: RPC-Unions
description: Gekapselte und nicht gekapselte Unions und deren Format mit Remote Prozedur Aufruf (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473164"
---
# <a name="rpc-unions"></a><span data-ttu-id="4b6a8-103">RPC-Unions</span><span class="sxs-lookup"><span data-stu-id="4b6a8-103">RPC unions</span></span>

<span data-ttu-id="4b6a8-104">Sowohl gekapselte als auch nicht gekapselte Unions haben eine gemeinsame Union- \_ Arm- \_<> Auswahl</span><span class="sxs-lookup"><span data-stu-id="4b6a8-104">Both encapsulated and nonencapsulated unions share a common union\_arm\_selector<> format:</span></span>

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

<span data-ttu-id="4b6a8-105">Das \_ Feld Union Arms<2> besteht aus zwei Teilen.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-105">The union\_arms<2> field consists of two parts.</span></span> <span data-ttu-id="4b6a8-106">Wenn die Union eine Union im 1,0-Stil ist, enthalten die oberen 4 Bits die Ausrichtung des Union-Arm (Ausrichtung des größten ausgerichteten Arm).</span><span class="sxs-lookup"><span data-stu-id="4b6a8-106">If the union is a MIDL 1.0 style union, the upper 4 bits contain the alignment of the union arm (alignment of greatest aligned arm).</span></span> <span data-ttu-id="4b6a8-107">Andernfalls sind die oberen 4 Bits 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4b6a8-107">Otherwise the upper 4 bits are zero.</span></span> <span data-ttu-id="4b6a8-108">Die unteren 12 Bits enthalten die Anzahl der Waffen in der Union.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-108">The lower 12 bits contain the number of arms in the union.</span></span> <span data-ttu-id="4b6a8-109">Anders gesagt:</span><span class="sxs-lookup"><span data-stu-id="4b6a8-109">In other words:</span></span>

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

<span data-ttu-id="4b6a8-110">Die Beschreibung des Offset- \_ zu- \_ Arm \_ -<2> Felder enthalten einen relativen Offset mit Vorzeichen zur Typbeschreibung des Arm-Typs.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-110">The offset\_to\_arm\_description<2> fields contain a relative signed offset to the arm's type description.</span></span> <span data-ttu-id="4b6a8-111">Allerdings wird das Feld mit Optimierung für einfache Typen überladen.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-111">However, the field is overloaded with optimization for simple types.</span></span> <span data-ttu-id="4b6a8-112">Hierfür ist das obere Byte dieses Offset Felds FC \_ Magic \_ Union \_ Byte (0x80) und das untere Byte der Kurzform der tatsächliche Format Zeichentyp des Arm.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-112">For these, the upper byte of this offset field is FC\_MAGIC\_UNION\_BYTE (0x80) and the lower byte of the short is the actual format character type of the arm.</span></span> <span data-ttu-id="4b6a8-113">Daher gibt es zwei Bereiche für die Offset Werte: "80 *xx*" bedeutet, dass *xx* eine typformatzeichenfolge ist. und alles andere innerhalb des Bereichs (80 ff.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-113">As such, there are two ranges for the offset values: "80 *xx*" means that *xx* is a type format string; and everything else within range (80 FF ..</span></span> <span data-ttu-id="4b6a8-114">7F) bedeutet einen tatsächlichen Offset.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-114">7f FF) means an actual offset.</span></span> <span data-ttu-id="4b6a8-115">Dadurch werden Offsets aus dem Bereich <80 00.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-115">This makes offsets from range <80 00 ..</span></span> <span data-ttu-id="4b6a8-116">80 FF > nicht als Offsets verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-116">80 FF > unavailable as offsets.</span></span> <span data-ttu-id="4b6a8-117">Der Compiler überprüft dies ab der 5.1.164 der mittleren Version.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-117">The compiler checks that as of MIDL version 5.1.164.</span></span>

<span data-ttu-id="4b6a8-118">Die Standard- \_ Arm- \_ Beschreibung<2> Feld gibt den Typ des Union-Arm-Werts für den Standardarm an (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="4b6a8-118">The default\_arm\_description<2> field indicates the type of union arm for the default arm, if any.</span></span> <span data-ttu-id="4b6a8-119">Wenn kein Standardarm für die Union angegeben ist, wird die \_ Standardarm- \_ Beschreibung<2> Feld 0xFFFF verwendet, und es wird eine Ausnahme ausgelöst, wenn der Schalter Wert keinen der \_ Arm-Case-Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-119">If there is no default arm specified for the union then the default\_arm\_description<2> field is 0xFFFF and an exception is raised if the switch\_is value does not match any of the arm case values.</span></span> <span data-ttu-id="4b6a8-120">Wenn die Standardarm angegeben, aber leer ist, ist die standardmäßige \_ Arm- \_ Beschreibung<2> Feld NULL.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-120">If the default arm is specified but empty, then the default\_arm\_description<2> field is zero.</span></span> <span data-ttu-id="4b6a8-121">Andernfalls weist die \_ \_ standardbeschreibungs-<2> Feld die gleiche Semantik wie die Offset- \_ zu- \_ Arm- \_ Beschreibung<2> Felder auf.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-121">Otherwise the default\_arm\_description<2> field has the same semantics as the offset\_to\_arm\_description<2> fields.</span></span>

<span data-ttu-id="4b6a8-122">Im folgenden finden Sie eine Zusammenfassung:</span><span class="sxs-lookup"><span data-stu-id="4b6a8-122">The following is a summary:</span></span>

-   <span data-ttu-id="4b6a8-123">0-leerer Standardwert</span><span class="sxs-lookup"><span data-stu-id="4b6a8-123">0 - empty default</span></span>
-   <span data-ttu-id="4b6a8-124">FFFF-kein Standardwert</span><span class="sxs-lookup"><span data-stu-id="4b6a8-124">FFFF - no default</span></span>
-   <span data-ttu-id="4b6a8-125">80xx-einfacher Typ</span><span class="sxs-lookup"><span data-stu-id="4b6a8-125">80xx - simple type</span></span>
-   <span data-ttu-id="4b6a8-126">anderer relativer Offset</span><span class="sxs-lookup"><span data-stu-id="4b6a8-126">other - relative offset</span></span>

## <a name="encapsulated-unions"></a><span data-ttu-id="4b6a8-127">Gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="4b6a8-127">Encapsulated Unions</span></span>

<span data-ttu-id="4b6a8-128">Eine gekapselte Union stammt aus einer speziellen Union-Syntax in IDL.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-128">An encapsulated union comes from a special union syntax in IDL.</span></span> <span data-ttu-id="4b6a8-129">Effektiv ist eine gekapselte Union eine Bündel Struktur mit einem Diskriminanten Feld am Anfang der Struktur und der Union als einziges anderes Element.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-129">Effectively, an encapsulated union is a bundle structure with a discriminant field at the beginning of the structure and the union as the only other member.</span></span>

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

<span data-ttu-id="4b6a8-130">Der Switch-Typ einer gekapselten Union \_<1> Feld hat zwei Teile.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-130">An encapsulated union's switch\_type<1> field has two parts.</span></span> <span data-ttu-id="4b6a8-131">Der untere Halbbyte bietet den eigentlichen Switchtyp, und der obere Halbbyte bietet das Arbeitsspeicher Inkrement für den Schritt, bei dem der Speicher Zeiger erhöht werden muss, um den Switch \_ is-Feld zu überspringen, der alle Auffüll Zeichen zwischen dem Switch \_ is ()-Feld der Stub-Struktur und dem eigentlichen Union-Feld einschließt.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-131">The lower nibble provides the actual switch type, and the upper nibble provides the memory increment to step over that is an amount that the memory pointer must be incremented to skip past the switch\_is field, which includes any padding between the switch\_is() field of the stub-constructed structure and the actual union field.</span></span>

<span data-ttu-id="4b6a8-132">Die Arbeitsspeicher \_ Größe<2> Feld entspricht nur der Größe der Union und ist mit nicht gekapselten Unions identisch.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-132">The memory\_size<2> field is the size of the union only, and is identical to nonencapsulated unions.</span></span> <span data-ttu-id="4b6a8-133">Wenn Sie die Gesamtgröße der Struktur abrufen möchten, die die Union enthält, fügen Sie die Arbeitsspeicher \_ Größe<2> zu Arbeitsspeicher Inkrement hinzu, um einen Prozedur Schritt auszuführen, d. h. den oberen Halbbyte des \_ Switchtyps<1> Feld, und richten Sie dann die Ausrichtung an, die dem Inkrement entspricht.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-133">To obtain the total size of the structure that contains the union, add memory\_size<2> to memory increment to step over, that is to the upper nibble of the switch\_type<1> field, then align by the alignment corresponding to the increment.</span></span>

## <a name="nonencapsulated-unions"></a><span data-ttu-id="4b6a8-134">Nicht gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="4b6a8-134">Nonencapsulated Unions</span></span>

<span data-ttu-id="4b6a8-135">Eine nicht gekapselte Union ist eine typische Situation, in der eine Union ein Argument oder ein Feld ist und der Switch ein anderes Argument bzw. Feld ist.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-135">A nonencapsulated union is a typical situation where a union is one argument or field and the switch is another argument or field, respectively.</span></span>

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

<span data-ttu-id="4b6a8-136">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="4b6a8-136">Where:</span></span>

<span data-ttu-id="4b6a8-137">Der \_ Switchtyp<1> Feld ist ein Formatzeichen für den Diskriminanten.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-137">The switch\_type<1> field is a format character for the discriminant.</span></span>

<span data-ttu-id="4b6a8-138">Der Schalter \_ ist \_ ein Deskriptor,<> Feld ein Korrelations Deskriptor ist und abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="4b6a8-138">The switch\_is\_descriptor<> field is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="4b6a8-139">Für den Schalter ist jedoch \_ \_ Description<> wenn die Union in eine Struktur eingebettet ist, ist das Offset-Feld des Schalters \_ \_ Description<> der Offset zum Switch \_ ist das Feld von der Union-Position in der Struktur (nicht vom Anfang der Struktur).</span><span class="sxs-lookup"><span data-stu-id="4b6a8-139">However, for the switch\_is\_description<>, if the union is embedded in a structure, the offset field of the switch\_is\_description<> is the offset to the switch\_is field from the union's position in the structure (not from the beginning of the structure).</span></span>

<span data-ttu-id="4b6a8-140">Der Offset \_ - \_ zu \_ -Größe-und der \_ Arm \_ -Beschreibungs-<2> Feld gibt den Offset der Union-Größe und der Arm-Beschreibung an, die für gekapselte Unions identisch ist und von allen nicht gekapselten Unions desselben Typs gemeinsam genutzt wird:</span><span class="sxs-lookup"><span data-stu-id="4b6a8-140">The offset\_to\_size\_and\_arm\_description<2> field gives the offset to the union's size and arm description, which is identical to that for encapsulated unions and is shared by all nonencapsulated unions of the same type :</span></span>

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 