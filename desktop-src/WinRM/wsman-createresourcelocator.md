---
title: WSMAN. kreateresourcelocator-Methode (WSManDisp. h)
description: Erstellt ein ResourceLocator-Objekt, das verwendet werden kann, anstatt einen Ressourcen-URI in Sitzungs Objekt Vorgängen wie "Session. Get", "Session. Put" oder "Session. Enumerate" anzugeben.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung der Methode "kreateresourcelocator"
- Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Methode "kreateresourcelocator"
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949791"
---
# <a name="wsmancreateresourcelocator-method"></a><span data-ttu-id="c58de-106">WSMAN. kreateresourcelocator-Methode</span><span class="sxs-lookup"><span data-stu-id="c58de-106">WSMan.CreateResourceLocator method</span></span>

<span data-ttu-id="c58de-107">Erstellt ein [**ResourceLocator**](resourcelocator.md) -Objekt, das verwendet werden kann, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c58de-107">Creates a [**ResourceLocator**](resourcelocator.md) object that can be used instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c58de-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c58de-108">Syntax</span></span>


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c58de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c58de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c58de-110">*URI* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c58de-110">*uri* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c58de-111">Der Ressourcen-URI für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="c58de-111">The resource URI for the resource.</span></span> <span data-ttu-id="c58de-112">Weitere Informationen zu URI-Zeichen folgen finden Sie unter [Ressourcen-URIs](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="c58de-112">For more information about URI strings, see [Resource URIs](resource-uris.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c58de-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c58de-113">Return value</span></span>

<span data-ttu-id="c58de-114">Ein [**ResourceLocator**](resourcelocator.md) -Objekt, das dann zum Ausführen von lokalen oder Remote-WinRM-Vorgängen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c58de-114">A [**ResourceLocator**](resourcelocator.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="c58de-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c58de-115">Remarks</span></span>

<span data-ttu-id="c58de-116">Wenn die **Fragmentdialekt** -Eigenschaft im [**ResourceLocator**](resourcelocator.md) -Objekt nicht angegeben ist, ist der Standardwert die XPath 1,0-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="c58de-116">If the **FragmentDialect** property is not specified in the [**ResourceLocator**](resourcelocator.md) object, the default is the XPath 1.0 specification.</span></span> <span data-ttu-id="c58de-117">Weitere Informationen finden Sie unter [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="c58de-117">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="examples"></a><span data-ttu-id="c58de-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c58de-118">Examples</span></span>

<span data-ttu-id="c58de-119">Im folgenden VBScript-Codebeispiel wird ein [**ResourceLocator**](resourcelocator.md) -Objekt erstellt und der Eigenschafts Wert für die Netzwerkadapter **Beschreibung** aus der Instanz von [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) mit dem Index "1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c58de-119">The following VBScript code example creates a [**ResourceLocator**](resourcelocator.md) object and gets the network adapter **Description** property value from the instance of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) with an Index of "1".</span></span>


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a><span data-ttu-id="c58de-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c58de-120">Requirements</span></span>



| <span data-ttu-id="c58de-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c58de-121">Requirement</span></span> | <span data-ttu-id="c58de-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c58de-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c58de-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c58de-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c58de-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c58de-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c58de-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c58de-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c58de-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c58de-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c58de-127">Header</span><span class="sxs-lookup"><span data-stu-id="c58de-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c58de-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c58de-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c58de-129">IDL</span><span class="sxs-lookup"><span data-stu-id="c58de-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c58de-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c58de-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c58de-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c58de-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="c58de-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c58de-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c58de-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c58de-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c58de-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c58de-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c58de-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c58de-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c58de-136">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="c58de-136">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c58de-137">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="c58de-137">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="c58de-138">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="c58de-138">**Session**</span></span>](session.md)
</dt> </dl>

 

