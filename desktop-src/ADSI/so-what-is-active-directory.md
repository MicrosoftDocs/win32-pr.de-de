---
title: Übersicht über das Tutorial ADSI with Visual Basic
description: Active Directory ist eine zweckgebundene Datenbank \ 8212; Es handelt sich nicht um eine Registrierungs Ersetzung.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104555828"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a><span data-ttu-id="ffa21-103">Übersicht über das Tutorial: ADSI with Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ffa21-103">Tutorial Overview: ADSI with Visual Basic</span></span>

> [!Note]  
> <span data-ttu-id="ffa21-104">Die folgende Dokumentation ist Teil einer erweiterten Szenariobeschreibung für Visual Basic-Entwickler.</span><span class="sxs-lookup"><span data-stu-id="ffa21-104">The following documentation is part of an extended scenario description for Visual Basic developers.</span></span> <span data-ttu-id="ffa21-105">Eine allgemeine Übersicht über Active Directory finden Sie in der Dokumentation [zu IT-Experten auf TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="ffa21-105">If you are looking for a general overview of Active Directory, see the [IT Pro docs on Technet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span></span> <span data-ttu-id="ffa21-106">Eine ausführlichere Betrachtung der Entwicklungsseite Active Directory finden Sie unter [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="ffa21-106">For a more in-depth look at the development side of Active Directory, see [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span></span> <span data-ttu-id="ffa21-107">Eine größere Einführung in Active Directory-Dienst Schnittstellen finden Sie im übergeordneten Thema dieses Themas: [Active Directory Dienst Schnittstellen](active-directory-service-interfaces-adsi.md)sowie im gleich geordneten Thema: Informationen zu [Active Directory Dienst Schnittstellen](about-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="ffa21-107">For a larger introduction to Active Directory Service Interfaces, see this topic's parent topic: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), as well as the sibling topic: [About Active Directory Service Interfaces](about-adsi.md).</span></span>

 

<span data-ttu-id="ffa21-108">Active Directory ist eine zweckgebundene Datenbank – es handelt sich nicht um eine Registrierungs Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="ffa21-108">Active Directory is a special-purpose database — it is not a registry replacement.</span></span> <span data-ttu-id="ffa21-109">Das Verzeichnis ist für die Verarbeitung einer großen Anzahl von Lese-und Such Vorgängen und einer erheblich geringeren Anzahl von Änderungen und Updates konzipiert.</span><span class="sxs-lookup"><span data-stu-id="ffa21-109">The directory is designed to handle a large number of read and search operations and a significantly smaller number of changes and updates.</span></span> <span data-ttu-id="ffa21-110">Active Directory Daten sind hierarchisch, repliziert und erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="ffa21-110">Active Directory data is hierarchical, replicated, and extensible.</span></span> <span data-ttu-id="ffa21-111">Da Sie repliziert wird, möchten Sie keine dynamischen Daten speichern, wie z. b. Aktienkurse oder CPU-Leistung.</span><span class="sxs-lookup"><span data-stu-id="ffa21-111">Because it is replicated, you do not want to store dynamic data, such as corporate stock prices or CPU performance.</span></span> <span data-ttu-id="ffa21-112">Wenn die Daten Computer spezifisch sind, speichern Sie die Daten in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ffa21-112">If your data is machine-specific, store the data in the registry.</span></span> <span data-ttu-id="ffa21-113">Typische Beispiele für Daten, die im Verzeichnis gespeichert werden, sind Drucker Warteschlangen Daten, Benutzer Kontaktdaten und Netzwerk-/computerkonfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="ffa21-113">Typical examples of data stored in the directory include printer queue data, user contact data, and network/computer configuration data.</span></span> <span data-ttu-id="ffa21-114">Die Active Directory-Datenbank besteht aus Objekten und Attributen.</span><span class="sxs-lookup"><span data-stu-id="ffa21-114">The Active Directory database consists of objects and attributes.</span></span> <span data-ttu-id="ffa21-115">Objekte und Attribut Definitionen werden im Active Directory Schema gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ffa21-115">Objects and attribute definitions are stored in the Active Directory schema.</span></span>

<span data-ttu-id="ffa21-116">Sie Fragen sich vielleicht, welche Objekte derzeit in Active Directory gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ffa21-116">You may be wondering what objects are currently stored in Active Directory.</span></span> <span data-ttu-id="ffa21-117">Active Directory hat drei Partitionen.</span><span class="sxs-lookup"><span data-stu-id="ffa21-117">Active Directory has three partitions.</span></span> <span data-ttu-id="ffa21-118">Diese werden auch als Namenskontexte bezeichnet: Domäne, Schema und Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ffa21-118">These are also known as naming contexts: domain, schema, and configuration.</span></span> <span data-ttu-id="ffa21-119">Die Domänen Partition enthält Benutzer, Gruppen, Kontakte, Computer, Organisationseinheiten und viele andere Objekttypen.</span><span class="sxs-lookup"><span data-stu-id="ffa21-119">The domain partition contains users, groups, contacts, computers, organizational units, and many other object types.</span></span> <span data-ttu-id="ffa21-120">Da Active Directory erweiterbar ist, können Sie auch eigene Klassen und/oder Attribute hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ffa21-120">Because Active Directory is extensible, you can also add your own classes and/or attributes.</span></span> <span data-ttu-id="ffa21-121">Die Schema Partition enthält Klassen und Attribut Definitionen.</span><span class="sxs-lookup"><span data-stu-id="ffa21-121">The schema partition contains classes and attribute definitions.</span></span> <span data-ttu-id="ffa21-122">Die Konfigurations Partition enthält Konfigurationsdaten für Dienste, Partitionen und Standorte.</span><span class="sxs-lookup"><span data-stu-id="ffa21-122">The configuration partition includes configuration data for services, partitions, and sites.</span></span>

<span data-ttu-id="ffa21-123">Der folgende Screenshot zeigt die Active Directory Domänen Partition.</span><span class="sxs-lookup"><span data-stu-id="ffa21-123">The following screen shot shows the Active Directory domain partition.</span></span>

![Active Directory-Domänen Partition](images/adadsi1.png)

## <a name="related-topics"></a><span data-ttu-id="ffa21-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ffa21-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffa21-126">Zugreifen auf Active Directory mithilfe Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ffa21-126">Accessing Active Directory Using Visual Basic</span></span>](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[<span data-ttu-id="ffa21-127">Szenario: fabrikam Corporation</span><span class="sxs-lookup"><span data-stu-id="ffa21-127">Scenario: The Fabrikam Corporation</span></span>](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[<span data-ttu-id="ffa21-128">Erweiterte Themen</span><span class="sxs-lookup"><span data-stu-id="ffa21-128">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 