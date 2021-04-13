---
title: EAP-Installation
description: Anbieter implementieren eaps, auch als Authentifizierungsprotokolle bezeichnet, in Dynamic Link Libraries (DLLs).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389634"
---
# <a name="eap-installation"></a><span data-ttu-id="9e6d2-103">EAP-Installation</span><span class="sxs-lookup"><span data-stu-id="9e6d2-103">EAP Installation</span></span>

<span data-ttu-id="9e6d2-104">Anbieter implementieren eaps, auch als Authentifizierungsprotokolle bezeichnet, in Dynamic Link Libraries (DLLs).</span><span class="sxs-lookup"><span data-stu-id="9e6d2-104">Vendors implement EAPs, also known as authentication protocols, in dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="9e6d2-105">Eine DLL für das Authentifizierungsprotokoll muss sowohl auf dem Client-als auch auf dem Server Computer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-105">A DLL for the authentication protocol must reside on both the client and server computers.</span></span> <span data-ttu-id="9e6d2-106">Der Einfachheit halber können die Client-und Server-DLLs identisch sein. Dies ist jedoch keine Voraussetzung.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-106">For simplicity, the client and server DLLs may be identical; however, this is not a requirement.</span></span> <span data-ttu-id="9e6d2-107">Beachten Sie außerdem, dass dieselbe DLL mehr als ein Authentifizierungsprotokoll unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-107">Also, be aware that the same DLL may support more than one authentication protocol.</span></span>

<span data-ttu-id="9e6d2-108">Der Anbieter sollte Setup Software zum Installieren und Entfernen der DLL bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-108">The vendor should provide setup software to install and remove the DLL.</span></span> <span data-ttu-id="9e6d2-109">Von der Setup Software sollten außerdem die entsprechenden Schlüssel und Werte für das Authentifizierungsprotokoll in der Systemregistrierung erstellt und bei der Deinstallation entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-109">The setup software should also create the appropriate keys and values for the authentication protocol in the system registry and remove them upon uninstall.</span></span>

<span data-ttu-id="9e6d2-110">Die Installation der einzelnen EAP-dll sollte den folgenden Registrierungsschlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-110">The installation of each EAP DLL should create the following registry key.</span></span>

<span data-ttu-id="9e6d2-111">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**</span><span class="sxs-lookup"><span data-stu-id="9e6d2-111">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Rasman**\\**PPP**\\**EAP**\\**&lt;eaptypeid&gt;**</span></span>

<span data-ttu-id="9e6d2-112">Im vorangehenden Pfad ist **&lt; eaptypeid &gt;** die ID des Authentifizierungs Protokolls.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-112">In the preceding path, **&lt;eaptypeid&gt;** is the ID of the authentication protocol.</span></span> <span data-ttu-id="9e6d2-113">Der Anbieter muss diese ID von der Internet Assigned Numbers Authority (IANA) abrufen.</span><span class="sxs-lookup"><span data-stu-id="9e6d2-113">The vendor must obtain this ID from the Internet Assigned Numbers Authority (IANA).</span></span>

<span data-ttu-id="9e6d2-114">Weitere Informationen und eine Beschreibung der unterstützten Werte für diesen Schlüssel finden Sie unter [Registrierungs Werte für das Authentifizierungsprotokoll](authentication-protocol-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="9e6d2-114">For more information and a description of the supported values for this key, see [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).</span></span>

 

 




