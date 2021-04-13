---
title: Enumerationskonstanten (WSManDisp. h)
description: Die Enumeration enthält Konstanten, wie in der folgenden Liste aufgelistet, die im flags-Parameter durch Aufrufe von Session. Enumerate und iwsmansession Enumerate verwendet werden.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391716"
---
# <a name="enumeration-constants"></a><span data-ttu-id="80229-103">Enumerationskonstanten</span><span class="sxs-lookup"><span data-stu-id="80229-103">Enumeration Constants</span></span>

<span data-ttu-id="80229-104">Die **\_ \_ wsmanenumflags** -Enumeration enthält Konstanten, wie in der folgenden Liste aufgelistet, die im *Flags* -Parameter durch Aufrufe von [**Session. Enumerate**](session-enumerate.md) und [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80229-104">The **\_\_WSManEnumFlags** enumeration contains constants, as listed in the following list, used in the *flags* parameter by calls to [**Session.Enumerate**](session-enumerate.md) and [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

<span data-ttu-id="80229-105">Beachten Sie, dass **wsmanflagreturnobject** und **wsmanflaghierarchydeep** der Standardwert sind, wenn der *Flags* -Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="80229-105">Be aware that **WSManFlagReturnObject** and **WSManFlagHierarchyDeep** are the default if the *flags* parameter is not specified.</span></span>

<dl> <dt>

<span data-ttu-id="80229-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**Wsmanflagreturnobject**</span><span class="sxs-lookup"><span data-stu-id="80229-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80229-107">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="80229-107">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="80229-108">Batches enthalten die angeforderten XML-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="80229-108">Batches contain the requested XML instances.</span></span> <span data-ttu-id="80229-109">Dies ist der Standardwert für den Flag-Parameter.</span><span class="sxs-lookup"><span data-stu-id="80229-109">This is the default value for the flag parameter.</span></span>

<span data-ttu-id="80229-110">Die zugeordnete Skript Methode lautet " [**WSMAN. enumerationflagreturnobject**](wsman-enumerationflagreturnobject.md) ", und die C++-Methode ist " [**iwsmanex. enumerationflagreturnobject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)".</span><span class="sxs-lookup"><span data-stu-id="80229-110">The associated scripting method is [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80229-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**Wsmanflagnonxmltext**</span><span class="sxs-lookup"><span data-stu-id="80229-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80229-112">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="80229-112">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="80229-113">Dieses Flag steuert, wie der *Filter* -Parameter im Aufrufen von [**Session. Enumerate**](session-enumerate.md) von WinRM interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="80229-113">This flag controls how the *filter* parameter in the call to [**Session.Enumerate**](session-enumerate.md) is interpreted by WinRM.</span></span>

<span data-ttu-id="80229-114">Das Format des Filters kann ein XML-Fragment oder eine Text Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="80229-114">The format of the filter may be an XML fragment or a string of plain text.</span></span> <span data-ttu-id="80229-115">Das Format wird durch den [*Filter Dialekt*](windows-remote-management-glossary.md) des [*Filters*](windows-remote-management-glossary.md) bestimmt, der im Aufrufen von [**Session. Enumerate**](session-enumerate.md) oder [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet wird, der spezifisch für den ausgeführten Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="80229-115">The format is determined by the [*filter dialect*](windows-remote-management-glossary.md) of the [*filter*](windows-remote-management-glossary.md) used in the call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), which is specific to the operation performed.</span></span>

<span data-ttu-id="80229-116">Wenn der *Dialekt* Parameter nicht angegeben wird, versucht WinRM, den Dialekt basierend auf dem ersten Zeichen des Filters zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="80229-116">If the *dialect* parameter is not specified, WinRM attempts to determine the dialect based on the first character of the filter.</span></span> <span data-ttu-id="80229-117">Wenn das erste Zeichen < ist, der Filter jedoch nicht tatsächlich ein XML-Fragment ist, sollte dieses Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="80229-117">If the first character is <, but the filter is not actually an XML fragment, then this flag should be set.</span></span> <span data-ttu-id="80229-118">Ein Filter im folgenden Format erfordert beispielsweise, dass Sie **wsmanflagnonxmltext** festlegen, damit der Filter ordnungsgemäß interpretiert wird:</span><span class="sxs-lookup"><span data-stu-id="80229-118">For example, a filter in the following format requires that you set **WSManFlagNonXmlText** so that the filter is correctly interpreted:</span></span>

`<25 && > 1`

<span data-ttu-id="80229-119">Wenn der Filter ein XML-Fragment ist, ist dieses Flag nicht erforderlich, da das Fragment mit < beginnt, das WinRM ordnungsgemäß als XML interpretiert.</span><span class="sxs-lookup"><span data-stu-id="80229-119">If the filter is an XML fragment, then this flag is not required because the fragment starts with <, which WinRM correctly interprets as XML.</span></span> <span data-ttu-id="80229-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="80229-120">For example,</span></span>

`<filter>select * from aDataStructure</filter>`

<span data-ttu-id="80229-121">Wenn sich der Filter im nur-Text-Modus befindet, der nicht mit < beginnt, ist dieses Flag nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="80229-121">If the filter is in plain text that does not start with <, then this flag is not required.</span></span> <span data-ttu-id="80229-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="80229-122">For example,</span></span>

`select * from aDataStructure`

<span data-ttu-id="80229-123">Die zugeordnete Skript Methode ist [**WSMAN. enumerationflagnonxmltext**](wsman-enumerationflagnonxmltext.md) , und die C++-Methode ist [**iwsmanex. enumerationflagnonxmltext**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span><span class="sxs-lookup"><span data-stu-id="80229-123">The associated scripting method is [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) and the C++ method is [**IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80229-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**Enumerationflagreturnetpr**</span><span class="sxs-lookup"><span data-stu-id="80229-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80229-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="80229-125">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="80229-126">Batches enthalten Endpunkt Verweise (EPRS) für die entsprechenden XML-Instanzen, jedoch nicht die eigentlichen Instanzen.</span><span class="sxs-lookup"><span data-stu-id="80229-126">Batches contain endpoint references (EPRs) for the corresponding XML instances, but not the actual instances.</span></span>

<span data-ttu-id="80229-127">Die zugeordnete Skript Methode ist [**WSMAN. enumerationflagreturnetpr**](wsman-enumerationflagreturnepr.md) , und die C++-Methode ist [**iwsmanex. enumerationflagreturnetpr**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span><span class="sxs-lookup"><span data-stu-id="80229-127">The associated scripting method is [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80229-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**Wsmanflagreturnobjectandepr**</span><span class="sxs-lookup"><span data-stu-id="80229-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80229-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="80229-129">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="80229-130">Batches enthalten sowohl die angeforderte XML-Instanz als auch die entsprechenden EPRS, die in einem [*WSMAN: Items*](windows-remote-management-glossary.md) -Element enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="80229-130">Batches contain both the requested XML instances and the corresponding EPRs contained in a [*wsman:Items*](windows-remote-management-glossary.md) element.</span></span>

<span data-ttu-id="80229-131">Die zugeordnete Skript Methode lautet " [**WSMAN. enumerationflagreturnobjectandepr**](wsman-enumerationflagreturnobjectandepr.md) ", und die C++-Methode ist " [**iwsmanex. enumerationflagreturnobjectandepr**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)".</span><span class="sxs-lookup"><span data-stu-id="80229-131">The associated scripting method is [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80229-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**Wsmanflaghierarchydeep**</span><span class="sxs-lookup"><span data-stu-id="80229-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80229-133">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="80229-133">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="80229-134">Abgeleitete Klassen Instanzen werden eingeschlossen und entsprechend ihren eigentlichen Schemas dargestellt.</span><span class="sxs-lookup"><span data-stu-id="80229-134">Derived class instances are included and are represented according to their actual schemas.</span></span>

<span data-ttu-id="80229-135">Die zugeordnete Skript Methode lautet [**WSMAN. enumerationflaghierarchydeep**](wsman-enumerationflaghierarchydeep.md) und die C++-Methode ist [**iwsmanex. enumerationflaghierarchydeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span><span class="sxs-lookup"><span data-stu-id="80229-135">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80229-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**Wsmanflaghierarchyflache**</span><span class="sxs-lookup"><span data-stu-id="80229-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80229-137">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="80229-137">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="80229-138">Abgeleitete Klassen Instanzen werden ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="80229-138">Derived class instances are excluded.</span></span> <span data-ttu-id="80229-139">Es werden nur Instanzen des angeforderten Typs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80229-139">Only instances of the requested type are shown.</span></span>

<span data-ttu-id="80229-140">Die zugeordnete Skript Methode ist [**WSMAN. enumerationflaghierarchyflache**](wsman-enumerationflaghierarchyshallow.md) , und die C++-Methode ist [**iwsmanex. enumerationflaghierarchyflache**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span><span class="sxs-lookup"><span data-stu-id="80229-140">The associated scripting method is [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80229-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**Wsmanflaghierarchydeepbasepropsonly**</span><span class="sxs-lookup"><span data-stu-id="80229-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80229-142">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="80229-142">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="80229-143">Abgeleitete Klassen Instanzen werden eingeschlossen und entsprechend dem Basisklassen Schema dargestellt.</span><span class="sxs-lookup"><span data-stu-id="80229-143">Derived class instances are included and are represented according to the base class schema.</span></span> <span data-ttu-id="80229-144">Eigenschaften, die in der abgeleiteten Klasse definiert sind, werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80229-144">Properties defined in the derived class are not shown.</span></span>

<span data-ttu-id="80229-145">Die zugeordnete Skript Methode lautet [**WSMAN. enumerationflaghierarchydeepbasepropsonly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) , und die C++-Methode ist [**iwsmanex. enumerationflaghierarchydeepbasepropsonly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span><span class="sxs-lookup"><span data-stu-id="80229-145">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80229-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80229-146">Requirements</span></span>



| <span data-ttu-id="80229-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80229-147">Requirement</span></span> | <span data-ttu-id="80229-148">Wert</span><span class="sxs-lookup"><span data-stu-id="80229-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80229-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80229-149">Minimum supported client</span></span><br/> | <span data-ttu-id="80229-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80229-150">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="80229-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80229-151">Minimum supported server</span></span><br/> | <span data-ttu-id="80229-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80229-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="80229-153">Header</span><span class="sxs-lookup"><span data-stu-id="80229-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="80229-154"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="80229-154"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="80229-155">IDL</span><span class="sxs-lookup"><span data-stu-id="80229-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80229-156"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80229-156"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80229-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80229-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80229-158">WinRM-Konstanten und-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="80229-158">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="80229-159">Auflisten oder Auflisten aller Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="80229-159">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="80229-160">Abfragen für bestimmte Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="80229-160">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





