---
title: Session. aufrufen-Methode (WSManDisp. h)
description: Ruft eine Methode auf und gibt die Ergebnisse des Methodenaufrufs zurück.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Methoden Windows-Remoteverwaltung aufrufen
- Methoden Windows-Remoteverwaltung aufrufen, Sitzungs Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Methode "aufrufen"
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743224"
---
# <a name="sessioninvoke-method"></a><span data-ttu-id="5ca06-106">Session. aufrufen-Methode</span><span class="sxs-lookup"><span data-stu-id="5ca06-106">Session.Invoke method</span></span>

<span data-ttu-id="5ca06-107">Ruft eine Methode auf und gibt die Ergebnisse des Methodenaufrufs zurück.</span><span class="sxs-lookup"><span data-stu-id="5ca06-107">Invokes a method and returns the results of the method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca06-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ca06-108">Syntax</span></span>


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5ca06-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ca06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca06-110">*Aktions-URI* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ca06-110">*actionUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca06-111">Der URI der aufzurufenden Methode.</span><span class="sxs-lookup"><span data-stu-id="5ca06-111">The URI of the method to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="5ca06-112">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ca06-112">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca06-113">Der Bezeichner der abzurufenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="5ca06-113">The identifier of the resource to retrieve.</span></span>

<span data-ttu-id="5ca06-114">Dieser Parameter kann einen der folgenden Parameter enthalten:</span><span class="sxs-lookup"><span data-stu-id="5ca06-114">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="5ca06-115">URI mit oder ohne [*Selektoren*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5ca06-115">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5ca06-116">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird der Schlüssel durch angegeben `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="5ca06-116">In the following Visual Basic Scripting Edition (VBScript) example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="5ca06-117">[**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="5ca06-117">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="5ca06-118">Endpunkt Verweis der [*WS-Adressierung*](windows-remote-management-glossary.md) , wie im [WS-Management-Protokoll](ws-management-protocol.md) -Standard beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5ca06-118">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="5ca06-119">Weitere Informationen zur öffentlichen Spezifikation WS-Management Protokolls finden Sie unter [Verwaltungs Spezifikationen Index page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="5ca06-119">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="5ca06-120">*Parameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ca06-120">*parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca06-121">Die XML-Darstellung der Eingabe für die Methode.</span><span class="sxs-lookup"><span data-stu-id="5ca06-121">The XML representation of the input for the method.</span></span> <span data-ttu-id="5ca06-122">Diese Zeichenfolge muss angegeben werden, oder diese Methode schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="5ca06-122">This string must be supplied or this method will fail.</span></span>

</dd> <dt>

<span data-ttu-id="5ca06-123">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5ca06-123">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca06-124">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="5ca06-124">Reserved.</span></span> <span data-ttu-id="5ca06-125">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5ca06-125">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca06-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ca06-126">Return value</span></span>

<span data-ttu-id="5ca06-127">Die XML-Darstellung der Methoden Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5ca06-127">The XML representation of the method output.</span></span>

## <a name="examples"></a><span data-ttu-id="5ca06-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ca06-128">Examples</span></span>

<span data-ttu-id="5ca06-129">Im folgenden VBScript-Codebeispiel wird ein Calc.exe Prozess gestartet.</span><span class="sxs-lookup"><span data-stu-id="5ca06-129">The following VBScript code example starts a Calc.exe process.</span></span> <span data-ttu-id="5ca06-130">Der *strinputparameters* -Parameter enthält die Eingabeparameter im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="5ca06-130">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="5ca06-131">Der einzige erforderliche Eingabeparameter für die [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode der WMI- [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse ist die auszuführende Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="5ca06-131">The only required input parameter for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is the command line to execute.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



<span data-ttu-id="5ca06-132">Im folgenden VBScript-Codebeispiel wird die **Session. aufrufen** -Methode aufgerufen, um die [**Stop Service**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) -Methode des [**Win32- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service)auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5ca06-132">The following VBScript code example calls the **Session.Invoke** method to execute the [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) method of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="5ca06-133">Die **Stop Service** -Methode hat keine Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="5ca06-133">The **StopService** method does not have input parameters.</span></span> <span data-ttu-id="5ca06-134">Die **Aufruf** Methode erfordert jedoch eine XML-Zeichenfolge im *Parameter para* meters.</span><span class="sxs-lookup"><span data-stu-id="5ca06-134">However, the **Invoke** method requires an XML string in the *parameters* parameter.</span></span>


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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



## <a name="requirements"></a><span data-ttu-id="5ca06-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ca06-135">Requirements</span></span>



| <span data-ttu-id="5ca06-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ca06-136">Requirement</span></span> | <span data-ttu-id="5ca06-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5ca06-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca06-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ca06-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca06-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ca06-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5ca06-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ca06-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca06-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ca06-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5ca06-142">Header</span><span class="sxs-lookup"><span data-stu-id="5ca06-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca06-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca06-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ca06-144">IDL</span><span class="sxs-lookup"><span data-stu-id="5ca06-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ca06-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ca06-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5ca06-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ca06-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ca06-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5ca06-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5ca06-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5ca06-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca06-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca06-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ca06-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ca06-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca06-151">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="5ca06-151">**Session**</span></span>](session.md)
</dt> </dl>

 

