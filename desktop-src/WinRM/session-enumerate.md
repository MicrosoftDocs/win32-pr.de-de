---
title: Session. Enumerate-Methode (WSManDisp. h)
description: Listet eine Tabelle, eine Datensammlung oder eine Protokoll Ressource auf.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumerate-Methode Windows-Remoteverwaltung
- Enumerate-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Enumerate-Methode
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040379"
---
# <a name="sessionenumerate-method"></a><span data-ttu-id="b15c8-106">Session. Enumerate-Methode</span><span class="sxs-lookup"><span data-stu-id="b15c8-106">Session.Enumerate method</span></span>

<span data-ttu-id="b15c8-107">Listet eine Tabelle, eine Datensammlung oder eine Protokoll Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="b15c8-107">Enumerates a table, data collection, or log resource.</span></span> <span data-ttu-id="b15c8-108">Um eine Abfrage zu erstellen, schließen Sie einen *Filter* Parameter und einen *Dialekt* Parameter in eine Enumeration ein.</span><span class="sxs-lookup"><span data-stu-id="b15c8-108">To create a query, include a *filter* parameter and a *dialect* parameter in an enumeration.</span></span> <span data-ttu-id="b15c8-109">Sie können auch ein [**ResourceLocator**](resourcelocator.md) -Objekt verwenden, um Abfragen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b15c8-109">You can also use a [**ResourceLocator**](resourcelocator.md) object to create queries.</span></span> <span data-ttu-id="b15c8-110">Weitere Informationen finden Sie unter [auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="b15c8-110">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b15c8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b15c8-111">Syntax</span></span>


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b15c8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b15c8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b15c8-113">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b15c8-113">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15c8-114">Der Bezeichner der abzurufenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="b15c8-114">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="b15c8-115">Dieser Parameter kann einen der folgenden Parameter enthalten:</span><span class="sxs-lookup"><span data-stu-id="b15c8-115">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="b15c8-116">Der URI der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b15c8-116">The URI of the resource.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   <span data-ttu-id="b15c8-117">Ein [**ResourceLocator**](resourcelocator.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b15c8-117">A [**ResourceLocator**](resourcelocator.md) object.</span></span>
-   <span data-ttu-id="b15c8-118">Ein [*WS-adressierungsend*](windows-remote-management-glossary.md) Punkt Verweis, wie im WS-Management Protocol-Standard beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b15c8-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="b15c8-119">Weitere Informationen zur öffentlichen Spezifikation für [WS-Management-Protokoll](ws-management-protocol.md)finden Sie auf der [Seite Verwaltungs Spezifikationen Index](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="b15c8-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="b15c8-120">*Filter* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b15c8-120">*filter* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b15c8-121">Ein Filter, der definiert, welche Elemente in der Ressource von der-Enumeration zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b15c8-121">A filter that defines what items in the resource are returned by the enumeration.</span></span> <span data-ttu-id="b15c8-122">Wenn die Ressource aufgelistet ist, werden nur die Elemente zurückgegeben, die mit den Filterkriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b15c8-122">When the resource is enumerated, only those items that match the filter criteria are returned.</span></span> <span data-ttu-id="b15c8-123">Wenn Sie einen *Filter* Parameter und einen *Dialekt* Parameter in eine Enumeration einschließen, wird die Enumeration in eine Abfrage konvertiert.</span><span class="sxs-lookup"><span data-stu-id="b15c8-123">Including a *filter* parameter and a *dialect* parameter in an enumeration converts the enumeration into a query.</span></span> <span data-ttu-id="b15c8-124">Ein Beispiel finden Sie unter [Abfragen für bestimmte Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="b15c8-124">For an example, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

<span data-ttu-id="b15c8-125">Wenn Sie über ein [**ResourceLocator**](resourcelocator.md) -Objekt für den *resourceUri* -Parameter verfügen, sollte dieser Parameter nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b15c8-125">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="b15c8-126">*Dialekt* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b15c8-126">*dialect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b15c8-127">Die Sprache, die vom Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b15c8-127">The language used by the filter.</span></span> <span data-ttu-id="b15c8-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), eine Teilmenge von SQL, die von WMI verwendet wird, ist die einzige unterstützte Sprache.</span><span class="sxs-lookup"><span data-stu-id="b15c8-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), a subset of SQL used by WMI, is the only language supported.</span></span>

<span data-ttu-id="b15c8-129">Wenn Sie über ein [**ResourceLocator**](resourcelocator.md) -Objekt für den *resourceUri* -Parameter verfügen, sollte dieser Parameter nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b15c8-129">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="b15c8-130">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b15c8-130">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b15c8-131">Ein Parameter, der in der **\_ \_ wsmanenumflags** -Enumeration ein Flag enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="b15c8-131">A parameter that must contain a flag in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="b15c8-132">Weitere Informationen finden Sie unter [Enumerationskonstanten](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b15c8-132">For more information, see [Enumeration Constants](enumeration-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b15c8-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b15c8-133">Return value</span></span>

<span data-ttu-id="b15c8-134">Ein [**Enumeratorobjekt**](enumerator.md) , das die Ergebnisse der-Enumeration enthält.</span><span class="sxs-lookup"><span data-stu-id="b15c8-134">An [**Enumerator**](enumerator.md) object that contains the results of the enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="b15c8-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b15c8-135">Remarks</span></span>

<span data-ttu-id="b15c8-136">Weitere Informationen zum Einschränken von Netzwerk aufrufen während einer Enumeration finden Sie in der Eigenschaft [**batchitems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="b15c8-136">For more information about limiting network calls during an enumeration, see the [**BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="b15c8-137">Beachten Sie, dass wenn die Flags die [**Enumerationskonstanten**](enumeration-constants.md) **wsmanflaghierarchydeepbasepropsonly** oder **wsmanflaghierarchyflache** enthalten, Windows-Remoteverwaltung Dienst den Fehlercode **Fehler \_ WSMAN \_ Polymorphism- \_ Modus \_ nicht unterstützt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b15c8-137">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then Windows Remote Management service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

<span data-ttu-id="b15c8-138">Wenn ein Filter angegeben wird, muss es sich um ein gültiges Dokument in Bezug auf das Schema der Ressource handeln.</span><span class="sxs-lookup"><span data-stu-id="b15c8-138">If a filter is specified, it must be a valid document with respect to the schema of the resource.</span></span> <span data-ttu-id="b15c8-139">Der Dialekt Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b15c8-139">The dialect parameter is optional.</span></span> <span data-ttu-id="b15c8-140">Wenn die Filter Zeichenfolge jedoch mit < beginnt, aber kein XML-Fragment ist, fügen Sie entweder den *Dialekt* Parameter ein, oder legen Sie das **wsmanflagnonxmltext** -Flag im *Flags* -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="b15c8-140">However, if the filter string begins with <, but is not an XML fragment, then either include the *dialect* parameter or set the **WSManFlagNonXmlText** flag in the *flags* parameter.</span></span> <span data-ttu-id="b15c8-141">Weitere Informationen finden Sie unter [**Enumerationskonstanten**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b15c8-141">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

<span data-ttu-id="b15c8-142">Die entsprechende C++-Methode ist [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="b15c8-142">The corresponding C++ method is [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

## <a name="examples"></a><span data-ttu-id="b15c8-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b15c8-143">Examples</span></span>

<span data-ttu-id="b15c8-144">Im folgenden VBScript-Codebeispiel werden die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanzen auf einem Remote Computer aufgelistet, der durch den voll qualifizierten Domänen Namen (Servername.Domain.com) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b15c8-144">The following VBScript code example enumerates the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instances on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="b15c8-145">Beachten Sie, dass das Freigeben des Enumerationsobjekt ausstehende enumerationsanforderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="b15c8-145">Be aware that freeing the enumeration object clears pending enumeration requests.</span></span> <span data-ttu-id="b15c8-146">Die DisplayOutput-Unterroutine verwendet die XML-Transformations Datei (WsmTxt. Xsl) des WinRM-Befehlszeilen Tools, um die Daten in tabellarischer Form auszugeben.</span><span class="sxs-lookup"><span data-stu-id="b15c8-146">The DisplayOutput subroutine uses the Winrm command-line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b15c8-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b15c8-147">Requirements</span></span>



| <span data-ttu-id="b15c8-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b15c8-148">Requirement</span></span> | <span data-ttu-id="b15c8-149">Wert</span><span class="sxs-lookup"><span data-stu-id="b15c8-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b15c8-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b15c8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b15c8-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b15c8-151">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b15c8-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b15c8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b15c8-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b15c8-153">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b15c8-154">Header</span><span class="sxs-lookup"><span data-stu-id="b15c8-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="b15c8-155"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b15c8-155"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b15c8-156">IDL</span><span class="sxs-lookup"><span data-stu-id="b15c8-156">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b15c8-157"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b15c8-157"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b15c8-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b15c8-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="b15c8-159"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b15c8-159"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b15c8-160">DLL</span><span class="sxs-lookup"><span data-stu-id="b15c8-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b15c8-161"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b15c8-161"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b15c8-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b15c8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15c8-163">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="b15c8-163">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="b15c8-164">Abfragen für bestimmte Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="b15c8-164">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="b15c8-165">**Batchitems**</span><span class="sxs-lookup"><span data-stu-id="b15c8-165">**BatchItems**</span></span>](session-batchitems.md)
</dt> <dt>

[<span data-ttu-id="b15c8-166">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="b15c8-166">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

