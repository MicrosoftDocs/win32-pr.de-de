---
title: Einschränkungen bei der Schema Erweiterung
description: Um die Wahrscheinlichkeit von Schema Änderungen durch eine Anwendung zu verringern, die andere Anwendungen unterbricht, und die Schema Konsistenz aufrechtzuerhalten, Active Directory Domain Services Einschränkungen für den Typ von Schema Änderungen erzwingen, die eine Anwendung oder ein Benutzer ausführen darf.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707566"
---
# <a name="restrictions-on-schema-extension"></a><span data-ttu-id="719ba-103">Einschränkungen bei der Schema Erweiterung</span><span class="sxs-lookup"><span data-stu-id="719ba-103">Restrictions on Schema Extension</span></span>

<span data-ttu-id="719ba-104">Um die Wahrscheinlichkeit von Schema Änderungen durch eine Anwendung zu verringern, die andere Anwendungen unterbricht, und die Schema Konsistenz aufrechtzuerhalten, Active Directory Domain Services Einschränkungen für den Typ von Schema Änderungen erzwingen, die eine Anwendung oder ein Benutzer ausführen darf.</span><span class="sxs-lookup"><span data-stu-id="719ba-104">In order to reduce the possibility of schema changes by one application breaking other applications and to maintain schema consistency, Active Directory Domain Services enforce restrictions on the type of schema changes that an application or user is allowed to make.</span></span>

<span data-ttu-id="719ba-105">Die Einschränkungen werden nur beim Ändern vorhandener Schema Objekte auferlegt.</span><span class="sxs-lookup"><span data-stu-id="719ba-105">The restrictions are imposed only on modification of existing schema objects.</span></span> <span data-ttu-id="719ba-106">Das Schema wird in zwei Kategorien eingeteilt.</span><span class="sxs-lookup"><span data-stu-id="719ba-106">The schema is categorized into two categories.</span></span> <span data-ttu-id="719ba-107">Die Schema Objekte, die im Basis Schema mit Windows 2000 ausgeliefert werden, gehören zu Kategorie 1.</span><span class="sxs-lookup"><span data-stu-id="719ba-107">The schema objects that ship with Windows 2000 in the base schema belong to Category 1.</span></span> <span data-ttu-id="719ba-108">Alle Schema Objekte, die später von anderen Anwendungen oder Benutzern durch dynamische Schema Erweiterungen hinzugefügt werden, gehören zu Kategorie 2.</span><span class="sxs-lookup"><span data-stu-id="719ba-108">Any schema objects added later by other applications or users through dynamic schema extension belong to Category 2.</span></span> <span data-ttu-id="719ba-109">Die Kategorie eines Schema Objekts kann durch das 0x10-Bit bestimmt werden, das im **systemFlags** -Attribut für das **classSchema** -Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="719ba-109">The category of a schema object can be determined by the 0x10 bit set in the **systemFlags** attribute on the **classSchema** object.</span></span> <span data-ttu-id="719ba-110">Dieses Bit wird nur für Objekte der Kategorie 1 festgelegt und kann nicht geändert werden. es kann auch nicht für ein beliebiges Objekt der Kategorie 2 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="719ba-110">This bit is only set on Category 1 objects, and cannot be altered, nor can it be set on any Category 2 object.</span></span>

<span data-ttu-id="719ba-111">Das **systemFlags** -Attribut wird intern von Active Directory Domain Services verwendet, um besondere Merkmale von "Infrastruktur"-Objekten im Basis Schema zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="719ba-111">The **systemFlags** attribute is used internally by Active Directory Domain Services to identify special characteristics of "infrastructure" objects in the base schema.</span></span> <span data-ttu-id="719ba-112">Zusätzlich zur Identifizierung von Objekten der Kategorie 1 steuert **systemFlags** , ob ein Objekt verschoben, gelöscht oder umbenannt werden kann.</span><span class="sxs-lookup"><span data-stu-id="719ba-112">In addition to identifying Category 1 objects, **systemFlags** controls whether an object can be moved, deleted, or renamed.</span></span> <span data-ttu-id="719ba-113">Diese Vorgänge werden für Objekte verhindert, von denen Windows 2000 abhängig ist, um ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="719ba-113">These operations are prevented for objects that Windows 2000 depends on to run.</span></span>

<span data-ttu-id="719ba-114">Bei allen Schema Objekten, Kategorie 1 oder 2, müssen Active Directory Domain Services die folgenden Einschränkungen erzwingen:</span><span class="sxs-lookup"><span data-stu-id="719ba-114">On any schema objects, Category 1 or 2, Active Directory Domain Services impose the following restrictions:</span></span>

-   <span data-ttu-id="719ba-115">Sie können eine neue **must-** Klasse nicht zu einer Klasse hinzufügen (direkt oder durch Vererbung durch Hinzufügen einer zusätzlichen Klasse).</span><span class="sxs-lookup"><span data-stu-id="719ba-115">You cannot add a new **mustContain** to a class (directly or through inheritance by adding an auxiliary class).</span></span>
-   <span data-ttu-id="719ba-116">Sie können keine **mustare** der Klasse löschen (direkt oder durch Vererbung).</span><span class="sxs-lookup"><span data-stu-id="719ba-116">You cannot delete any **mustContain** of the class (directly or through inheritance).</span></span>

<span data-ttu-id="719ba-117">Außerdem werden die folgenden zusätzlichen Einschränkungen für Schema Objekte der Kategorie 1 auferlegt:</span><span class="sxs-lookup"><span data-stu-id="719ba-117">In addition, the following additional restrictions are imposed on Category 1 schema objects:</span></span>

-   <span data-ttu-id="719ba-118">Sie können die folgenden Attribute eines Attributs der Kategorie 1 nicht ändern:</span><span class="sxs-lookup"><span data-stu-id="719ba-118">You cannot change the following attributes of a Category 1 attribute:</span></span>

    -   <span data-ttu-id="719ba-119">**rangeLower** und **rangeUpper** (Wertebereich).</span><span class="sxs-lookup"><span data-stu-id="719ba-119">**rangeLower** and **rangeUpper** (value range).</span></span>
    -   <span data-ttu-id="719ba-120">**attributeSecurityGuid** (bestimmt, in welchem Eigenschafts Satz das Attribut ggf. zu gehört).</span><span class="sxs-lookup"><span data-stu-id="719ba-120">**attributeSecurityGuid** (determines which property set the attribute belongs in, if any).</span></span>

-   <span data-ttu-id="719ba-121">Die **defaultobjectcategory** einer Klasse der Kategorie 1 kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="719ba-121">You cannot change the **defaultObjectCategory** of a Category 1 class.</span></span>
-   <span data-ttu-id="719ba-122">Sie können die **objectCategory** einer beliebigen Instanz einer Klasse der Kategorie 1 nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="719ba-122">You cannot change the **objectCategory** of any instance of a Category 1 class.</span></span>
-   <span data-ttu-id="719ba-123">Es ist nicht möglich, eine Klasse oder ein Attribut der Kategorie 1 zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="719ba-123">You cannot make a Category 1 class or attribute defunct.</span></span>
-   <span data-ttu-id="719ba-124">Es ist nicht möglich, den **ldapDisplayName** einer Klasse oder eines Attributs der Kategorie 1 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="719ba-124">You cannot change the **lDAPDisplayName** of a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="719ba-125">Sie können eine Klasse oder ein Attribut der Kategorie 1 nicht umbenennen.</span><span class="sxs-lookup"><span data-stu-id="719ba-125">You cannot rename a Category 1 class or attribute.</span></span>

 

 




