---
title: RemoteServerName
description: Konfiguriert den Client so, dass das Objekt auf einem bestimmten Computer ausgeführt wird, wenn eine Aktivierungsfunktion aufgerufen wird, für die keine COSERVERINFO-Struktur angegeben ist.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Remoteservername-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339918"
---
# <a name="remoteservername"></a><span data-ttu-id="7d8b9-104">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="7d8b9-104">RemoteServerName</span></span>

<span data-ttu-id="7d8b9-105">Konfiguriert den Client so, dass das Objekt auf einem bestimmten Computer ausgeführt wird, wenn eine Aktivierungsfunktion aufgerufen wird, für die keine [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-105">Configures the client to request the object be run at a particular computer whenever an activation function is called for which a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure is not specified.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7d8b9-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="7d8b9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a><span data-ttu-id="7d8b9-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d8b9-107">Remarks</span></span>

<span data-ttu-id="7d8b9-108">**Remoteservername** ermöglicht die einfache Konfigurations Verwaltung von Client Anwendungen. Sie können ohne hart codierte Servernamen geschrieben werden und können konfiguriert werden, indem Sie die **Remoteservername** -Registrierungs Werte der Klassen von Objekten ändern, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-108">**RemoteServerName** allows simple configuration management of client applications; they may be written without hard-coded server names and can be configured by modifying the **RemoteServerName** registry values of the classes of objects they use.</span></span>

<span data-ttu-id="7d8b9-109">Wie in der Dokumentation für die [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) -Enumeration und die [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur beschrieben, handelt es sich bei einem der Parameter der verteilten COM-Aktivierung um einen Zeiger auf eine **COSERVERINFO** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-109">As described in the documentation for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration and the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, one of the parameters of the distributed COM activation is a pointer to a **COSERVERINFO** structure.</span></span> <span data-ttu-id="7d8b9-110">Wenn dieser Wert nicht **null** ist, überschreibt die Informationen in der **COSERVERINFO** -Struktur die Einstellung des **Remoteservername** -Schlüssels für den Funktions Aufruf.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-110">When this value is not **NULL**, the information in the **COSERVERINFO** structure overrides the setting of the **RemoteServerName** key for the function call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d8b9-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d8b9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d8b9-112">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="7d8b9-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 