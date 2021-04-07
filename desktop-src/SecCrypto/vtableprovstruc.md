---
description: Enthält Zeiger auf Rückruf Funktionen, die von den Funktionen des Kryptografiedienstanbieters (CSP) verwendet werden können.
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Vtableprovstruc-Struktur (cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759457"
---
# <a name="vtableprovstruc-structure"></a><span data-ttu-id="8dac4-103">Vtableprovstruc-Struktur</span><span class="sxs-lookup"><span data-stu-id="8dac4-103">VTableProvStruc structure</span></span>

<span data-ttu-id="8dac4-104">Die **vtableprovstruc** -Struktur enthält Zeiger auf Rückruf Funktionen, die von den Funktionen des [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8dac4-104">The **VTableProvStruc** structure contains pointers to callback functions that can be used by [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dac4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dac4-105">Syntax</span></span>


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a><span data-ttu-id="8dac4-106">Member</span><span class="sxs-lookup"><span data-stu-id="8dac4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8dac4-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="8dac4-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="8dac4-108">Ein **DWORD** -Wert, der die Version der-Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="8dac4-108">A **DWORD** value that indicates the version of the structure.</span></span> <span data-ttu-id="8dac4-109">Drei Versionen dieser Struktur werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="8dac4-109">Three versions of this structure are used.</span></span> <span data-ttu-id="8dac4-110">Die Versionen sind 1, 2 und 3 und legen fest, welche Member der Struktur gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8dac4-110">The versions are number 1, 2, and 3, and determine which members of the structure are valid.</span></span> <span data-ttu-id="8dac4-111">Member der Version 1 sind auf allen Systemen gültig, die diese Struktur unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8dac4-111">Version 1 members are valid on all systems that support this structure.</span></span>

<span data-ttu-id="8dac4-112">Dabei handelt es sich um ein Mitglied der Version 1.</span><span class="sxs-lookup"><span data-stu-id="8dac4-112">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="8dac4-113">**Funcverifyimage**</span><span class="sxs-lookup"><span data-stu-id="8dac4-113">**FuncVerifyImage**</span></span>
</dt> <dd>

<span data-ttu-id="8dac4-114">Die Adresse einer [**funkverifyimage**](funcverifyimage.md) -Rückruffunktion, die der CSP verwendet, um die Signatur aller DLLs zu überprüfen, die vom CSP geladen werden.</span><span class="sxs-lookup"><span data-stu-id="8dac4-114">The address of a [**FuncVerifyImage**](funcverifyimage.md) callback function that the CSP uses to verify the signature of any DLLs that the CSP will load.</span></span> <span data-ttu-id="8dac4-115">Alle Erweiterungs-DLLs, in die ein CSP Funktionsaufrufe durchführt, müssen auf die gleiche Weise (und mit demselben Schlüssel) wie die primäre CSP-DLL signiert werden.</span><span class="sxs-lookup"><span data-stu-id="8dac4-115">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="8dac4-116">Um diese Signatur sicherzustellen, müssen die zusätzlichen DLLs dynamisch mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion geladen werden.</span><span class="sxs-lookup"><span data-stu-id="8dac4-116">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="8dac4-117">Aber bevor die dll geladen wird, muss die Signatur der dll überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="8dac4-117">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="8dac4-118">Der CSP führt diese Überprüfung durch Aufrufen der Funktion **funcverifyimage** aus, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8dac4-118">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

<span data-ttu-id="8dac4-119">Dieser Funktionszeiger kann gespeichert und verwendet werden, bis der CSP-kontextfrei gegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8dac4-119">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="8dac4-120">Dabei handelt es sich um ein Mitglied der Version 1.</span><span class="sxs-lookup"><span data-stu-id="8dac4-120">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="8dac4-121">**Funkreturnhwnd**</span><span class="sxs-lookup"><span data-stu-id="8dac4-121">**FuncReturnhWnd**</span></span>
</dt> <dd>

<span data-ttu-id="8dac4-122">Die Adresse einer [**funkreturnhwnd**](funcreturnhwnd.md) -Rückruffunktion, die das Fenster Handle zurückgibt, das der CSP als übergeordnetes Element oder Besitzer einer beliebigen angezeigten Benutzeroberfläche verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="8dac4-122">The address of a [**FuncReturnhWnd**](funcreturnhwnd.md) callback function that returns the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span> <span data-ttu-id="8dac4-123">CSPs, die nicht direkt mit dem Benutzer und CSPs kommunizieren, die für diesen Zweck dedizierte Hardware verwenden, können diesen Eintrag ignorieren.</span><span class="sxs-lookup"><span data-stu-id="8dac4-123">CSPs that do not communicate directly with the user and CSPs that use dedicated hardware for this purpose can ignore this entry.</span></span> <span data-ttu-id="8dac4-124">Dieses Fenster Handle ist standardmäßig auf 0 festgelegt, aber eine Anwendung kann diese auf einen anderen Wert festlegen, indem die Funktion " [**cryptsetprovparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) " zum Festlegen der Eigenschaft " **PP-Client- \_ \_ HWND** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8dac4-124">This window handle is zero by default, but an application can set this to a different value by using the [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) function to set the **PP\_CLIENT\_HWND** property.</span></span>

<span data-ttu-id="8dac4-125">Dieser Funktionszeiger kann gespeichert und verwendet werden, bis der CSP-kontextfrei gegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8dac4-125">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="8dac4-126">Dabei handelt es sich um ein Mitglied der Version 1.</span><span class="sxs-lookup"><span data-stu-id="8dac4-126">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="8dac4-127">**dwprovtype**</span><span class="sxs-lookup"><span data-stu-id="8dac4-127">**dwProvType**</span></span>
</dt> <dd>

<span data-ttu-id="8dac4-128">Ein **DWORD** -Wert, der den Typ des abzurufenden Anbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="8dac4-128">A **DWORD** value that specifies the type of provider to acquire.</span></span> <span data-ttu-id="8dac4-129">Die folgenden [*Anbieter Typen*](../secgloss/p-gly.md) sind vordefiniert und werden in der [CSP-Interoperabilität](https://www.bing.com/search?q=CSP+Interoperability)ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="8dac4-129">The following [*provider types*](../secgloss/p-gly.md) are predefined and are discussed in detail in [CSP Interoperability](https://www.bing.com/search?q=CSP+Interoperability):</span></span>

-   <span data-ttu-id="8dac4-130">Prov \_ RSA \_ Full</span><span class="sxs-lookup"><span data-stu-id="8dac4-130">PROV\_RSA\_FULL</span></span>
-   <span data-ttu-id="8dac4-131">Prov \_ RSA \_ sig</span><span class="sxs-lookup"><span data-stu-id="8dac4-131">PROV\_RSA\_SIG</span></span>
-   <span data-ttu-id="8dac4-132">Prov- \_ DSS</span><span class="sxs-lookup"><span data-stu-id="8dac4-132">PROV\_DSS</span></span>
-   <span data-ttu-id="8dac4-133">Prov- \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="8dac4-133">PROV\_FORTEZZA</span></span>
-   <span data-ttu-id="8dac4-134">Prov \_ MS \_ Exchange</span><span class="sxs-lookup"><span data-stu-id="8dac4-134">PROV\_MS\_EXCHANGE</span></span>

<span data-ttu-id="8dac4-135">Dabei handelt es sich um ein Mitglied der Version 2.</span><span class="sxs-lookup"><span data-stu-id="8dac4-135">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="8dac4-136">**pbcontextinfo**</span><span class="sxs-lookup"><span data-stu-id="8dac4-136">**pbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8dac4-137">Ein Zeiger auf ein Array von Kontextinformationen.</span><span class="sxs-lookup"><span data-stu-id="8dac4-137">A pointer to an array of context information.</span></span> <span data-ttu-id="8dac4-138">Die Member " **pbcontextinfo** " und " **cbcontextinfo** " bestimmen zusammen den verwendeten Informations Satz, wenn eine [**cpsetprovparam**](https://www.bing.com/search?q=**CPSetProvParam**) -Funktion mit \_ \_ festgelegtem PP-Kontext Info Satz aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8dac4-138">The **pbContextInfo** and **cbContextInfo** members together determine the information set used when a [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) function is called with PP\_CONTEXT\_INFO set.</span></span>

<span data-ttu-id="8dac4-139">Dabei handelt es sich um ein Mitglied der Version 2.</span><span class="sxs-lookup"><span data-stu-id="8dac4-139">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="8dac4-140">**cbcontextinfo**</span><span class="sxs-lookup"><span data-stu-id="8dac4-140">**cbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8dac4-141">Ein **DWORD** -Wert, der die Anzahl der Elemente im **pbcontextinfo** -Array angibt.</span><span class="sxs-lookup"><span data-stu-id="8dac4-141">A **DWORD** value that indicates the number of elements in the **pbContextInfo** array.</span></span>

<span data-ttu-id="8dac4-142">Dabei handelt es sich um ein Mitglied der Version 2.</span><span class="sxs-lookup"><span data-stu-id="8dac4-142">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="8dac4-143">**pszprovname**</span><span class="sxs-lookup"><span data-stu-id="8dac4-143">**pszProvName**</span></span>
</dt> <dd>

<span data-ttu-id="8dac4-144">Eine Zeichenfolge, die den Namen des Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="8dac4-144">A string that contains the name of the provider.</span></span>

<span data-ttu-id="8dac4-145">Dabei handelt es sich um ein Mitglied der Version 3.</span><span class="sxs-lookup"><span data-stu-id="8dac4-145">This is a version 3 member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dac4-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8dac4-146">Remarks</span></span>

<span data-ttu-id="8dac4-147">Die Zeiger in der **vtableprovstruc** -Struktur sind nur innerhalb der [**cpacquirecontext**](https://www.bing.com/search?q=**CPAcquireContext**) -Funktion verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8dac4-147">The pointers in the **VTableProvStruc** structure are only available within the [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) function.</span></span> <span data-ttu-id="8dac4-148">Wenn Elemente der Struktur nach Abschluss eines Aufrufes von **cpacquirecontext** benötigt werden, müssen vom CSP Kopien der benötigten Strukturelemente erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8dac4-148">If members of the structure are needed after a call to **CPAcquireContext** is completed, copies of the needed structure elements must be made by the CSP.</span></span> <span data-ttu-id="8dac4-149">Die Funktionszeiger in dieser Struktur können gespeichert und verwendet werden, bis der CSP-kontextfrei gegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8dac4-149">The function pointers in this structure can be stored and used until the CSP context is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dac4-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dac4-150">Requirements</span></span>



| <span data-ttu-id="8dac4-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8dac4-151">Requirement</span></span> | <span data-ttu-id="8dac4-152">Wert</span><span class="sxs-lookup"><span data-stu-id="8dac4-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8dac4-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8dac4-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8dac4-154">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8dac4-154">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8dac4-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8dac4-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8dac4-156">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8dac4-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8dac4-157">Header</span><span class="sxs-lookup"><span data-stu-id="8dac4-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dac4-158"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dac4-158"><dt>Cspdk.h</dt></span></span> </dl> |
| <span data-ttu-id="8dac4-159">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="8dac4-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8dac4-160">**Vtableprovstrucw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="8dac4-160">**VTableProvStrucW** (Unicode)</span></span><br/>                                          |



 

 
