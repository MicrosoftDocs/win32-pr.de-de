---
title: Enumerator. ReadItem-Methode (WSManDisp. h)
description: Ruft ein Element aus der Ressource ab und gibt eine XML-Darstellung des Elements zurück.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- ReadItem-Methode Windows-Remoteverwaltung
- ReadItem-Methode Windows-Remoteverwaltung, Enumeratorobjekt
- Enumeratorobjekt Windows-Remoteverwaltung, ReadItem-Methode
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040380"
---
# <a name="enumeratorreaditem-method"></a><span data-ttu-id="6b348-106">Enumerator. ReadItem-Methode</span><span class="sxs-lookup"><span data-stu-id="6b348-106">Enumerator.ReadItem method</span></span>

<span data-ttu-id="6b348-107">Ruft ein Element aus der Ressource ab und gibt eine XML-Darstellung des Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="6b348-107">Retrieves an item from the resource and returns an XML representation of the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b348-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b348-108">Syntax</span></span>


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a><span data-ttu-id="6b348-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b348-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b348-110">*resource*</span><span class="sxs-lookup"><span data-stu-id="6b348-110">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="6b348-111">Der URI des Elements.</span><span class="sxs-lookup"><span data-stu-id="6b348-111">The URI of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b348-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b348-112">Return value</span></span>

<span data-ttu-id="6b348-113">Die XML-Darstellung des Elements.</span><span class="sxs-lookup"><span data-stu-id="6b348-113">The XML representation of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b348-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b348-114">Remarks</span></span>

<span data-ttu-id="6b348-115">Um die Anzahl der gelesenen Elemente einzuschränken, legen Sie die Eigenschaft [**Session.Batchitems**](session-batchitems.md) ) fest.</span><span class="sxs-lookup"><span data-stu-id="6b348-115">To limit the number of items that are read, set the [**Session.BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="6b348-116">Beachten Sie, dass die Freigabe des Enumerationsobjekt alle ausstehenden enumerationsanforderungen bereinigt.</span><span class="sxs-lookup"><span data-stu-id="6b348-116">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span>

<span data-ttu-id="6b348-117">Die [**Session. Enumerate**](session-enumerate.md) -Methode ruft eine Auflistung nicht auf die gleiche Weise ab, wie eine [WMI-Abfrage](/windows/desktop/WmiSdk/querying-wmi), wie z `SELECT * from Win32_LogicalDisk` . b., eine Auflistung in einem [**errbewbjectset**](/windows/desktop/WmiSdk/swbemobjectset)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6b348-117">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in the same way that a [WMI query](/windows/desktop/WmiSdk/querying-wmi), such as `SELECT * from Win32_LogicalDisk`, returns a collection in an [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span></span> <span data-ttu-id="6b348-118">Um eine Datei als Textstream zu lesen, erstellen Sie das Skript- [Textstream](/previous-versions//312a5kbt(v=vs.85)) -Objekt, und rufen Sie die [Textstream. read line](/previous-versions//h7se9d4f(v=vs.85)) -Methode auf, um jede Zeile der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="6b348-118">To read a file as a text stream, you create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="6b348-119">Auf ähnliche Weise rufen Sie die **Session. Enumerate** -Methode auf, um ein [**Enumeratorobjekt**](enumerator.md) zu erhalten, und rufen dann die **Enumerator. ReadItem** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="6b348-119">In a similar way, you call the **Session.Enumerate** method to obtain an [**Enumerator**](enumerator.md) object and then call the **Enumerator.ReadItem** method.</span></span> <span data-ttu-id="6b348-120">Wie beim Lesen aus der Textdatei können Sie die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Eigenschaft überprüfen, um zu überprüfen, ob Sie das Ende der Datenelemente erreicht haben.</span><span class="sxs-lookup"><span data-stu-id="6b348-120">As in reading from the text file, you can check the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

## <a name="examples"></a><span data-ttu-id="6b348-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b348-121">Examples</span></span>

<span data-ttu-id="6b348-122">Im folgenden VBScript-Beispiel wird die [**Session. Enumerate**](session-enumerate.md) -Methode aufgerufen, um eine Liste geplanter Aufträge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6b348-122">The following VBScript example calls the [**Session.Enumerate**](session-enumerate.md) method to obtain a list of scheduled jobs.</span></span> <span data-ttu-id="6b348-123">Die DisplayOutput-Unterroutine verwendet das WinRM-Befehlszeilen Tool XML Transform File (WsmTxt. Xsl), um die Daten in tabellarischer Form auszugeben.</span><span class="sxs-lookup"><span data-stu-id="6b348-123">The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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



## <a name="requirements"></a><span data-ttu-id="6b348-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b348-124">Requirements</span></span>



| <span data-ttu-id="6b348-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b348-125">Requirement</span></span> | <span data-ttu-id="6b348-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6b348-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b348-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b348-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6b348-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b348-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6b348-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b348-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6b348-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b348-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6b348-131">Header</span><span class="sxs-lookup"><span data-stu-id="6b348-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b348-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b348-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b348-133">IDL</span><span class="sxs-lookup"><span data-stu-id="6b348-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b348-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b348-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6b348-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b348-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b348-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b348-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b348-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6b348-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b348-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b348-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b348-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b348-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b348-140">**Enumerator**</span><span class="sxs-lookup"><span data-stu-id="6b348-140">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="6b348-141">Auflisten oder Auflisten aller Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="6b348-141">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

