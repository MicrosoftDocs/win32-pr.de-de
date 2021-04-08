---
title: Programmgesteuerte Erweiterung
description: Programmgesteuerte Erweiterungen haben mehrere Vorzüge, eine Anwendung ist jedoch nicht transparent. der Administrator muss der Dokumentation Vertrauen, die in der Setup Anwendung enthalten ist.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Programmgesteuerte Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707583"
---
# <a name="programmatic-extension"></a><span data-ttu-id="86116-104">Programmgesteuerte Erweiterung</span><span class="sxs-lookup"><span data-stu-id="86116-104">Programmatic Extension</span></span>

<span data-ttu-id="86116-105">Der Vorteil einer LDIF-Datei besteht darin, dass der Administrator seine Funktion überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="86116-105">The benefit of an LDIF file is that the administrator can examine its function.</span></span> <span data-ttu-id="86116-106">Das Schema kann jedoch auch Programm gesteuert erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="86116-106">However, the schema can also be extended programmatically.</span></span> <span data-ttu-id="86116-107">Programmgesteuerte Erweiterungen haben mehrere Vorzüge, aber eine Anwendung ist nicht transparent. der Administrator muss der Dokumentation Vertrauen, die in der Setup Anwendung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="86116-107">Programmatic extensions have several merits, but an application is opaque; the administrator must trust the documentation included with the setup application.</span></span> <span data-ttu-id="86116-108">Die Verwendung von programmgesteuerten Schema Erweiterungen kann eine Barriere für die Bereitstellung von Anwendungen darstellen, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="86116-108">Use of programmatic schema extensions may be a barrier to deployment for applications that use them.</span></span> <span data-ttu-id="86116-109">Eine programmgesteuerte Erweiterung ist invariant. Es handelt sich um eine ausführbare Windows NT-Datei.</span><span class="sxs-lookup"><span data-stu-id="86116-109">A programmatic extension is invariant; it is a Windows NT executable.</span></span> <span data-ttu-id="86116-110">Die Binärdatei kann nicht manipuliert werden, im Gegensatz zu einer LDIF-oder CSV-Datei, die versehentlich oder böswillig bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="86116-110">The binary cannot be tampered with, unlike an LDIF or .csv file, which can be edited inadvertently or maliciously.</span></span>

<span data-ttu-id="86116-111">Zu den Vorteilen einer LDIF-Datei gehören:</span><span class="sxs-lookup"><span data-stu-id="86116-111">Benefits of an LDIF file include:</span></span>

-   <span data-ttu-id="86116-112">Anwendungen können Fehler erkennen und Wiederherstellen und Benutzer Feedback bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="86116-112">Applications can detect and recover from errors and provide user feedback.</span></span>
-   <span data-ttu-id="86116-113">Anwendungen können Unicode verarbeiten, ohne auf Base64-Codierung zurückzugreifen.</span><span class="sxs-lookup"><span data-stu-id="86116-113">Applications can handle Unicode without resorting to Base64 encoding.</span></span>
-   <span data-ttu-id="86116-114">Anwendungen können Windows Installer Setup-APIs nutzen.</span><span class="sxs-lookup"><span data-stu-id="86116-114">Applications can leverage Windows Installer setup APIs.</span></span>
-   <span data-ttu-id="86116-115">Anwendungen können signiert werden, um Authentizität zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="86116-115">Applications can be signed to establish authenticity.</span></span>

 

 




