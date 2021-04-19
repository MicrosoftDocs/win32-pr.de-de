---
title: Dllsurrogateausführ Bare Datei
description: Ermöglicht das Ausführen von DLL-Servern in einem benutzerdefinierten Ersatzprozess in Verbindung mit dem Registrierungs Wert dllersatz. Wenn dllsurrogateexe nicht angegeben wird, übergibt com den Wert NULL als Wert für den ersten Parameter der Funktion "deateprocess".
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Dllsurrogateausführ barer Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338498"
---
# <a name="dllsurrogateexecutable"></a><span data-ttu-id="c400a-105">Dllsurrogateausführ Bare Datei</span><span class="sxs-lookup"><span data-stu-id="c400a-105">DllSurrogateExecutable</span></span>

<span data-ttu-id="c400a-106">Ermöglicht das Ausführen von DLL-Servern in einem benutzerdefinierten Ersatzprozess in Verbindung mit dem Registrierungs Wert [**dllersatz**](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="c400a-106">Enables DLL servers to run in a custom surrogate process, in conjunction with the [**DllSurrogate**](dllsurrogate.md) registry value.</span></span> <span data-ttu-id="c400a-107">Wenn **dllsurrogateexe** nicht angegeben wird, übergibt com den Wert **null** als Wert für den ersten Parameter der Funktion " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ".</span><span class="sxs-lookup"><span data-stu-id="c400a-107">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c400a-108">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="c400a-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a><span data-ttu-id="c400a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c400a-109">Remarks</span></span>

<span data-ttu-id="c400a-110">Dieser Wert ist vom Typ **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="c400a-110">This value is of type **REG\_SZ**.</span></span> <span data-ttu-id="c400a-111">Dies funktioniert in Verbindung mit dem [**dllersatz**](dllsurrogate.md) -Wert, um Mehrdeutigkeit bei Verwendung [**der Funktion "**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Funktion" zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c400a-111">It works in conjunction with the [**DllSurrogate**](dllsurrogate.md) value to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="c400a-112">**Dllersatz** gibt an, ob ein benutzerdefiniertes Ersatz Zeichen verwendet werden muss. diese Informationen werden als erster Parameter für " **kreateprocess**" übergeben.</span><span class="sxs-lookup"><span data-stu-id="c400a-112">**DllSurrogate** indicates whether a custom surrogate needs to be used, and this information is passed as the first parameter for **CreateProcess**.</span></span> <span data-ttu-id="c400a-113">Abhängig von der Implementierung von " **kreateprocess**" sind diese Informationen möglicherweise mehrdeutig.</span><span class="sxs-lookup"><span data-stu-id="c400a-113">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="c400a-114">Wenn **dllsurrogateexe** angegeben wird, übergibt com den Wert als ersten Parameter von " **kreateprocess**".</span><span class="sxs-lookup"><span data-stu-id="c400a-114">If **DllSurrogateExecutable** is specified, COM passes the value as the first parameter of **CreateProcess**.</span></span> <span data-ttu-id="c400a-115">Wenn **dllsurrogateexe** nicht angegeben wird, übergibt com den Wert **null** als Wert für den ersten Parameter von " **kreateprocess**".</span><span class="sxs-lookup"><span data-stu-id="c400a-115">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c400a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c400a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c400a-117">**Coregisterersatz**</span><span class="sxs-lookup"><span data-stu-id="c400a-117">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="c400a-118">DLL-Surrogates</span><span class="sxs-lookup"><span data-stu-id="c400a-118">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="c400a-119">**Dllersatz**</span><span class="sxs-lookup"><span data-stu-id="c400a-119">**DllSurrogate**</span></span>](dllsurrogate.md)
</dt> <dt>

[<span data-ttu-id="c400a-120">**Isurrogate**</span><span class="sxs-lookup"><span data-stu-id="c400a-120">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 