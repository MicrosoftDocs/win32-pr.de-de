---
title: Activateatstorage
description: Konfiguriert den Client für die instanzialisierung von Objekten auf dem gleichen Computer wie der persistente Zustand, den Sie verwenden oder von dem Sie initialisiert werden.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039696"
---
# <a name="activateatstorage"></a><span data-ttu-id="c4b1b-104">Activateatstorage</span><span class="sxs-lookup"><span data-stu-id="c4b1b-104">ActivateAtStorage</span></span>

<span data-ttu-id="c4b1b-105">Konfiguriert den Client für die instanzialisierung von Objekten auf dem gleichen Computer wie der persistente Zustand, den Sie verwenden oder von dem Sie initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-105">Configures the client to instantiate objects on the same computer as the persistent state they are using or from which they are initialized.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c4b1b-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="c4b1b-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a><span data-ttu-id="c4b1b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4b1b-107">Remarks</span></span>

<span data-ttu-id="c4b1b-108">Dies ist ein **reg \_ SZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="c4b1b-109">Jeder Wert, der mit "y" oder "y" beginnt, gibt an, dass **activateatstorage** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-109">Any value that begins with 'Y' or 'y' indicates that **ActivateAtStorage** should be used.</span></span>

<span data-ttu-id="c4b1b-110">Die **activateatstorage** -Funktion bietet eine transparente Möglichkeit, um Clients das Auffinden von laufenden Objekten auf dem gleichen Computer wie die Daten zu ermöglichen, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-110">The **ActivateAtStorage** capability provides a transparent way to allow clients to locate running objects on the same computer as the data that they use.</span></span> <span data-ttu-id="c4b1b-111">Dadurch wird der Netzwerkverkehr reduziert, da das Objekt anstelle von Aufrufen über das Netzwerk lokale Dateisystem Aufrufe ausführt.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-111">This reduces network traffic because the object performs local file-system calls instead of calls across the network.</span></span>

<span data-ttu-id="c4b1b-112">Wenn ein Wert für **activateatstorage** festgelegt wird, wird dies zum Standardverhalten bei Aufrufen der Funktionen [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) und [**cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) sowie für die Datei-monikerimplementierung von [**IMoniker:: BindTo Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="c4b1b-112">When a value is set for **ActivateAtStorage**, this becomes the default behavior in calls to the [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) and [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) functions, as well as to the file moniker implementation of [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="c4b1b-113">Bei allen diesen Aufrufen überschreibt die Angabe einer [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur die Einstellung von **activateatstorage** für die Dauer des Funktionsaufrufs.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-113">In all of these calls, specifying a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure overrides the setting of **ActivateAtStorage** for the duration of the function call.</span></span> <span data-ttu-id="c4b1b-114">Der Aufrufer kann **COSERVERINFO** -Informationen über die [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) -Struktur an **IMoniker:: BindToObject** übergeben.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-114">The caller can pass **COSERVERINFO** information to **IMoniker::BindToObject** through the [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) structure.</span></span>

<span data-ttu-id="c4b1b-115">Der für **activateatstorage** festgelegte Wert ist auch das Standardverhalten, wenn der CLSCTX- \_ Remote \_ Server angegeben wird, wenn auf dem Client Computer keine Registrierungsinformationen für die Klasse installiert sind.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-115">The value set for **ActivateAtStorage** is also the default behavior when CLSCTX\_REMOTE\_SERVER is specified if no registry information for the class is installed on the client's computer.</span></span> <span data-ttu-id="c4b1b-116">Client Anwendungen, die für die Nutzung von **activateatstorage** geschrieben wurden, benötigen daher möglicherweise weniger Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="c4b1b-116">Client applications written to take advantage of **ActivateAtStorage** may therefore require less administration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4b1b-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4b1b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4b1b-118">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="c4b1b-118">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[<span data-ttu-id="c4b1b-119">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="c4b1b-119">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[<span data-ttu-id="c4b1b-120">**Cogetinstancefromistorage**</span><span class="sxs-lookup"><span data-stu-id="c4b1b-120">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[<span data-ttu-id="c4b1b-121">**COSERVERINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b1b-121">**COSERVERINFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[<span data-ttu-id="c4b1b-122">**IMoniker:: bindtoken Object**</span><span class="sxs-lookup"><span data-stu-id="c4b1b-122">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[<span data-ttu-id="c4b1b-123">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="c4b1b-123">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 