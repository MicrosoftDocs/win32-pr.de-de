---
title: Kategorisierung von DCOM-Proxys und Stub
description: Kategorisierung von DCOM-Proxys und Stub
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341333"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a><span data-ttu-id="86433-103">Kategorisierung von DCOM-Proxys und Stub</span><span class="sxs-lookup"><span data-stu-id="86433-103">Categorizing DCOM Proxies and Stubs</span></span>

<span data-ttu-id="86433-104">DCOM Marshalls Verweise auf Objekte durch das Erstellen von objrefs, die CLSIDs enthalten.</span><span class="sxs-lookup"><span data-stu-id="86433-104">DCOM marshals references to objects by constructing OBJREFs that contain CLSIDs.</span></span> <span data-ttu-id="86433-105">Diese CLSIDs sind anfällig für Sicherheitsangriffe, da beliebige DLLs während des Marshalling geladen werden können.</span><span class="sxs-lookup"><span data-stu-id="86433-105">These CLSIDs are vulnerable to security attacks because arbitrary DLLs can be loaded during marshaling.</span></span> <span data-ttu-id="86433-106">Allerdings \_ \_ \_ kann beim Aufrufen von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) das eoac-Flag No Custom Marshal angegeben werden (siehe [**Eole- \_ Authentifizierungs \_ Funktionen**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span><span class="sxs-lookup"><span data-stu-id="86433-106">However, the EOAC\_NO\_CUSTOM\_MARSHAL flag can be specified when calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (see [**EOLE\_AUTHENTICATION\_CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span></span> <span data-ttu-id="86433-107">Das Festlegen dieses Flags trägt zum Schutz der Serversicherheit bei der Verwendung von DCOM bei, da es die Wahrscheinlichkeit verringert, dass beliebige DLLs ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="86433-107">Setting this flag helps protect server security when using DCOM because it reduces the chances of executing arbitrary DLLs.</span></span> <span data-ttu-id="86433-108">Wenn dieses Flag festgelegt ist, lässt der Server nur das Marshalling von CLSIDs zu, die in ole32.dll, comadmin.dll, comsvcs.dll oder es.dll implementiert sind oder die die CATID- \_ Marshaler-Kategorie-ID implementieren.</span><span class="sxs-lookup"><span data-stu-id="86433-108">When this flag is set, the server allows the marshaling only of CLSIDs that are implemented in ole32.dll, comadmin.dll, comsvcs.dll, or es.dll, or that implement the CATID\_MARSHALER category ID.</span></span>

<span data-ttu-id="86433-109">Der CATID- \_ Mars Haller ist eine Komponenten Kategorie-GUID, die einer CLSID zugeordnet werden kann, die Benutzer definiert gemarshallt wird.</span><span class="sxs-lookup"><span data-stu-id="86433-109">CATID\_MARSHALER is a component category GUID that can be associated with a CLSID that is being custom marshaled.</span></span> <span data-ttu-id="86433-110">Die Schnittstellen, die mit dieser CLSID als Benutzer definiert gemarshallt werden, sind zulässig, wenn der eoac \_ keinen \_ benutzerdefinierten \_ Marshal über [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="86433-110">The interfaces being custom marshaled with this CLSID are allowed when the EOAC\_NO\_CUSTOM\_MARSHAL is set via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86433-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86433-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86433-112">Komponentenkategorien</span><span class="sxs-lookup"><span data-stu-id="86433-112">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 