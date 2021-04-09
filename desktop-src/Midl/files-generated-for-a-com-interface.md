---
title: Für eine COM-Schnittstelle generierte Dateien
description: Für COM-Schnittstellen kombiniert der Mittelwert Compiler alle Client-und Objekt Server-Erweiterungs Routinen und-Daten in einer einzelnen Schnittstellen Proxy Datei.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- Mittel l compilermittell, Mittel l und com
- COM-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948665"
---
# <a name="files-generated-for-a-com-interface"></a><span data-ttu-id="78597-105">Für eine COM-Schnittstelle generierte Dateien</span><span class="sxs-lookup"><span data-stu-id="78597-105">Files Generated for a COM Interface</span></span>

<span data-ttu-id="78597-106">Für COM-Schnittstellen kombiniert der Mittelwert Compiler alle Client-und Objekt Server-Erweiterungs Routinen und-Daten in einer einzelnen Schnittstellen Proxy Datei.</span><span class="sxs-lookup"><span data-stu-id="78597-106">For COM interfaces, the MIDL compiler combines all client and object server auxiliary routines and data into a single interface proxy file.</span></span> <span data-ttu-id="78597-107">Diese Datei enthält die Ersatz Einstiegspunkte für Clients und Server.</span><span class="sxs-lookup"><span data-stu-id="78597-107">This file includes the surrogate entry points for both clients and servers.</span></span> <span data-ttu-id="78597-108">Außerdem generiert der-compilercompiler eine Schnittstellen Header Datei, eine Schnittstellen-UUID-Datei und eine Schnittstellen Registrierungsdatei.</span><span class="sxs-lookup"><span data-stu-id="78597-108">In addition, the MIDL compiler generates an interface header file, an interface UUID file and an interface registration file.</span></span> <span data-ttu-id="78597-109">Diese Dateien werden beim Erstellen einer Proxy-dll verwendet, die den Code enthält, um die Verwendung der-Schnittstelle sowohl von Client Anwendungen als auch von Objekt Servern zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="78597-109">You will use all these files when creating a proxy DLL that contains the code to support the use of the interface by both client applications and object servers.</span></span> <span data-ttu-id="78597-110">Beim Erstellen der ausführbaren Datei für eine Client Anwendung, die die-Schnittstelle verwendet, verwenden Sie außerdem die-Schnittstellen Header Datei und die-Schnittstellen-UUID-Datei.</span><span class="sxs-lookup"><span data-stu-id="78597-110">You will also use the interface header file and the interface UUID file when creating the executable file for a client application that uses the interface.</span></span>

<span data-ttu-id="78597-111">In den folgenden Themen werden die einzelnen Dateien beschrieben, die für eine benutzerdefinierte COM-Schnittstelle generiert werden, indem Sie das **\[** [**Object**](object.md) - **\]** Attribut in die Schnittstellen Attribut Liste der IDL-Datei einschließen:</span><span class="sxs-lookup"><span data-stu-id="78597-111">The following topics describe each of the files generated for a custom COM interface, which you identify by including the **\[**[**object**](object.md)**\]** attribute in the interface attribute list of the IDL file:</span></span>

-   [<span data-ttu-id="78597-112">Die Schnittstellen Proxy Datei</span><span class="sxs-lookup"><span data-stu-id="78597-112">The Interface Proxy File</span></span>](the-interface-proxy-file.md)
-   [<span data-ttu-id="78597-113">Die Header Dateien</span><span class="sxs-lookup"><span data-stu-id="78597-113">The Header Files</span></span>](the-header-files.md)
-   [<span data-ttu-id="78597-114">Die UUID-Schnittstellen Datei</span><span class="sxs-lookup"><span data-stu-id="78597-114">The Interface UUID File</span></span>](the-interface-uuid-file.md)
-   [<span data-ttu-id="78597-115">Die Schnittstellen Registrierungsdatei</span><span class="sxs-lookup"><span data-stu-id="78597-115">The Interface Registration File</span></span>](the-interface-registration-file.md)

<span data-ttu-id="78597-116">Weitere Informationen finden Sie unter [Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md), [**/App \_ config**](-app-config.md), [Interface Definition (IDL)-Datei](interface-definition-idl-file.md)und entwickeln [und Registrieren einer Proxy-dll](../com/building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="78597-116">For more information, see [Application Configuration File (ACF)](application-configuration-file-acf-.md), [**/app\_config**](-app-config.md), [Interface Definition (IDL) File](interface-definition-idl-file.md), and [Building and Registering a Proxy DLL](../com/building-and-registering-a-proxy-dll.md).</span></span>

 

 