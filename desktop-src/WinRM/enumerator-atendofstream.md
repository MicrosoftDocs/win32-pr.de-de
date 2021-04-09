---
title: Enumerator. atendovstream-Eigenschaft (WSManDisp. h)
description: Ruft einen booleschen Wert ab, der angibt, ob in der Auflistung weitere Elemente vorhanden sind.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Atendotstream-Eigenschaft Windows-Remoteverwaltung
- Atendobstream-Eigenschaft Windows-Remoteverwaltung, Enumeratorobjekt
- EnumeratorobjektWindows-Remoteverwaltung, atendobstream-Eigenschaft
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103266"
---
# <a name="enumeratoratendofstream-property"></a><span data-ttu-id="efed5-106">Enumerator. atendovstream (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="efed5-106">Enumerator.AtEndOfStream property</span></span>

<span data-ttu-id="efed5-107">Ruft einen booleschen Wert ab, der angibt, ob in der Auflistung weitere Elemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="efed5-107">Gets a Boolean value that indicates whether there are any more items in the collection.</span></span>

<span data-ttu-id="efed5-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="efed5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="efed5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="efed5-109">Syntax</span></span>


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="efed5-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="efed5-110">Property value</span></span>

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="efed5-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Fall**</span><span class="sxs-lookup"><span data-stu-id="efed5-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span></span>


</dt> <dd>

<span data-ttu-id="efed5-112">Es sind keine weiteren Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="efed5-112">No more items are in the collection.</span></span>

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="efed5-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Alarm**</span><span class="sxs-lookup"><span data-stu-id="efed5-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span></span>


</dt> <dd>

<span data-ttu-id="efed5-114">Es sind weitere Elemente verfügbar.</span><span class="sxs-lookup"><span data-stu-id="efed5-114">More items are available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efed5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efed5-115">Remarks</span></span>

<span data-ttu-id="efed5-116">Wenn Sie das [**Enumeratorobjekt**](enumerator.md) freigeben, nachdem Sie alle benötigten Daten erhalten haben, werden alle ausstehenden enumerationsanforderungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="efed5-116">If you free the [**Enumerator**](enumerator.md) object after you have obtained all the data required, then any pending enumeration requests are removed.</span></span> <span data-ttu-id="efed5-117">Weitere Informationen finden Sie unter [auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="efed5-117">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="examples"></a><span data-ttu-id="efed5-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efed5-118">Examples</span></span>

<span data-ttu-id="efed5-119">Im folgenden VBScript-Beispiel werden Betriebssystem Instanzen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="efed5-119">The following VBScript example enumerates operating system instances.</span></span> <span data-ttu-id="efed5-120">Beachten Sie, dass die Freigabe des Enumerationsobjekt alle ausstehenden enumerationsanforderungen bereinigt.</span><span class="sxs-lookup"><span data-stu-id="efed5-120">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span> <span data-ttu-id="efed5-121">Die DisplayOutput-Unterroutine formatiert die Datenausgabe auf die gleiche Weise wie das WinRM. cmd-Tool.</span><span class="sxs-lookup"><span data-stu-id="efed5-121">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

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



## <a name="requirements"></a><span data-ttu-id="efed5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efed5-122">Requirements</span></span>



| <span data-ttu-id="efed5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efed5-123">Requirement</span></span> | <span data-ttu-id="efed5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="efed5-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="efed5-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efed5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="efed5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efed5-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="efed5-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efed5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="efed5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efed5-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="efed5-129">Header</span><span class="sxs-lookup"><span data-stu-id="efed5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="efed5-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="efed5-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="efed5-131">IDL</span><span class="sxs-lookup"><span data-stu-id="efed5-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="efed5-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="efed5-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="efed5-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="efed5-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="efed5-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="efed5-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="efed5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="efed5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efed5-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efed5-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="efed5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efed5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efed5-138">**Enumerator**</span><span class="sxs-lookup"><span data-stu-id="efed5-138">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="efed5-139">Auflisten oder Auflisten aller Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="efed5-139">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





