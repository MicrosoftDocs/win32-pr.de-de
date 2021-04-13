---
title: Session. Timeout-Eigenschaft (WSManDisp. h)
description: Legt die maximale Zeitspanne (in Millisekunden) fest, die die Client Anwendung wartet, bis Windows-Remoteverwaltung den Vorgang beendet.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Timeout-Eigenschaft Windows-Remoteverwaltung
- Timeout-Eigenschaft Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Timeout-Eigenschaft
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341358"
---
# <a name="sessiontimeout-property"></a><span data-ttu-id="3ca49-106">Session. Timeout (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3ca49-106">Session.Timeout property</span></span>

<span data-ttu-id="3ca49-107">Legt die maximale Zeitspanne (in Millisekunden) fest, die die Client Anwendung wartet, bis Windows-Remoteverwaltung den Vorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="3ca49-107">Sets and gets the maximum amount of time, in milliseconds, that the client application waits for Windows Remote Management to complete its operations.</span></span>

<span data-ttu-id="3ca49-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3ca49-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca49-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ca49-109">Syntax</span></span>


```VB
Session.Timeout As long
```



## <a name="property-value"></a><span data-ttu-id="3ca49-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3ca49-110">Property value</span></span>

<span data-ttu-id="3ca49-111">Timeout Wert in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="3ca49-111">Time-out value, in milliseconds.</span></span> <span data-ttu-id="3ca49-112">Wenn der Timeout Wert überschritten wird, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="3ca49-112">When the time-out value is exceeded, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca49-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ca49-113">Remarks</span></span>

<span data-ttu-id="3ca49-114">Der Timeout Wert kann vor jedem vom Agent ausgeführten Vorgang festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3ca49-114">The time-out value can be set before each operation performed by the agent.</span></span> <span data-ttu-id="3ca49-115">Wenn kein Timeout Wert angegeben wird, legt der Agent den Timeout Wert fest.</span><span class="sxs-lookup"><span data-stu-id="3ca49-115">If a time-out value is not specified, the agent sets the time-out value.</span></span>

<span data-ttu-id="3ca49-116">Während eines Enumerationsvorgangs kann der Timeout Wert nicht zurückgesetzt werden, während die Ressource aufgezählt wird.</span><span class="sxs-lookup"><span data-stu-id="3ca49-116">During an enumerate operation, the time-out value cannot be reset while the resource is being enumerated.</span></span>

## <a name="examples"></a><span data-ttu-id="3ca49-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ca49-117">Examples</span></span>

<span data-ttu-id="3ca49-118">Im folgenden VBScript-Codebeispiel wird ein Calc.exe Prozess mit der [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode der WMI- [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse gestartet.</span><span class="sxs-lookup"><span data-stu-id="3ca49-118">The following VBScript code example starts a Calc.exe process using the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span> <span data-ttu-id="3ca49-119">Der *strinputparameters* -Parameter enthält die Eingabeparameter im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="3ca49-119">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="3ca49-120">Das Skript gibt ein Timeout für die Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="3ca49-120">The script specifies a time-out for the session.</span></span>


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

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

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



## <a name="requirements"></a><span data-ttu-id="3ca49-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ca49-121">Requirements</span></span>



| <span data-ttu-id="3ca49-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ca49-122">Requirement</span></span> | <span data-ttu-id="3ca49-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3ca49-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca49-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ca49-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca49-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ca49-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3ca49-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ca49-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca49-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ca49-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3ca49-128">Header</span><span class="sxs-lookup"><span data-stu-id="3ca49-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca49-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca49-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ca49-130">IDL</span><span class="sxs-lookup"><span data-stu-id="3ca49-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ca49-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ca49-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ca49-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3ca49-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ca49-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ca49-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ca49-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca49-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ca49-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ca49-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ca49-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ca49-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca49-137">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="3ca49-137">**Session**</span></span>](session.md)
</dt> </dl>

 

