---
description: Wenn Sie den Active Directory Anbieter über WMI aufrufen, geben Sie den LDAP-Namespace (Lightweight Directory Access Protocol) und ADSI-Pfade (Active Directory Services Interface) an.
ms.assetid: 55733fba-2170-4400-a516-896f6bf9525a
ms.tgt_platform: multiple
title: Verwenden der richtigen Active Directory Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e321d6919c48103be930226cf11c4b3e82dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360162"
---
# <a name="using-the-proper-active-directory-syntax"></a><span data-ttu-id="9476b-103">Verwenden der richtigen Active Directory Syntax</span><span class="sxs-lookup"><span data-stu-id="9476b-103">Using the Proper Active Directory Syntax</span></span>

<span data-ttu-id="9476b-104">Wenn Sie den [Active Directory Anbieter](/previous-versions/windows/desktop/dsprov/active-directory-provider) über WMI aufrufen, geben Sie den LDAP-Namespace (Lightweight Directory Access Protocol) und ADSI-Pfade (Active Directory Services Interface) an.</span><span class="sxs-lookup"><span data-stu-id="9476b-104">You supply the Lightweight Directory Access Protocol (LDAP) namespace and Active Directory Services Interface (ADSI) paths when calling the [Active Directory Provider](/previous-versions/windows/desktop/dsprov/active-directory-provider) through WMI.</span></span>

<span data-ttu-id="9476b-105">In den folgenden Themen werden der LDAP-Namespace und der ADSI-Pfad beschrieben:</span><span class="sxs-lookup"><span data-stu-id="9476b-105">The following topics describe the LDAP namespace and the ADSI path:</span></span>

-   [<span data-ttu-id="9476b-106">Beschreiben des LDAP-Namespace</span><span class="sxs-lookup"><span data-stu-id="9476b-106">Describing the LDAP Namespace</span></span>](describing-the-ldap-namespace.md)

    <span data-ttu-id="9476b-107">Ein Namespace Pfad beschreibt den Speicherort eines Remote Namespace.</span><span class="sxs-lookup"><span data-stu-id="9476b-107">A namespace path describes the location of a remote namespace.</span></span> <span data-ttu-id="9476b-108">Verwenden Sie den Namespace Pfad, um eine Remote Verbindung mit einem Active Directory Namespace herzustellen.</span><span class="sxs-lookup"><span data-stu-id="9476b-108">Use the namespace path to connect remotely to an Active Directory namespace.</span></span>

-   [<span data-ttu-id="9476b-109">Beschreiben des ADSI-Pfads</span><span class="sxs-lookup"><span data-stu-id="9476b-109">Describing the ADSI Path</span></span>](describing-the-adsi-path.md)

    <span data-ttu-id="9476b-110">Der ADSI-Pfad beschreibt den Speicherort eines Objekts, das die ADSI-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="9476b-110">The ADSI path describes the location of an object using the ADSI API.</span></span> <span data-ttu-id="9476b-111">Verwenden Sie den ADSI-Pfad in den Parametern, die der Anbieter an Active Directory übergibt.</span><span class="sxs-lookup"><span data-stu-id="9476b-111">Use the ADSI path in parameters that the provider passes onto Active Directory.</span></span>

> [!Note]  
> <span data-ttu-id="9476b-112">Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="9476b-112">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 
