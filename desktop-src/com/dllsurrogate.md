---
title: Dllersatz
description: Ermöglicht das Ausführen von DLL-Servern in einem Ersatz Vorgang. Wenn eine leere Zeichenfolge angegeben wird, wird das vom System bereitgestellte Ersatz Zeichen verwendet. Andernfalls gibt der Wert den Pfad des zu verwendenden Ersatz Zeichens an.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- Dllersatz-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391062"
---
# <a name="dllsurrogate"></a><span data-ttu-id="e9c87-105">Dllersatz</span><span class="sxs-lookup"><span data-stu-id="e9c87-105">DllSurrogate</span></span>

<span data-ttu-id="e9c87-106">Ermöglicht das Ausführen von DLL-Servern in einem Ersatz Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e9c87-106">Enables DLL servers to run in a surrogate process.</span></span> <span data-ttu-id="e9c87-107">Wenn eine leere Zeichenfolge angegeben wird, wird das vom System bereitgestellte Ersatz Zeichen verwendet. Andernfalls gibt der Wert den Pfad des zu verwendenden Ersatz Zeichens an.</span><span class="sxs-lookup"><span data-stu-id="e9c87-107">If an empty string is specified, the system-supplied surrogate is used; otherwise, the value specifies the path of the surrogate to be used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e9c87-108">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="e9c87-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a><span data-ttu-id="e9c87-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9c87-109">Remarks</span></span>

<span data-ttu-id="e9c87-110">Dies ist ein **reg \_ SZ** -Wert, der angibt, dass es sich bei der Klasse um eine DLL handelt, die in einem Ersatzprozess aktiviert werden soll, und um den zu verwendenden Ersatzprozess zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9c87-110">This is a **REG\_SZ** value that specifies that the class is a DLL that is to be activated in a surrogate process, and the surrogate process to be used.</span></span> <span data-ttu-id="e9c87-111">Legen Sie den *Pfad* auf eine leere Zeichenfolge oder auf **null** fest, um den vom System bereitgestellten generischen Ersatzprozess zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9c87-111">To use the system-supplied generic surrogate process, set *path* to an empty string or **NULL**.</span></span> <span data-ttu-id="e9c87-112">Wenn Sie einen anderen Ersatzprozess angeben möchten, legen Sie den *Pfad* auf den Pfad des Ersatz Zeichens fest.</span><span class="sxs-lookup"><span data-stu-id="e9c87-112">To specify another surrogate process, set *path* to the path of the surrogate.</span></span> <span data-ttu-id="e9c87-113">Wie in der Angabe des Pfads eines Servers unter dem Schlüssel [**LocalServer32**](localserver32.md) ist eine vollständige Pfadspezifikation nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e9c87-113">As in the specification of the path of a server under the [**LocalServer32**](localserver32.md) key, a full path specification is not necessary.</span></span> <span data-ttu-id="e9c87-114">Das Ersatz Zeichen muss geschrieben werden, um ordnungsgemäß mit dem DCOM-Dienst zu kommunizieren, wie in [Schreiben eines benutzerdefinierten Ersatz](writing-a-custom-surrogate.md)Zeichens beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e9c87-114">The surrogate must be written to properly communicate with the DCOM service as described in [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

<span data-ttu-id="e9c87-115">Der **dllersatz** -Wert muss vorhanden sein, damit ein dll-Server in einem Ersatz Zeichen aktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e9c87-115">The **DllSurrogate** value must be present for a DLL server to be activated in a surrogate.</span></span> <span data-ttu-id="e9c87-116">Die Aktivierung bezieht sich auf einen Aufrufen von " [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)", " [**cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)", " **cokreateinstanceex**", " [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)", " [**cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)" oder " [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)".</span><span class="sxs-lookup"><span data-stu-id="e9c87-116">Activation refers to a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage), or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="e9c87-117">Das Ausführen von DLLs in einem Ersatzprozess bietet die Vorteile einer ausführbaren Implementierung, einschließlich der Fehler Isolation, der Möglichkeit, mehrere Clients gleichzeitig zu bedienen, und ermöglicht es dem Server, Dienste für Remote Clients in einer verteilten Umgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e9c87-117">Running DLLs in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9c87-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9c87-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9c87-119">**Coregisterersatz**</span><span class="sxs-lookup"><span data-stu-id="e9c87-119">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="e9c87-120">DLL-Surrogates</span><span class="sxs-lookup"><span data-stu-id="e9c87-120">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="e9c87-121">**Dllsurrogateausführ Bare Datei**</span><span class="sxs-lookup"><span data-stu-id="e9c87-121">**DllSurrogateExecutable**</span></span>](dllsurrogateexecutable.md)
</dt> <dt>

[<span data-ttu-id="e9c87-122">**Isurrogate**</span><span class="sxs-lookup"><span data-stu-id="e9c87-122">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 