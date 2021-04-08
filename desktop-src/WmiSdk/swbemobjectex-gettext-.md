---
description: Gibt eine XML-Darstellung eines Objekts oder einer Instanz zurück. Die Textdatei wird im angegebenen XML-Format formatiert, wie in wbemubjecttextformatenum gezeigt.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: SWbemObjectEx.GetText_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050467"
---
# <a name="swbemobjectexgettext_-method"></a><span data-ttu-id="e6ee7-104">Methode ' errbemubjectex. gettext ' \_</span><span class="sxs-lookup"><span data-stu-id="e6ee7-104">SWbemObjectEx.GetText\_ method</span></span>

<span data-ttu-id="e6ee7-105">Die **gettext \_** -Methode des " [**errbemubjectex**](swbemobjectex.md) "-Objekts gibt eine XML-Darstellung eines Objekts oder einer Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-105">The **GetText\_** method of the [**SWbemObjectEx**](swbemobjectex.md) object returns an XML representation of an object or instance.</span></span> <span data-ttu-id="e6ee7-106">Die Textdatei wird im angegebenen XML-Format formatiert, wie in [**wbemubjecttextformatenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-106">The text file is formatted in the XML format specified as shown in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span></span>

<span data-ttu-id="e6ee7-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e6ee7-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ee7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6ee7-108">Syntax</span></span>


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e6ee7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6ee7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ee7-110">*itextformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6ee7-110">*iTextFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ee7-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-111">Required.</span></span> <span data-ttu-id="e6ee7-112">Ein Wert aus [**wbemubjecttextformatenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) , der das resultierende XML-Format angibt.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-112">A value from [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) that specifies the resulting XML format.</span></span>

</dd> <dt>

<span data-ttu-id="e6ee7-113">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e6ee7-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ee7-114">Reservierte Vorgangs-Flags.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-114">Reserved operation flags.</span></span> <span data-ttu-id="e6ee7-115">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e6ee7-115">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="e6ee7-116">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="e6ee7-116">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ee7-117">Ein [**-**](swbemnamedvalueset.md) Objekt, das den Kontext für den Vorgang festlegt.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span> <span data-ttu-id="e6ee7-118">Der Standardwert ist NULL.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-118">The default is null.</span></span> <span data-ttu-id="e6ee7-119">Weitere Informationen zu den zulässigen Name-Wert-Paaren finden Sie unten in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-119">For more information about the name/value pairs permitted, see Remarks below.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ee7-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6ee7-120">Return value</span></span>

<span data-ttu-id="e6ee7-121">Diese Methode hat keine Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-121">This method has no return values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6ee7-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e6ee7-122">Error codes</span></span>

<span data-ttu-id="e6ee7-123">Nach Abschluss der **gettext \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-123">After completion of the **GetText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e6ee7-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e6ee7-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e6ee7-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-125">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e6ee7-126">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="e6ee7-126">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="e6ee7-127">Das angeforderte Format wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-127">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e6ee7-128">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e6ee7-128">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e6ee7-129">Einer der Parameter für den Aufruf ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-129">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="e6ee7-130">**wbemErrCriticalError** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="e6ee7-130">**wbemErrCriticalError** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="e6ee7-131">Ein interner, schwerwiegender und unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-131">An internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="e6ee7-132">Melden Sie diesen Fehler dem technischen Support von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-132">Report this error to Microsoft Technical Support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6ee7-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6ee7-133">Remarks</span></span>

<span data-ttu-id="e6ee7-134">Beim Erstellen des " [**Swap**](swbemnamedvalueset.md)Name/Value"-Paars sind nur die folgenden Name/Wert-Paare zulässig.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-134">When constructing your [**SWbemNamedValueSet**](swbemnamedvalueset.md), only the following name/value pairs are permitted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6ee7-135">Name</span><span class="sxs-lookup"><span data-stu-id="e6ee7-135">Name</span></span></th>
<th><span data-ttu-id="e6ee7-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e6ee7-136">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6ee7-137">LocalOnly</span><span class="sxs-lookup"><span data-stu-id="e6ee7-137">LocalOnly</span></span></td>
<td><span data-ttu-id="e6ee7-138"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="e6ee7-138"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="e6ee7-139"><strong>True</strong>gibt an, dass nur lokal definierte Eigenschaften und Methoden im resultierenden XML-Code vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-139">If <strong>TRUE</strong>, only locally defined properties and methods are present in the resulting XML.</span></span> <span data-ttu-id="e6ee7-140">Der Standardwert ist <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-140">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6ee7-141">Includezqualifizierer</span><span class="sxs-lookup"><span data-stu-id="e6ee7-141">IncludeQualifiers</span></span></td>
<td><span data-ttu-id="e6ee7-142"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="e6ee7-142"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="e6ee7-143"><strong>True</strong>gibt an, dass Qualifizierer von Klassen, Instanzen, Eigenschaften und Methoden im resultierenden XML-Code enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-143">If <strong>TRUE</strong>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.</span></span> <span data-ttu-id="e6ee7-144">Der Standardwert ist <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-144">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6ee7-145">Pathlevel</span><span class="sxs-lookup"><span data-stu-id="e6ee7-145">PathLevel</span></span></td>
<td><span data-ttu-id="e6ee7-146"><strong>VT-I4</strong></span><span class="sxs-lookup"><span data-stu-id="e6ee7-146"><strong>VT-I4</strong></span></span><br/> <span data-ttu-id="e6ee7-147">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e6ee7-147">Default is 0 (zero).</span></span> <span data-ttu-id="e6ee7-148">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="e6ee7-148">Possible values are:</span></span><br/>
<ul>
<li><span data-ttu-id="e6ee7-149">0: abhängig davon, <CLASS> <INSTANCE> ob das Objekt eine Klasse oder eine Instanz ist, wird ein-oder-Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-149">0: A <CLASS> or <INSTANCE> element is created depending on whether the object is a class or instance.</span></span></li>
<li><span data-ttu-id="e6ee7-150">1: ein- <VALUE.NAMEDOBJECT> Element wird generiert.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-150">1: A <VALUE.NAMEDOBJECT> element is generated.</span></span></li>
<li><span data-ttu-id="e6ee7-151">2: ein- <VALUE.OBJECTWITHLOCALPATH> Element wird generiert.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-151">2: A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span></li>
<li><span data-ttu-id="e6ee7-152">3: ein- <VALUE.OBJECTWITHPATH> Element wird generiert.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-152">3: A <VALUE.OBJECTWITHPATH> element is generated.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6ee7-153">Excludebug SystemProperties</span><span class="sxs-lookup"><span data-stu-id="e6ee7-153">ExcludeSystemProperties</span></span></td>
<td><span data-ttu-id="e6ee7-154"><strong>VT-bool</strong></span><span class="sxs-lookup"><span data-stu-id="e6ee7-154"><strong>VT-BOOL</strong></span></span><br/> <span data-ttu-id="e6ee7-155"><strong>True</strong>gibt an, dass Systemeigenschaften wie __NAMESPACE aus der Ausgabe ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-155">If <strong>TRUE</strong>, system properties, like __NAMESPACE, are excluded from the output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6ee7-156">Includeclassorigin</span><span class="sxs-lookup"><span data-stu-id="e6ee7-156">IncludeClassOrigin</span></span></td>
<td><span data-ttu-id="e6ee7-157"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="e6ee7-157"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="e6ee7-158">Wenn <strong>true</strong>, wird das Klassen Ursprungs Attribut für das <PROPERTY> -Element und das-Element festgelegt <METHOD> .</span><span class="sxs-lookup"><span data-stu-id="e6ee7-158">If <strong>TRUE</strong>, the class origin attribute is set on the <PROPERTY> and <METHOD> elements.</span></span> <span data-ttu-id="e6ee7-159">Der Standardwert ist <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-159">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e6ee7-160">Weitere Informationen zum Erstellen eines " [**taubemnamedvalueset**](swbemnamedvalueset.md)" finden [**Sie unter "austauschen von namedvalueset. Add**](swbemnamedvalueset-add.md)".</span><span class="sxs-lookup"><span data-stu-id="e6ee7-160">For more information about creating an [**SWbemNamedValueSet**](swbemnamedvalueset.md), see [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e6ee7-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6ee7-161">Examples</span></span>

<span data-ttu-id="e6ee7-162">Das folgende Skript zeigt, wie eine XML-Darstellung der [**Win32- \_ BIOS**](/windows/desktop/CIMWin32Prov/win32-bios) -Klassendefinition abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-162">The following script shows how to obtain an XML representation of the [**Win32\_Bios**](/windows/desktop/CIMWin32Prov/win32-bios) class definition.</span></span> <span data-ttu-id="e6ee7-163">Wenn Sie eine bestimmte Instanz des **Win32- \_ BIOS** angeben, können Sie die Daten dieses Objekts in XML abrufen.</span><span class="sxs-lookup"><span data-stu-id="e6ee7-163">By specifying a particular instance of **Win32\_Bios**, you can obtain that object's data in XML.</span></span>


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a><span data-ttu-id="e6ee7-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6ee7-164">Requirements</span></span>



| <span data-ttu-id="e6ee7-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6ee7-165">Requirement</span></span> | <span data-ttu-id="e6ee7-166">Wert</span><span class="sxs-lookup"><span data-stu-id="e6ee7-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ee7-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6ee7-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ee7-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6ee7-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e6ee7-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6ee7-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ee7-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6ee7-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e6ee7-171">Header</span><span class="sxs-lookup"><span data-stu-id="e6ee7-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6ee7-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6ee7-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6ee7-173">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e6ee7-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6ee7-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e6ee7-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e6ee7-175">DLL</span><span class="sxs-lookup"><span data-stu-id="e6ee7-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6ee7-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6ee7-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e6ee7-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="e6ee7-177">CLSID</span></span><br/>                    | <span data-ttu-id="e6ee7-178">CLSID- \_ Swap-Austausch</span><span class="sxs-lookup"><span data-stu-id="e6ee7-178">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="e6ee7-179">IID</span><span class="sxs-lookup"><span data-stu-id="e6ee7-179">IID</span></span><br/>                      | <span data-ttu-id="e6ee7-180">IID \_ iswbejebjectex</span><span class="sxs-lookup"><span data-stu-id="e6ee7-180">IID\_ISWbemObjectEx</span></span><br/>                                                          |



 

