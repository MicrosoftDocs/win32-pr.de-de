---
description: SNMP-Textkonventionen werden CIM-definierten Typen zugeordnet.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Text Konvention-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343787"
---
# <a name="textual-convention-macro"></a><span data-ttu-id="57124-103">Text Konvention-Makro</span><span class="sxs-lookup"><span data-stu-id="57124-103">TEXTUAL-CONVENTION Macro</span></span>

<span data-ttu-id="57124-104">SNMP-Textkonventionen werden CIM-definierten Typen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="57124-104">SNMP textual conventions map to CIM-defined types.</span></span>

> [!Note]  
> <span data-ttu-id="57124-105">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="57124-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="57124-106">Die folgenden Zuordnungsregeln gelten für die SNMP-Textkonventionen:</span><span class="sxs-lookup"><span data-stu-id="57124-106">The following mapping rules apply to SNMP textual conventions:</span></span>

-   <span data-ttu-id="57124-107">Die benannte Typdefinition in der Syntax Klausel ordnet der CIM-Eigenschaften **qualifiziererobjektsyntax \_** wörtlich zu.</span><span class="sxs-lookup"><span data-stu-id="57124-107">The named type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax**.</span></span>
-   <span data-ttu-id="57124-108">Verwenden Sie die folgende Tabelle, um Textkonventionen zuzuordnen, wenn sich die Syntax Klausel explizit auf eine Text Konvention eines SNMPv2C-Text Konvention-Makros bezieht, oder auf eine implizite Text Konvention verweist.</span><span class="sxs-lookup"><span data-stu-id="57124-108">Use the following table to map textual conventions when the SYNTAX clause explicitly refers to a textual convention of a SNMPv2C TEXTUAL-CONVENTION macro, or refers to an implied textual convention.</span></span> <span data-ttu-id="57124-109">Der Standardwert ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="57124-109">The default value is always **NULL**.</span></span>



| <span data-ttu-id="57124-110">Text Konvention</span><span class="sxs-lookup"><span data-stu-id="57124-110">Textual convention</span></span> | <span data-ttu-id="57124-111">CIM-Variant-Typ</span><span class="sxs-lookup"><span data-stu-id="57124-111">CIM variant type</span></span> | <span data-ttu-id="57124-112">CIM Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="57124-112">CIM qualifier</span></span>                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57124-113">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="57124-113">DateAndTime</span></span>        | <span data-ttu-id="57124-114">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="57124-114">**VT\_BSTR**</span></span>     | <span data-ttu-id="57124-115">**Text \_ Konvention**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="57124-115">**textual\_convention**: DateAndTime</span></span><br/> <span data-ttu-id="57124-116">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="57124-116">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="57124-117">**Objekt \_ Syntax**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="57124-117">**object\_syntax**: DateAndTime</span></span><br/> <span data-ttu-id="57124-118">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57124-118">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="57124-119">Display String</span><span class="sxs-lookup"><span data-stu-id="57124-119">Displaystring</span></span>      | <span data-ttu-id="57124-120">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="57124-120">**VT\_BSTR**</span></span>     | <span data-ttu-id="57124-121">**Text \_ Konvention**: Display String</span><span class="sxs-lookup"><span data-stu-id="57124-121">**textual\_convention**: Displaystring</span></span><br/> <span data-ttu-id="57124-122">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="57124-122">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="57124-123">**Objekt \_ Syntax**: Display String</span><span class="sxs-lookup"><span data-stu-id="57124-123">**object\_syntax**: Displaystring</span></span><br/> <span data-ttu-id="57124-124">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57124-124">**cimtype**: string</span></span><br/>   |
| <span data-ttu-id="57124-125">MacAddress</span><span class="sxs-lookup"><span data-stu-id="57124-125">MacAddress</span></span>         | <span data-ttu-id="57124-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="57124-126">**VT\_BSTR**</span></span>     | <span data-ttu-id="57124-127">**Text \_ Konvention**: MACAddress</span><span class="sxs-lookup"><span data-stu-id="57124-127">**textual\_convention**: MacAddress</span></span><br/> <span data-ttu-id="57124-128">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="57124-128">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="57124-129">**Objekt \_ Syntax**: MACAddress</span><span class="sxs-lookup"><span data-stu-id="57124-129">**object\_syntax**: MacAddress</span></span><br/> <span data-ttu-id="57124-130">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57124-130">**cimtype**: string</span></span><br/>         |
| <span data-ttu-id="57124-131">Physaddress</span><span class="sxs-lookup"><span data-stu-id="57124-131">PhysAddress</span></span>        | <span data-ttu-id="57124-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="57124-132">**VT\_BSTR**</span></span>     | <span data-ttu-id="57124-133">**Text \_ Konvention**: physaddress</span><span class="sxs-lookup"><span data-stu-id="57124-133">**textual\_convention**: PhysAddress</span></span><br/> <span data-ttu-id="57124-134">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="57124-134">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="57124-135">**Objekt \_ Syntax**: physaddress</span><span class="sxs-lookup"><span data-stu-id="57124-135">**object\_syntax**: PhysAddress</span></span><br/> <span data-ttu-id="57124-136">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57124-136">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="57124-137">Snmpudpaddress</span><span class="sxs-lookup"><span data-stu-id="57124-137">SnmpUDPAddress</span></span>     | <span data-ttu-id="57124-138">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="57124-138">**VT\_BSTR**</span></span>     | <span data-ttu-id="57124-139">**Text \_ Konvention**: snmpudpaddress</span><span class="sxs-lookup"><span data-stu-id="57124-139">**textual\_convention**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="57124-140">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="57124-140">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="57124-141">**Objekt \_ Syntax**: snmpudpaddress</span><span class="sxs-lookup"><span data-stu-id="57124-141">**object\_syntax**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="57124-142">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57124-142">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="57124-143">Snmposiaddress</span><span class="sxs-lookup"><span data-stu-id="57124-143">SnmpOSIAddress</span></span>     | <span data-ttu-id="57124-144">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="57124-144">**VT\_BSTR**</span></span>     | <span data-ttu-id="57124-145">**Text \_ Konvention**: snmposiaddress</span><span class="sxs-lookup"><span data-stu-id="57124-145">**textual\_convention**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="57124-146">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="57124-146">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="57124-147">**Objekt \_ Syntax**: snmposiaddress</span><span class="sxs-lookup"><span data-stu-id="57124-147">**object\_syntax**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="57124-148">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57124-148">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="57124-149">Snmpipxaddress</span><span class="sxs-lookup"><span data-stu-id="57124-149">SnmpIPXAddress</span></span>     | <span data-ttu-id="57124-150">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="57124-150">**VT\_BSTR**</span></span>     | <span data-ttu-id="57124-151">**Text \_ Konvention**: snmpipxaddress</span><span class="sxs-lookup"><span data-stu-id="57124-151">**textual\_convention**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="57124-152">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="57124-152">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="57124-153">**Objekt \_ Syntax**: snmpipxaddress</span><span class="sxs-lookup"><span data-stu-id="57124-153">**object\_syntax**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="57124-154">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57124-154">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="57124-155">Der CIM-definierte Variant-Typ und die CIM-Eigenschafts Qualifizierer **Text \_ Konvention**, **Codierung**, **Objekt \_ Syntax** und **CimType** -Zuordnung unter Verwendung des zugrunde liegenden primitiven Typs.</span><span class="sxs-lookup"><span data-stu-id="57124-155">The CIM-defined variant type and the CIM property qualifiers **textual\_convention**, **encoding**, **object\_syntax**, and **cimtype** map using the underlying primitive type.</span></span>
-   <span data-ttu-id="57124-156">Die Display-Hint-Klausel des SNMPv2C-Text Konvention-Makros wird dem CIM-Eigenschaften qualifiziereranzeige- **\_ Hinweis** wörtlich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="57124-156">The DISPLAY-HINT clause of the SNMPv2C TEXTUAL-CONVENTION macro maps verbatim to the CIM property qualifier **display\_hint**.</span></span> <span data-ttu-id="57124-157">Dieser Qualifizierer wird nicht generiert, wenn kein Textkonventionen-Makro vorhanden ist oder das Makro keine Display-Hint-Klausel enthält.</span><span class="sxs-lookup"><span data-stu-id="57124-157">This qualifier is not generated if there is no TEXTUAL-CONVENTION macro, or the macro does not contain a DISPLAY-HINT clause.</span></span>

## <a name="example-code"></a><span data-ttu-id="57124-158">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="57124-158">Example Code</span></span>

<span data-ttu-id="57124-159">Im folgenden Beispiel wird eine SNMPv1-Text Konvention beschrieben.</span><span class="sxs-lookup"><span data-stu-id="57124-159">The following example describes an SNMPv1 textual convention.</span></span>

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

<span data-ttu-id="57124-160">Dieses Beispiel generiert die folgenden CIM-Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="57124-160">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

<span data-ttu-id="57124-161">Im folgenden Beispiel wird eine SNMPv2-Text Konvention beschrieben.</span><span class="sxs-lookup"><span data-stu-id="57124-161">The following example describes an SNMPv2 textual convention.</span></span>

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

<span data-ttu-id="57124-162">Dieses Beispiel generiert die folgenden CIM-Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="57124-162">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




