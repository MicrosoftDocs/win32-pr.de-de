---
title: Schema (AD DS)
description: Active Directory Schema ist als Satz von Objektklassen Instanzen implementiert, die im Verzeichnis gespeichert werden.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory Schema Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "103719884"
---
# <a name="schema-ad-ds"></a><span data-ttu-id="e81a3-104">Schema (AD DS)</span><span class="sxs-lookup"><span data-stu-id="e81a3-104">Schema (AD DS)</span></span>

<span data-ttu-id="e81a3-105">Active Directory Schema ist als Satz von Objektklassen Instanzen implementiert, die im Verzeichnis gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e81a3-105">Active Directory schema is implemented as a set of object class instances stored in the directory.</span></span> <span data-ttu-id="e81a3-106">Dies unterscheidet sich sehr von vielen Verzeichnissen, die über ein Schema verfügen, aber als Textdatei gespeichert werden, die beim Start gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e81a3-106">This is very different than many directories that have a schema but store it as a text file read at startup.</span></span> <span data-ttu-id="e81a3-107">Das Speichern des Schemas im Verzeichnis hat viele Vorteile.</span><span class="sxs-lookup"><span data-stu-id="e81a3-107">Storing the schema in the directory has many advantages.</span></span> <span data-ttu-id="e81a3-108">Benutzer Anwendungen können diese z. b. lesen, um zu ermitteln, welche Objekte und Eigenschaften verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e81a3-108">For example, user applications can read it to discover what objects and properties are available.</span></span>

<span data-ttu-id="e81a3-109">Active Directory Schema kann dynamisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e81a3-109">Active Directory schema can be updated dynamically.</span></span> <span data-ttu-id="e81a3-110">Das heißt, eine Anwendung kann das Schema mit neuen Attributen und Klassen erweitern und die Erweiterungen sofort verwenden.</span><span class="sxs-lookup"><span data-stu-id="e81a3-110">That is, an application can extend the schema with new attributes and classes and use the extensions immediately.</span></span> <span data-ttu-id="e81a3-111">Schema Aktualisierungen werden erreicht, indem die im Verzeichnis gespeicherten Schema Objekte erstellt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e81a3-111">Schema updates are accomplished by creating or modifying the schema objects stored in the directory.</span></span> <span data-ttu-id="e81a3-112">Wie jedes Objekt in Active Directory schützen Zugriffs Steuerungs Listen (ACLs) Schema Objekte, sodass autorisierte Benutzer das Schema nur ändern können.</span><span class="sxs-lookup"><span data-stu-id="e81a3-112">Like every object in Active Directory, access-control lists (ACLs) protect schema objects, so authorized users only may alter the schema.</span></span>

<span data-ttu-id="e81a3-113">Weitere Informationen finden Sie unter [Active Directory Schema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="e81a3-113">For more information, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 




