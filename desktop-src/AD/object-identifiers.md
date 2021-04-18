---
title: Objekt Bezeichner (AD DS)
description: Objekt-IDs (OIDs) sind eindeutige numerische Werte, die von verschiedenen ausstellenden Behörden ausgegeben werden, um Datenelemente, Syntaxen und andere Teile verteilter Anwendungen eindeutig zu identifizieren.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- Objekt Bezeichner AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "106339036"
---
# <a name="object-identifiers-ad-ds"></a><span data-ttu-id="2444f-104">Objekt Bezeichner (AD DS)</span><span class="sxs-lookup"><span data-stu-id="2444f-104">Object Identifiers (AD DS)</span></span>

<span data-ttu-id="2444f-105">Objekt-IDs (OIDs) sind eindeutige numerische Werte, die von verschiedenen ausstellenden Behörden ausgegeben werden, um Datenelemente, Syntaxen und andere Teile verteilter Anwendungen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2444f-105">Object Identifiers (OIDs) are unique numeric values issued by various issuing authorities to uniquely identify data elements, syntaxes, and other parts of distributed applications.</span></span> <span data-ttu-id="2444f-106">OIDs finden Sie in OSI-Anwendungen, X. 500-Verzeichnissen, SNMP und anderen Anwendungen, in denen die Eindeutigkeit wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="2444f-106">OIDs are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="2444f-107">OIDs basieren auf einer Baumstruktur, in der eine übergeordnete ausstellende Zertifizierungsstelle, wie z. b. das ISO, eine Verzweigung der Struktur einer untergeordneten Zertifizierungsstelle zuordnet, die wiederum untergeordnete branches zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="2444f-107">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a subauthority, who in turn can allocate subbranches.</span></span>

<span data-ttu-id="2444f-108">Das LDAP-Protokoll (RFC 2251) erfordert einen Verzeichnisdienst, um Objektklassen, Attribute und Syntaxen mit OIDs zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2444f-108">The LDAP protocol (RFC 2251) requires a directory service to identify object classes, attributes, and syntaxes with OIDs.</span></span> <span data-ttu-id="2444f-109">Dies ist Teil der LDAP X. 500-Legacy-Version.</span><span class="sxs-lookup"><span data-stu-id="2444f-109">This is part of the LDAP X.500 legacy.</span></span>

<span data-ttu-id="2444f-110">OIDs in Active Directory Domain Services enthalten einige von der ISO-Ausgabe für X. 500-Klassen und-Attribute sowie einige von Microsoft und anderen ausstellenden Behörden ausgestellten.</span><span class="sxs-lookup"><span data-stu-id="2444f-110">OIDs in Active Directory Domain Services include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft and other issuing authorities.</span></span> <span data-ttu-id="2444f-111">Die OID-Notation ist eine gepunktete Zeichenfolge von Zahlen, z. b. "1.2.840.113556.1.5.9", die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2444f-111">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.9", which is described in the following table.</span></span>



| <span data-ttu-id="2444f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2444f-112">Value</span></span>  | <span data-ttu-id="2444f-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2444f-113">Meaning</span></span>          | <span data-ttu-id="2444f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2444f-114">Description</span></span>                                              |
|--------|------------------|----------------------------------------------------------|
| <span data-ttu-id="2444f-115">1</span><span class="sxs-lookup"><span data-stu-id="2444f-115">1</span></span>      | <span data-ttu-id="2444f-116">ISO</span><span class="sxs-lookup"><span data-stu-id="2444f-116">ISO</span></span>              | <span data-ttu-id="2444f-117">Identifiziert die Stamm Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="2444f-117">Identifies the root authority.</span></span>                           |
| <span data-ttu-id="2444f-118">2</span><span class="sxs-lookup"><span data-stu-id="2444f-118">2</span></span>      | <span data-ttu-id="2444f-119">ANSI</span><span class="sxs-lookup"><span data-stu-id="2444f-119">ANSI</span></span>             | <span data-ttu-id="2444f-120">Von ISO zugewiesene Gruppen Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="2444f-120">Group designation assigned by ISO.</span></span>                       |
| <span data-ttu-id="2444f-121">840</span><span class="sxs-lookup"><span data-stu-id="2444f-121">840</span></span>    | <span data-ttu-id="2444f-122">USA</span><span class="sxs-lookup"><span data-stu-id="2444f-122">USA</span></span>              | <span data-ttu-id="2444f-123">Die von der Gruppe zugewiesene Bezeichnung für Land/Region.</span><span class="sxs-lookup"><span data-stu-id="2444f-123">Country/region designation assigned by the group.</span></span>        |
| <span data-ttu-id="2444f-124">113556</span><span class="sxs-lookup"><span data-stu-id="2444f-124">113556</span></span> | <span data-ttu-id="2444f-125">Microsoft</span><span class="sxs-lookup"><span data-stu-id="2444f-125">Microsoft</span></span>        | <span data-ttu-id="2444f-126">Organisations Bezeichnung, die vom Land/der Region zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2444f-126">Organization designation assigned by the country/region.</span></span> |
| <span data-ttu-id="2444f-127">1</span><span class="sxs-lookup"><span data-stu-id="2444f-127">1</span></span>      | <span data-ttu-id="2444f-128">Active Directory</span><span class="sxs-lookup"><span data-stu-id="2444f-128">Active Directory</span></span> | <span data-ttu-id="2444f-129">Wird von der Organisation zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2444f-129">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="2444f-130">5</span><span class="sxs-lookup"><span data-stu-id="2444f-130">5</span></span>      | <span data-ttu-id="2444f-131">Klassen</span><span class="sxs-lookup"><span data-stu-id="2444f-131">Classes</span></span>          | <span data-ttu-id="2444f-132">Wird von der Organisation zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2444f-132">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="2444f-133">9</span><span class="sxs-lookup"><span data-stu-id="2444f-133">9</span></span>      | <span data-ttu-id="2444f-134">**Benutzer** Klasse</span><span class="sxs-lookup"><span data-stu-id="2444f-134">**user** class</span></span>   | <span data-ttu-id="2444f-135">Wird von der Organisation zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2444f-135">Assigned by the organization.</span></span>                            |



 

<span data-ttu-id="2444f-136">Weitere Informationen und eine Erörterung zweier Prozeduren, mit denen gültige OIDs zum Erweitern des Active Directory Schemas abgerufen werden, finden Sie unter Abrufen [eines Objekt Bezeichners](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="2444f-136">For more information, and a discussion of two procedures used to obtain valid OIDs for use in extending the Active Directory schema, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>

 

 




