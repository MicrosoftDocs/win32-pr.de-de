---
title: Benennungs Attribute und-Klassen
description: Dieses Thema enthält Richtlinien für die Benennung von Attributen und Klassen.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Benennungs Attribute und-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "106339528"
---
# <a name="naming-attributes-and-classes"></a><span data-ttu-id="6ebc3-104">Benennungs Attribute und-Klassen</span><span class="sxs-lookup"><span data-stu-id="6ebc3-104">Naming Attributes and Classes</span></span>

<span data-ttu-id="6ebc3-105">Dieses Thema enthält Richtlinien für die Benennung von Attributen und Klassen.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-105">This topic includes guidelines for naming attributes and classes.</span></span>

<span data-ttu-id="6ebc3-106">Um eine neue Klasse oder ein neues Attribut zu erstellen, befolgen Sie die folgenden Benennungs Regeln:</span><span class="sxs-lookup"><span data-stu-id="6ebc3-106">To create a new class or attribute, adhere to the following naming rules:</span></span>

-   <span data-ttu-id="6ebc3-107">Verwenden Sie den gleichen Namen für die **CN** -Eigenschaft und die **ldapDisplayName** -Eigenschaft eines neuen **attributeSchema** -oder **classSchema** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-107">Use the same name for both the **cn** and **lDAPDisplayName** properties of a new **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="6ebc3-108">Identifizieren Sie das Unternehmen mit einem Kleinbuchstaben-Präfix im ersten Abschnitt des Namens.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-108">Identify the company with a lower-case prefix in the first section of the name.</span></span> <span data-ttu-id="6ebc3-109">Dieses Präfix kann ein DNS-Name, ein Akronym oder eine andere Zeichenfolge sein, die das Unternehmen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-109">This prefix can be a DNS name, acronym, or other string that uniquely identifies the company.</span></span> <span data-ttu-id="6ebc3-110">Mit dem Präfix wird sichergestellt, dass alle Attribute und Klassen für ein bestimmtes Unternehmen beim Durchsuchen des Schemas nacheinander angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-110">The prefix ensures that all attributes and classes for a specific company are displayed consecutively when browsing the schema.</span></span>
-   <span data-ttu-id="6ebc3-111">Wenn Sie eine Schema Erweiterung als unabhängigen Softwarehersteller entwickeln, fügen Sie eine Abkürzung des Produkt namens des Präfix hinzu.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-111">If you are developing a schema extension as an independent software vendor, add an abbreviation of the product name of the prefix.</span></span> <span data-ttu-id="6ebc3-112">Dadurch wird die Unterscheidung zwischen mehreren Produkten hinzugefügt, die LDAP-Schema Erweiterungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-112">This adds distinction between multiple products that contain LDAP schema extensions.</span></span>
-   <span data-ttu-id="6ebc3-113">Verwenden Sie einen Bindestrich als das nächste Zeichen nach dem Präfix.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-113">Use a hyphen as the next character after the prefix.</span></span>
-   <span data-ttu-id="6ebc3-114">Geben Sie einen Attribut-oder Klassennamen an, der innerhalb des Unternehmens Attributs nach dem Bindestrich eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-114">Specify an attribute or class name that is unique within the company's attributes after the hyphen.</span></span> <span data-ttu-id="6ebc3-115">Dieser Teil des allgemeinen namens sollte beschreibend sein.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-115">This part of the common-name should be descriptive.</span></span> <span data-ttu-id="6ebc3-116">Verwenden Sie keine unlogisch-Namen, die für Entwickler und Viewer des Schemas bedeutungslos sind.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-116">Do not use illogical names that are meaningless to developers and viewers of the schema.</span></span>

<span data-ttu-id="6ebc3-117">Wenn beispielsweise das fiktive Fabrikam-Unternehmen das Schema durch Hinzufügen eines Attributs zum Speichern eines sprach-e-Mail-Bezeichners erweitert hat, könnte **CN** und **ldapDisplayName** des neuen Attributs "Fabrikam-voicemailid" lauten.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-117">For example, if the fictitious Fabrikam company extended the schema by adding an attribute for storing a voice-mail identifier, the **cn** and **lDAPDisplayName** of the new attribute could be "fabrikam-VoiceMailID".</span></span>

<span data-ttu-id="6ebc3-118">Wenn der **ldapDisplayName** eines Attributs oder einer Klasse nicht angegeben ist, verwendet das System den **CN** zum Generieren eines Attributs.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-118">If the **lDAPDisplayName** of an attribute or class is not specified, the system uses the **cn** to generate one.</span></span> <span data-ttu-id="6ebc3-119">Der System Algorithmus zum Erstellen des Namens kann jedoch zu Namenskollisionen oder Namen führen, die schwer lesbar sind.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-119">However, the system algorithm for generating the name may result in name collisions or names that are difficult to read.</span></span> <span data-ttu-id="6ebc3-120">Um diese Probleme zu vermeiden, wird empfohlen, dass ein **ldapDisplayName** für alle Attribute und Klassen explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-120">To avoid these problems, it is recommended that an **lDAPDisplayName** be explicitly specified for all attributes and classes.</span></span>

<span data-ttu-id="6ebc3-121">Zu Entwicklungs-und Testzwecken ist es möglicherweise wünschenswert, ein Versions Suffix an **CN** und **ldapDisplayName** anzufügen, z. b. "Fabrikam-voicemailid-001".</span><span class="sxs-lookup"><span data-stu-id="6ebc3-121">For development and testing purposes, it may be desirable to append a version suffix to the **cn** and **lDAPDisplayName**, for example, "fabrikam-VoiceMailID-001".</span></span> <span data-ttu-id="6ebc3-122">In einer verteilten Entwicklungs-/Testumgebung können Entwickler mit einem Versions Suffix mehrere Versionen Ihrer Software gleichzeitig ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-122">In a distributed development/test environment, a version suffix enables developers to run multiple versions of their software simultaneously.</span></span> <span data-ttu-id="6ebc3-123">Benennen Sie nach Abschluss der Tests das Attribut oder die Klasse um, um das Suffix zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-123">After testing is complete, rename the attribute or class to remove the suffix.</span></span>

<span data-ttu-id="6ebc3-124">Es ist nicht möglich, veraltete Versionen von Schema Erweiterungen zu löschen, aber es ist möglich, Sie zu deaktivieren und Sie mit nicht verfallenen Namen umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="6ebc3-124">It is not possible to delete defunct versions of a schema extensions, but it is possible to disable them and rename them with obscure names.</span></span> <span data-ttu-id="6ebc3-125">Weitere Informationen finden Sie unter [Deaktivieren vorhandener Klassen und Attribute](disabling-existing-classes-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6ebc3-125">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

 

 




