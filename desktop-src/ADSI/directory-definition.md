---
title: Verzeichnis Definition
description: Die Beispiel Anbieter Komponente verwendet einen relativ einfachen Verzeichnis Entwurf, um die Beziehung zwischen den Komponenten zu verdeutlichen und die Mindestanforderungen anzuzeigen, die für einen ADSI-Anbieter erforderlich sind.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855324"
---
# <a name="directory-definition"></a><span data-ttu-id="eea93-103">Verzeichnis Definition</span><span class="sxs-lookup"><span data-stu-id="eea93-103">Directory Definition</span></span>

<span data-ttu-id="eea93-104">Die Beispiel Anbieter Komponente verwendet einen relativ einfachen Verzeichnis Entwurf, um die Beziehung zwischen den Komponenten zu verdeutlichen und die Mindestanforderungen anzuzeigen, die für einen ADSI-Anbieter erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eea93-104">The example provider component uses a relatively simple directory design to clarify the relationship between components and to show the minimum requirements necessary to be an ADSI provider.</span></span>

<span data-ttu-id="eea93-105">Das "Verzeichnis" für die Beispiel Anbieter Komponente besteht aus zwei Stamm Knoten: "Seattle" und "Toronto".</span><span class="sxs-lookup"><span data-stu-id="eea93-105">The "directory" for the example provider component consists of two root nodes: "Seattle" and "Toronto".</span></span> <span data-ttu-id="eea93-106">Seattle enthält zwei weitere Unterebenen: "Bellevue" und "Redmond".</span><span class="sxs-lookup"><span data-stu-id="eea93-106">Seattle contains two more sublevels, "Bellevue" and "Redmond".</span></span> <span data-ttu-id="eea93-107">Jeder dieser Einträge enthält mehrere Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="eea93-107">Each of these entries contains several user accounts.</span></span> <span data-ttu-id="eea93-108">Der Eintrag "Toronto" hat keine weiteren Unterebenen, sondern enthält direkt mehrere Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="eea93-108">The "Toronto" entry has no further sublevels, but directly contains several user accounts.</span></span> <span data-ttu-id="eea93-109">In der folgenden Abbildung werden diese beiden Stamm Knoten angezeigt, die mit einem Netzwerk verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="eea93-109">The following figure shows these two root nodes connected to a network.</span></span>

![Verzeichnis Definition](images/dssmdo.png)

<span data-ttu-id="eea93-111">Im hierarchischen Begriffen enthält der Namespace-Knoten "Seattle" und "Toronto".</span><span class="sxs-lookup"><span data-stu-id="eea93-111">In hierarchical terms, the Namespace node contains "Seattle" and "Toronto".</span></span> <span data-ttu-id="eea93-112">"Seattle" enthält "Bellevue" und "Redmond".</span><span class="sxs-lookup"><span data-stu-id="eea93-112">"Seattle" contains "Bellevue" and "Redmond".</span></span> <span data-ttu-id="eea93-113">"Bellevue" und "Redmond" enthalten jeweils eine Gruppe von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="eea93-113">"Bellevue" and "Redmond" each contain a set of user accounts.</span></span> <span data-ttu-id="eea93-114">"Toronto" enthält direkt die Benutzerkonten ohne zwischengeschaltete Organisations Knoten.</span><span class="sxs-lookup"><span data-stu-id="eea93-114">"Toronto" directly contains the user accounts with no intermediate organizational nodes.</span></span>

<span data-ttu-id="eea93-115">Die Beispiel Anbieter Komponente stellt diese Struktur mit nur zwei Active Directory Objekttypen dar: ein Container Objekt und ein Blatt Objekt.</span><span class="sxs-lookup"><span data-stu-id="eea93-115">The example provider component represents this structure with only two Active Directory object types: a container object and a leaf object.</span></span> <span data-ttu-id="eea93-116">"Seattle", "Toronto", "Bellevue" und "Redmond" sind Containerobjekte, und jedes Benutzerkonto ist ein Blatt Objekt.</span><span class="sxs-lookup"><span data-stu-id="eea93-116">"Seattle", "Toronto", "Bellevue", and "Redmond" are container objects and each user account is a leaf object.</span></span>

<span data-ttu-id="eea93-117">Die Beispiel Anbieter Komponente erstellt eine Schema Klasse mit dem Namen "Organisationseinheit" für einen Container Objekttyp und eine Schema Klasse mit dem Namen "User" für ein Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="eea93-117">The example provider component creates a schema class called "Organizational Unit" for a container object type and a schema class called "User" for a user account.</span></span>

<span data-ttu-id="eea93-118">Die Eigenschaften für jede Schema Klasse, ihre Methoden und die Regeln, die die Einschluss Beziehungen für diese Objekte steuern, sind alle in der [Schema Verwaltung](schema-management.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="eea93-118">The properties for each schema class, their methods, and the rules that govern the containment relationships for these objects are all defined in [Schema Management](schema-management.md).</span></span>

 

 




