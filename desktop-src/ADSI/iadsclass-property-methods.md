---
title: Iadsclass-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsclass-Schnittstelle werden die folgenden Eigenschaften festgelegt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- Iadsclass-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105153"
---
# <a name="iadsclass-property-methods"></a><span data-ttu-id="4c663-105">Iadsclass-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="4c663-105">IADsClass Property Methods</span></span>

<span data-ttu-id="4c663-106">Mit den Eigenschafts Methoden der [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle werden die folgenden Eigenschaften festgelegt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4c663-106">The property methods of the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface get or set the following properties.</span></span> <span data-ttu-id="4c663-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4c663-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4c663-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4c663-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4c663-109">**Kter**</span><span class="sxs-lookup"><span data-stu-id="4c663-109">**Abstract**</span></span>
<span data-ttu-id="4c663-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-111">Boolescher Wert, der angibt, ob diese Klasse abstrakt oder nicht abstrakt ist.</span><span class="sxs-lookup"><span data-stu-id="4c663-111">Boolean value that indicates if this class is Abstract or non-abstract.</span></span> <span data-ttu-id="4c663-112">Wenn **true**, ist diese Klasse eine abstrakte Klasse und kann im Verzeichnisdienst nicht direkt instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="4c663-112">When **TRUE**, this class is an Abstract class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="4c663-113">Abstrakte Klassen können nur als Superklassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c663-113">Abstract classes can only be used as super classes.</span></span>

<dt>

<span data-ttu-id="4c663-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-115">Skript Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4c663-115">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-116">**"Auxderivedfrom"**</span><span class="sxs-lookup"><span data-stu-id="4c663-116">**AuxDerivedFrom**</span></span>
<span data-ttu-id="4c663-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-118">Array von ADsPath-Zeichen folgen, die die Super-Hilfssysteme angeben, von denen diese Klasse abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="4c663-118">Array of ADsPath strings that indicate the super Auxiliary classes this class derives from.</span></span>

<dt>

<span data-ttu-id="4c663-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-120">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c663-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-121">**Sten**</span><span class="sxs-lookup"><span data-stu-id="4c663-121">**Auxiliary**</span></span>
<span data-ttu-id="4c663-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-123">Boolescher Wert, der angibt, ob diese Klasse eine Hilfselemente ist.</span><span class="sxs-lookup"><span data-stu-id="4c663-123">Boolean value that indicates whether or not this class is Auxiliary.</span></span> <span data-ttu-id="4c663-124">Wenn **true**, ist diese Klasse eine Hilfsklasse und kann nicht direkt im Verzeichnisdienst instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="4c663-124">When **TRUE**, this class is an Auxiliary class and cannot be directly instantiated in the directory service.</span></span> <span data-ttu-id="4c663-125">Erweiterungs Klassen können nur als Superklassen anderer Erweiterungs Klassen oder als Quelle zusätzlicher Eigenschaften für Struktur Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c663-125">Auxiliary classes can only be used as super classes of other Auxiliary classes or as a source of additional properties on structural classes.</span></span>

<dt>

<span data-ttu-id="4c663-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-127">Skript Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4c663-127">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-128">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="4c663-128">**CLSID**</span></span>
<span data-ttu-id="4c663-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-130">Optionale anbieterspezifische CLSID, die das COM-Objekt identifiziert, das diese Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="4c663-130">Optional provider-specific CLSID identifying the COM object that implements this class.</span></span>

<dt>

<span data-ttu-id="4c663-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-132">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4c663-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-133">**Container**</span><span class="sxs-lookup"><span data-stu-id="4c663-133">**Container**</span></span>
<span data-ttu-id="4c663-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-135">Boolescher Wert, der angibt, ob diese Klasse ein Container anderer Objektklassen sein kann.</span><span class="sxs-lookup"><span data-stu-id="4c663-135">Boolean value that indicates if this class can be a container of other object classes.</span></span> <span data-ttu-id="4c663-136">Wenn dieser Wert **true** ist, können Sie die **get \_ Container** -Methode zum Abrufen eines Arrays von Objektklassen abrufen, die diese Klasse enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="4c663-136">If this value is **TRUE**, you can call the **get\_Container** method to get an array of the object classes that this class can contain.</span></span>

<dt>

<span data-ttu-id="4c663-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-138">Skript Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4c663-138">Scripting data type: **BOOLEAN**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-139">**Containment**</span><span class="sxs-lookup"><span data-stu-id="4c663-139">**Containment**</span></span>
<span data-ttu-id="4c663-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-141">Ein **BSTR** -Array, in dem jedes Element der Name einer Objektklasse ist, die diese Klasse enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="4c663-141">A **BSTR** array in which each element is the name of an object class that this class can contain.</span></span>

<dt>

<span data-ttu-id="4c663-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-143">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c663-143">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-144">**Derivedfrom**</span><span class="sxs-lookup"><span data-stu-id="4c663-144">**DerivedFrom**</span></span>
<span data-ttu-id="4c663-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-146">Array von ADsPath-Zeichen folgen, die angeben, von welchen Klassen diese Klasse abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="4c663-146">Array of ADsPath strings that indicate which classes this class was derived from.</span></span>

<dt>

<span data-ttu-id="4c663-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-148">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c663-148">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-149">**Helpfilecontext**</span><span class="sxs-lookup"><span data-stu-id="4c663-149">**HelpFileContext**</span></span>
<span data-ttu-id="4c663-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-151">Die Kontext-ID in **helpfilename** , in der spezifische Informationen für diese Klasse gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="4c663-151">Context ID inside **HelpFileName** where specific information for this class can be found.</span></span>

<dt>

<span data-ttu-id="4c663-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-153">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="4c663-153">Scripting data type: **long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-154">**Helpfilename**</span><span class="sxs-lookup"><span data-stu-id="4c663-154">**HelpFileName**</span></span>
<span data-ttu-id="4c663-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-156">Der Name einer Hilfedatei, die weitere Informationen zu Objekten dieser Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="4c663-156">Name of a help file that contains more information about objects of this class.</span></span>

<dt>

<span data-ttu-id="4c663-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-158">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4c663-158">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-159">**MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="4c663-159">**MandatoryProperties**</span></span>
<span data-ttu-id="4c663-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-161">**SAFEARRAY** von **Variant** s, die die Eigenschaften auflistet, die festgelegt werden müssen, damit diese Klasse in den Speicher geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="4c663-161">**SAFEARRAY** of **VARIANT** s that lists the properties that must be set for this class to be written to storage.</span></span> <span data-ttu-id="4c663-162">Wenn die Klasse nur eine Eigenschaft enthält, gibt **get \_ MandatoryProperties** einen **BSTR** zurück.</span><span class="sxs-lookup"><span data-stu-id="4c663-162">If the class only contains one property, then **get\_MandatoryProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="4c663-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-164">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c663-164">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-165">**Namingproperties**</span><span class="sxs-lookup"><span data-stu-id="4c663-165">**NamingProperties**</span></span>
<span data-ttu-id="4c663-166"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-166"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-167">**SAFEARRAY** von **BSTR** s, das die Eigenschaften auflistet, die zum Benennen von Attributen dieser Schema Klasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c663-167">**SAFEARRAY** of **BSTR** s that lists the properties used to name attributes of this schema class.</span></span>

<dt>

<span data-ttu-id="4c663-168">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-169">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c663-169">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-170">**OID**</span><span class="sxs-lookup"><span data-stu-id="4c663-170">**OID**</span></span>
<span data-ttu-id="4c663-171"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-171"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-172">Anbieter spezifischer Objekt Bezeichner, der diese Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="4c663-172">Provider-specific Object Identifier that defines this class.</span></span> <span data-ttu-id="4c663-173">Dies wird bereitgestellt, um die Schema Erweiterung mithilfe von Active Directory in Verzeichnisdiensten zuzulassen, die anbieterspezifische OIDs für Klassen erfordern.</span><span class="sxs-lookup"><span data-stu-id="4c663-173">This is provided to allow schema extension, using Active Directory, in directory services that require provider-specific OIDs for classes.</span></span>

<dt>

<span data-ttu-id="4c663-174">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-175">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4c663-175">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-176">**OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="4c663-176">**OptionalProperties**</span></span>
<span data-ttu-id="4c663-177"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-177"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-178">**SAFEARRAY** von **Variant** s, die die optionalen Eigenschaften für diese Schema Klasse auflistet.</span><span class="sxs-lookup"><span data-stu-id="4c663-178">**SAFEARRAY** of **VARIANT** s that lists the optional properties for this schema class.</span></span> <span data-ttu-id="4c663-179">Wenn die Klasse nur eine Eigenschaft enthält, gibt **get \_ OptionalProperties** einen **BSTR** zurück.</span><span class="sxs-lookup"><span data-stu-id="4c663-179">If the class only contains one property, then **get\_OptionalProperties** will return a **BSTR**.</span></span>

<dt>

<span data-ttu-id="4c663-180">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-181">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c663-181">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-182">**Possiblevorgesetzten**</span><span class="sxs-lookup"><span data-stu-id="4c663-182">**PossibleSuperiors**</span></span>
<span data-ttu-id="4c663-183"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-183"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-184">Array von ADsPath-Zeichen folgen, die die Schema Klassen angeben, die Instanzen dieser Klasse enthalten können.</span><span class="sxs-lookup"><span data-stu-id="4c663-184">Array of ADsPath strings that indicate the schema classes that can contain instances of this class.</span></span>

<dt>

<span data-ttu-id="4c663-185">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4c663-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c663-186">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4c663-186">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c663-187">**Primaryinterface**</span><span class="sxs-lookup"><span data-stu-id="4c663-187">**PrimaryInterface**</span></span>
<span data-ttu-id="4c663-188"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4c663-188"></dt> <dd> <dl></span></span>

<span data-ttu-id="4c663-189">Optionaler Anbieter spezifischer Bezeichner-GUID, der Objekten dieser Schema Klasse eine Schnittstelle zuordnet.</span><span class="sxs-lookup"><span data-stu-id="4c663-189">Optional provider-specific identifier GUID that associates an interface to objects of this schema class.</span></span> <span data-ttu-id="4c663-190">Beispielsweise wird die "User"-Klasse, die [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) und **primaryinterface** unterstützt, durch **IID \_ IADsUser** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4c663-190">For example, the "User" class that supports [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) and **PrimaryInterface** is identified by **IID\_IADsUser**.</span></span> <span data-ttu-id="4c663-191">Dies muss das Standard Zeichen folgen Format einer GUID aufweisen, wie durch com definiert.</span><span class="sxs-lookup"><span data-stu-id="4c663-191">This must be in the standard string format of a GUID, as defined by COM.</span></span> <span data-ttu-id="4c663-192">Diese GUID ist der Wert, der in der [**IADs:: get- \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) -Eigenschaft in Instanzen dieser Klasse für Anbieter angezeigt wird, die diese Eigenschaft implementieren.</span><span class="sxs-lookup"><span data-stu-id="4c663-192">This GUID is the value that appears in the [**IADs::get\_GUID**](/windows/desktop/api/Iads/nn-iads-iads) property in instances of this class for providers that implement this property.</span></span> <span data-ttu-id="4c663-193">Durch die Identifizierung einer Schema Klasse durch die IID der primären Schnittstelle des Klassen Codes kann die Verwendung von **QueryInterface** zur Laufzeit bestimmt werden, ob ein Objekt der gewünschten Klasse entspricht.</span><span class="sxs-lookup"><span data-stu-id="4c663-193">Identifying a schema class by IID of the class code's primary interface enables the use of **QueryInterface** at run time to determine whether an object is of the desired class.</span></span>

<dt>

<span data-ttu-id="4c663-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4c663-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c663-195">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4c663-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="4c663-196">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c663-196">Examples</span></span>

<span data-ttu-id="4c663-197">Im folgenden Codebeispiel wird gezeigt, wie die [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle verwendet wird, um zu bestimmen, ob ein Objekt ein Container sein kann. wenn dies der Fall ist, werden die Namen aller enthaltenen Objekte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4c663-197">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



<span data-ttu-id="4c663-198">Im folgenden Codebeispiel wird gezeigt, wie die [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstelle verwendet wird, um zu bestimmen, ob ein Objekt ein Container sein kann. wenn dies der Fall ist, werden die Namen aller enthaltenen Objekte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4c663-198">The following code example shows how to use the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface to determine if an object can be a container and, if so, lists the names of any contained objects.</span></span>


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="4c663-199">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c663-199">Requirements</span></span>



| <span data-ttu-id="4c663-200">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c663-200">Requirement</span></span> | <span data-ttu-id="4c663-201">Wert</span><span class="sxs-lookup"><span data-stu-id="4c663-201">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c663-202">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c663-202">Minimum supported client</span></span><br/> | <span data-ttu-id="4c663-203">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c663-203">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c663-204">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c663-204">Minimum supported server</span></span><br/> | <span data-ttu-id="4c663-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c663-205">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c663-206">Header</span><span class="sxs-lookup"><span data-stu-id="4c663-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c663-207"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c663-207"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4c663-208">DLL</span><span class="sxs-lookup"><span data-stu-id="4c663-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c663-209"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c663-209"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c663-210">IID</span><span class="sxs-lookup"><span data-stu-id="4c663-210">IID</span></span><br/>                      | <span data-ttu-id="4c663-211">IID \_ iadsclass ist als C8F93DD0-4AE0-11CF-9E73-00AA004A5691 definiert.</span><span class="sxs-lookup"><span data-stu-id="4c663-211">IID\_IADsClass is defined as C8F93DD0-4AE0-11CF-9E73-00AA004A5691</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4c663-212">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c663-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c663-213">**Iadsclass**</span><span class="sxs-lookup"><span data-stu-id="4c663-213">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="4c663-214">**Iadsclass:: Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="4c663-214">**IADsClass::Qualifiers**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





