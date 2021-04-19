---
description: Ruft den Klassennamen und andere Informationen ab, die einer angegebenen GUID im Manifest einer Komponente zugeordnet sind.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Sxslookupclrguid-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351246"
---
# <a name="sxslookupclrguid-function"></a><span data-ttu-id="14b3b-103">Sxslookupclrguid-Funktion</span><span class="sxs-lookup"><span data-stu-id="14b3b-103">SxsLookupClrGuid function</span></span>

<span data-ttu-id="14b3b-104">Ruft den Klassennamen und andere Informationen ab, die einer angegebenen GUID im Manifest einer Komponente zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="14b3b-104">Retrieves the class name and other information associated with a given GUID in a component's manifest.</span></span> <span data-ttu-id="14b3b-105">Diese Funktion wird nur verwendet, wenn die verwaltete, nicht verwaltete Interoperabilität auf niedriger Ebene in der .NET Framework implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-105">This function is used only when implementing low-level managed-unmanaged interoperability in the .NET Framework.</span></span> <span data-ttu-id="14b3b-106">Weitere Informationen zur verwalteten, nicht verwalteten Interoperabilität finden Sie unter "Interoperabilität mit nicht verwaltetem Code" im .NET Framework SDK und auch in [isolierten Anwendungen und](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="14b3b-106">For more information about managed-unmanaged interoperability, see "Interoperating with Unmanaged Code" in the .NET Framework SDK and also [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="14b3b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14b3b-107">Syntax</span></span>


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="14b3b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="14b3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b3b-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14b3b-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b3b-110">Eine Kombination aus null oder mehr der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="14b3b-110">A combination of zero or more of the following flags.</span></span>



| <span data-ttu-id="14b3b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="14b3b-111">Value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="14b3b-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="14b3b-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <span data-ttu-id="14b3b-113"><dt>**SxS \_ Die \_ CLR- \_ GUID für die Suche \_ verwendet \_ ActCtx**</dt> <dt>0x00000001</dt> .</span><span class="sxs-lookup"><span data-stu-id="14b3b-113"><dt>**SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX**</dt> <dt>0x00000001</dt></span></span> </dl>              | <span data-ttu-id="14b3b-114">Wenn dieses Flag festgelegt ist, muss der Parameter " *hactctx* " ein Aktivierungs Kontext Handle enthalten, das von der Funktion " [**deateactctx**](/windows/win32/api/winbase/nf-winbase-createactctxa) " zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-114">If this flag is set, then the *hActCtx* parameter must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="14b3b-115">Wenn dieses Flag nicht festgelegt ist, wird der Parameter " *hactctx* " ignoriert, und " **sxslookupclrguid** " durchsucht den derzeit aktiven Aktivierungs Kontext (die [**activateactctx**](/windows/win32/api/winbase/nf-winbase-activateactctx) -Funktion wird verwendet, um einen Aktivierungs Kontext aktiv zu machen).</span><span class="sxs-lookup"><span data-stu-id="14b3b-115">If this flag is not set, the *hActCtx* parameter is ignored and **SxsLookupClrGuid** searches the activation context that is currently active (the [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) function is used to make an activation context active).</span></span><br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <span data-ttu-id="14b3b-116"><dt>**SxS \_ Nachschlagen der \_ CLR- \_ GUID \_ Find \_ Ersatz**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="14b3b-116"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE**</dt> <dt>0x00010000</dt></span></span> </dl>  | <span data-ttu-id="14b3b-117">Wenn dieses Flag festgelegt ist, sucht **sxslookupclrguid** nach einem Ersatz Zeichen.</span><span class="sxs-lookup"><span data-stu-id="14b3b-117">If this flag is set, **SxsLookupClrGuid** searches for a surrogate.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <span data-ttu-id="14b3b-118"><dt>**SxS \_ \_CLR- \_ GUID \_ Suchen \_ CLR- \_ Klasse**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="14b3b-118"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="14b3b-119">Wenn dieses Flag festgelegt ist, sucht **sxslookupclrguid** nach einer Klasse.</span><span class="sxs-lookup"><span data-stu-id="14b3b-119">If this flag is set, **SxsLookupClrGuid** searches for a class.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <span data-ttu-id="14b3b-120"><dt>**SxS \_ Nachschlagen der \_ CLR- \_ GUID \_ finden Sie \_ beliebige**</dt> <dt>0x00030000</dt></span><span class="sxs-lookup"><span data-stu-id="14b3b-120"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_ANY**</dt> <dt>0x00030000</dt></span></span> </dl>                    | <span data-ttu-id="14b3b-121">Dabei handelt es sich um eine Kombination der **SxS-Lookup-CLR- \_ \_ \_ GUID \_ Find \_ Ersatz** und **SxS \_ Lookup \_ CLR \_ GUID \_ finden Sie \_ CLR- \_ klassenflags** . wenn beide festgelegt sind, sucht **sxslookupclrguid** zuerst nach einem Ersatz Zeichen und nur dann, wenn Sie eine Klasse finden.</span><span class="sxs-lookup"><span data-stu-id="14b3b-121">This is a combination of the **SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE** and **SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS** flags; if both are set, **SxsLookupClrGuid** searches for a surrogate first, and only if it does not find one, then searches for a class.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="14b3b-122">*pclsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14b3b-122">*pClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b3b-123">Ein Zeiger auf die GUID, über die im Aktivierungs Kontext nach Interoperation-Informationen gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="14b3b-123">A pointer to the GUID about which to search the activation context for interoperation information.</span></span> <span data-ttu-id="14b3b-124">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="14b3b-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14b3b-125">*hactctx* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="14b3b-125">*hActCtx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14b3b-126">Wenn die **SxS-Lookup-CLR- \_ \_ \_ GUID das \_ \_ ActCtx** -Flag verwenden im *dwFlags* -Parameter festgelegt ist, muss " *hactctx* " ein Aktivierungs Kontext Handle enthalten, das von der Funktion " [**deateactctx**](/windows/win32/api/winbase/nf-winbase-createactctxa) " zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-126">If the **SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX** flag is set in the *dwFlags* parameter, then *hActCtx* must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="14b3b-127">Andernfalls wird " *hactctx* " ignoriert.</span><span class="sxs-lookup"><span data-stu-id="14b3b-127">Otherwise, *hActCtx* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="14b3b-128">*pvoutputbuffer* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="14b3b-128">*pvOutputBuffer* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14b3b-129">Zeiger auf den Puffer, in den Rückgabe Informationen kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="14b3b-129">Pointer to the buffer into which return information is copied.</span></span> <span data-ttu-id="14b3b-130">Dieser Parameter kann nur dann NULL-Wert sein, wenn der *cboutputbuffer* -Parameter den Wert NULL hat.</span><span class="sxs-lookup"><span data-stu-id="14b3b-130">This parameter may be NULL-valued only if the *cbOutputBuffer* parameter is zero-valued.</span></span> <span data-ttu-id="14b3b-131">Die Daten, die in diesem Puffer beim Beenden platziert werden (falls vorhanden), bestehen aus einer **SxS- \_ GUID- \_ Informations \_** Struktur, gefolgt von zusätzlichen Zeichen folgen Daten, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="14b3b-131">The data placed in this buffer on exit (if any) consists of a **SXS\_GUID\_INFORMATION\_CLR** structure followed by any additional string data required.</span></span> <span data-ttu-id="14b3b-132">Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.</span><span class="sxs-lookup"><span data-stu-id="14b3b-132">See the Remarks section below for more information.</span></span>

</dd> <dt>

<span data-ttu-id="14b3b-133">*cboutputbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14b3b-133">*cbOutputBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b3b-134">Größe des Puffers in Byte, auf den durch den *pvoutputbuffer* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-134">Size in bytes of the buffer pointed to by the *pvOutputBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="14b3b-135">*pcboutputbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="14b3b-135">*pcbOutputBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14b3b-136">Ein Zeiger auf eine Variable, bei der die Größe (in Bytes) der Rückgabe Informationen beim Beenden platziert wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-136">Pointer to a variable where the size, in bytes, of the return information is placed on exit.</span></span> <span data-ttu-id="14b3b-137">Wenn der *cboutputbuffer* -Parameter 0 (null) ist, oder wenn die Größe des Ausgabepuffers kleiner ist als die Größe der Rückgabe Informationen, schlägt **sxslookupclrguid** fehl, und [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen Fehler aufgrund eines **\_ nicht ausreichenden \_ Puffers** zurück.</span><span class="sxs-lookup"><span data-stu-id="14b3b-137">If the *cbOutputBuffer* parameter is zero, or if the size of the output buffer is smaller than the size of the return information, then **SxsLookupClrGuid** fails and [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns an error of **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="14b3b-138">Verwenden Sie in diesem Fall den Wert in der Variablen, auf die von *pcboutputbuffer* verwiesen wird, um einen ausreichend großen Puffer zuzuordnen, und rufen Sie dann erneut **sxslookupclrguid** auf, um die gewünschten Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14b3b-138">In this case, use the value in the variable pointed to by *pcbOutputBuffer* to allocate a large enough buffer, and then call **SxsLookupClrGuid** again to retrieve the desired information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b3b-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14b3b-139">Return value</span></span>

<span data-ttu-id="14b3b-140">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="14b3b-140">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="14b3b-141">Weitere Fehlerinformationen erhalten Sie, wenn Sie [ **GetLastError** aufrufen.](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="14b3b-141">For more error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>

## <a name="remarks"></a><span data-ttu-id="14b3b-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14b3b-142">Remarks</span></span>

<span data-ttu-id="14b3b-143">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14b3b-143">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="14b3b-144">Verwaltete Komponenten können sich selbst als Unterstützung verwalteter "Interop-Assemblys" deklarieren, damit ein nicht verwalteter Win32-Komponentenconsumer auf die deklarierende Assembly verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="14b3b-144">Managed components may declare themselves as supporting managed "interop assemblies" so as to allow an unmanaged Win32 component consumer to reference the declaring assembly.</span></span> <span data-ttu-id="14b3b-145">Der Komponenten Consumer kann mit der verwalteten Komponente interagieren, indem [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für eine GUID aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-145">The component consumer can interact with the managed component by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on a GUID.</span></span> <span data-ttu-id="14b3b-146">Die Interoperation-Ebene leitet die Objekt Erstellungs Anforderung an .NET Framework weiter, erstellt eine Instanz des verwalteten Objekts und gibt einen Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="14b3b-146">The interoperation layer routes the object creation request to .NET Framework, creates an instance of the managed object, and returns an interface pointer.</span></span>

<span data-ttu-id="14b3b-147">**Sxslookupclrguid** ermöglicht den Frameworks das Abrufen von Informationen, die einer bestimmten GUID im Manifest der Komponente zugeordnet sind, z. b. den Namen der .NET-Klasse, die erforderliche Version der .NET Framework und die Hostassembly, in der Sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="14b3b-147">**SxsLookupClrGuid** allows the frameworks to retrieve information associated with a given GUID in the component's manifest, such as what its .NET class name is, what version of the .NET Framework it requires, and what host assembly it is located in.</span></span> <span data-ttu-id="14b3b-148">Verwaltete Komponenten veröffentlichen eine Interop-Assembly, die eine Reihe von Anweisungen enthält, die GUIDs mit Assemblynamen und Typnamen verknüpfen, und die .NET-Runtime brottet die Konstruktion verwalteter Objektinstanzen, wenn [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-148">Managed components publish an interop assembly that contains a number of statements associating GUIDs with assembly and type names, and the .NET runtime brokers the construction of managed object instances when [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is called.</span></span>

<span data-ttu-id="14b3b-149">Im folgenden finden Sie ein Beispiel für ein Komponenten Manifest, das eine CLR-GUID und ein CLR-Ersatz Zeichen deklariert, das **sxslookupclrguid** suchen kann:</span><span class="sxs-lookup"><span data-stu-id="14b3b-149">The following is a sample component manifest declaring a CLR GUID and a CLR surrogate that **SxsLookupClrGuid** can look up:</span></span>

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

<span data-ttu-id="14b3b-150">Ein Interoperation-Anbieter ruft **sxslookupclrguid** mit einem Zeiger auf die GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" auf. und erhalten in Rückgabe den Klassennamen "mysampleersatz", die erforderliche Laufzeitversion "1.0.3055" und die Text Identität "dotnet. Sample. Surrogates, Version = ' 1.0.0.0 ', Type = ' Interop '" der Hostingkomponente.</span><span class="sxs-lookup"><span data-stu-id="14b3b-150">An interoperation provider would call **SxsLookupClrGuid** with a pointer to the GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", and would receive in return the class name "MySampleSurrogate", the required runtime version "1.0.3055", and the textual identity "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" of the hosting component.</span></span>

<span data-ttu-id="14b3b-151">Diese Rückgabe Informationen sind enthalten und/oder referenziert durch eine **SxS- \_ GUID- \_ Informations- \_ CLR** -Struktur, die wie folgt deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-151">This return information would be contained and/or referenced by a **SXS\_GUID\_INFORMATION\_CLR** structure declared as follows.</span></span>

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

<span data-ttu-id="14b3b-152">Die Elemente dieser Struktur enthalten die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="14b3b-152">The members of this structure contain the following information.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14b3b-153">Member</span><span class="sxs-lookup"><span data-stu-id="14b3b-153">Member</span></span></th>
<th><span data-ttu-id="14b3b-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14b3b-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="14b3b-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>CBSIZE</strong></span><span class="sxs-lookup"><span data-stu-id="14b3b-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span></span><br/></td>
<td><span data-ttu-id="14b3b-156">Enthält die Größe der SXS_GUID_INFORMATION_CLR Struktur (Dadurch kann die-Struktur in späteren Versionen vergrößert werden).</span><span class="sxs-lookup"><span data-stu-id="14b3b-156">Contains the size of the SXS_GUID_INFORMATION_CLR structure (this allows the structure to grow in later versions).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14b3b-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span><span class="sxs-lookup"><span data-stu-id="14b3b-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span></span><br/></td>
<td><span data-ttu-id="14b3b-158">Enthält einen der folgenden zwei Flagwerte:</span><span class="sxs-lookup"><span data-stu-id="14b3b-158">Contains one of the following two flag values:</span></span> <br/>
<ul>
<li><span data-ttu-id="14b3b-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): gibt an, dass die angegebene GUID einem Ersatz Zeichen zugeordnet wurde &quot; .&quot;</span><span class="sxs-lookup"><span data-stu-id="14b3b-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Indicates that the specified GUID was associated with a &quot;surrogate.&quot;</span></span></li>
<li><span data-ttu-id="14b3b-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): gibt an, dass die angegebene GUID einer Klasse zugeordnet wurde &quot; .&quot;</span><span class="sxs-lookup"><span data-stu-id="14b3b-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Indicates that the specified GUID was associated with a &quot;class.&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14b3b-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszruntimeversion</strong></span><span class="sxs-lookup"><span data-stu-id="14b3b-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span></span><br/></td>
<td><span data-ttu-id="14b3b-162">Verweist auf eine NULL terminierte breit Zeichen-Zeichenfolge, die die Version der Laufzeit identifiziert, die im Host Manifest für diese Klasse angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="14b3b-162">Points to a zero-terminated wide-character string that identifies the version of the runtime specified in the host manifest for this class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14b3b-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwsztypame</strong></span><span class="sxs-lookup"><span data-stu-id="14b3b-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span></span><br/></td>
<td><span data-ttu-id="14b3b-164">Verweist auf eine NULL terminierte breit Zeichen-Zeichenfolge, die den Namen der .NET-Klasse enthält, die der angegebenen GUID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="14b3b-164">Points to a zero-terminated wide-character string that contains the name of the .NET class associated with the specified GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14b3b-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszassemblyidentity</strong></span><span class="sxs-lookup"><span data-stu-id="14b3b-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span></span><br/></td>
<td><span data-ttu-id="14b3b-166">Verweist auf eine NULL terminierte breit Zeichen-Zeichenfolge, die die Text Identität der Assembly enthält, die diese Klasse hostet.</span><span class="sxs-lookup"><span data-stu-id="14b3b-166">Points to a zero-terminated wide-character string that contains the textual identity of the assembly that hosts this class.</span></span> <span data-ttu-id="14b3b-167">Weitere Informationen zur Text Identität finden Sie &quot; unter Angeben von voll qualifizierten Typnamen unter "ermitteln &quot; &quot; von Typinformationen zur Laufzeit" &quot; unter &quot; Programmieren mit der .NET Framework &quot; im .NET Framework SDK.</span><span class="sxs-lookup"><span data-stu-id="14b3b-167">For more information about textual identity, see &quot;Specifying Fully Qualified Type Names&quot; under &quot;Discovering Type Information at Run Time&quot; under &quot;Programming with the .NET Framework&quot; in the .NET Framework SDK.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="14b3b-168">Eine nicht verwaltete Anwendung kann die auf diese Weise zurückgegebenen Informationen verwenden, um die richtige Version des .NET Framework zu laden, die Assembly zu laden, die durch das **pcwszassemblyidentity** -Element identifiziert wird, und dann eine Instanz der Klasse zu erstellen, die durch das **pcwsztywatame** -Element benannt wird.</span><span class="sxs-lookup"><span data-stu-id="14b3b-168">An unmanaged application can use the information returned in this fashion to load the right version of the .NET Framework, load the assembly identified by the **pcwszAssemblyIdentity** element, and then create an instance of the class named by the **pcwszTypeName** element.</span></span>

## <a name="examples"></a><span data-ttu-id="14b3b-169">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14b3b-169">Examples</span></span>

<span data-ttu-id="14b3b-170">Verwenden Sie das dynamische verknüpfen wie folgt, um die **sxslookupclrguid** -Funktion aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="14b3b-170">Use dynamic linking as follows to call the **SxsLookupClrGuid** function:</span></span>


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a><span data-ttu-id="14b3b-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14b3b-171">Requirements</span></span>



| <span data-ttu-id="14b3b-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14b3b-172">Requirement</span></span> | <span data-ttu-id="14b3b-173">Wert</span><span class="sxs-lookup"><span data-stu-id="14b3b-173">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b3b-174">DLL</span><span class="sxs-lookup"><span data-stu-id="14b3b-174">DLL</span></span><br/> | <dl> <span data-ttu-id="14b3b-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b3b-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b3b-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14b3b-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b3b-177">Isolierte Anwendungen und parallele Assemblys</span><span class="sxs-lookup"><span data-stu-id="14b3b-177">Isolated Applications and Side-by-side Assemblies</span></span>](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[<span data-ttu-id="14b3b-178">**"Kreateactctx"**</span><span class="sxs-lookup"><span data-stu-id="14b3b-178">**CreateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[<span data-ttu-id="14b3b-179">**Activateactctx**</span><span class="sxs-lookup"><span data-stu-id="14b3b-179">**ActivateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[<span data-ttu-id="14b3b-180">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="14b3b-180">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
