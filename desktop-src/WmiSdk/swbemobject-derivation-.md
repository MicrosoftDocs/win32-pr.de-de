---
description: Die Ableitung- \_ Eigenschaft des "errbemubject"-Objekts enthält ein Array von Zeichen folgen, die die Klassen abderivations Hierarchie für die Instanz beschreiben, auf die verwiesen wird.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: SWbemObject.Derivation_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84e7b4e53a1a5544c92bb5116f3f83189789487f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351786"
---
# <a name="swbemobjectderivation_-property"></a><span data-ttu-id="f86e6-103">Errbemubject. derivations ( \_ Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f86e6-103">SWbemObject.Derivation\_ property</span></span>

<span data-ttu-id="f86e6-104">Die **Ableitung \_** -Eigenschaft des " [**errbemubject**](swbemobject.md) "-Objekts enthält ein Array von Zeichen folgen, die die Klassen abderivations Hierarchie für die Instanz beschreiben, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f86e6-104">The **Derivation\_** property of the [**SWbemObject**](swbemobject.md) object contains an array of strings that describe the class derivation hierarchy for the instance being referenced.</span></span> <span data-ttu-id="f86e6-105">Das erste Element im Array definiert die übergeordnete Klasse, und das letzte Element definiert die Klasse "Dynastie".</span><span class="sxs-lookup"><span data-stu-id="f86e6-105">The first element in the array defines the parent class and the last element defines the dynasty class.</span></span> <span data-ttu-id="f86e6-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f86e6-106">This property is read-only.</span></span>

<span data-ttu-id="f86e6-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f86e6-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f86e6-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f86e6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86e6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f86e6-109">Syntax</span></span>


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a><span data-ttu-id="f86e6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f86e6-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="f86e6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f86e6-111">Examples</span></span>

<span data-ttu-id="f86e6-112">Im folgenden VBScript-Beispiel wird beschrieben, wie die Klassenhierarchie für Win32 \_ LogicalDisk abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f86e6-112">The following VBScript sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



<span data-ttu-id="f86e6-113">Im folgenden Perl-Beispiel wird beschrieben, wie die Klassenhierarchie für Win32 \_ LogicalDisk abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f86e6-113">he following Perl sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="f86e6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f86e6-114">Requirements</span></span>



| <span data-ttu-id="f86e6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f86e6-115">Requirement</span></span> | <span data-ttu-id="f86e6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f86e6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f86e6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f86e6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f86e6-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f86e6-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f86e6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f86e6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f86e6-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f86e6-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f86e6-121">Header</span><span class="sxs-lookup"><span data-stu-id="f86e6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f86e6-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f86e6-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f86e6-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f86e6-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f86e6-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f86e6-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f86e6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f86e6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f86e6-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f86e6-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f86e6-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="f86e6-127">CLSID</span></span><br/>                    | <span data-ttu-id="f86e6-128">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="f86e6-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f86e6-129">IID</span><span class="sxs-lookup"><span data-stu-id="f86e6-129">IID</span></span><br/>                      | <span data-ttu-id="f86e6-130">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="f86e6-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




