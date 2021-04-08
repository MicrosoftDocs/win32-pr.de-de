---
title: Abrufen einer Link-ID
description: Ab Windows Server 2003 ist es nicht mehr erforderlich, ein linkid von Microsoft anzufordern. Es gibt einen Prozess zum automatischen Erstellen eines linkid.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Abrufen einer Link-ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101439"
---
# <a name="obtaining-a-link-id"></a><span data-ttu-id="ec5fe-104">Abrufen einer Link-ID</span><span class="sxs-lookup"><span data-stu-id="ec5fe-104">Obtaining a Link ID</span></span>

<span data-ttu-id="ec5fe-105">Ab Windows Server 2003 ist es nicht mehr erforderlich, ein [**linkid**](/windows/desktop/ADSchema/a-linkid) von Microsoft anzufordern. Es gibt einen Prozess zum automatischen Erstellen eines **linkid**.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-105">Starting with Windows Server 2003, it is no longer necessary to request a [**linkID**](/windows/desktop/ADSchema/a-linkid) from Microsoft; there is a process for automatically generating a **linkID**.</span></span> <span data-ttu-id="ec5fe-106">Das System generiert automatisch eine Link-ID für ein neues Verknüpftes Attribut, wenn das **linkid** -Attribut des Attributs auf 1.2.840.113556.1.2.50 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-106">The system will automatically generate a link ID for a new linked attribute when the attribute's **linkID** attribute is set to 1.2.840.113556.1.2.50.</span></span> <span data-ttu-id="ec5fe-107">Ein Backlink für diesen vorwärts Link wird erstellt, indem der " **linkid** " auf " [**attributeId**](/windows/desktop/ADSchema/a-attributeid) " oder " [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) " des vorwärts links festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-107">A back link for this forward link is created by setting the **linkID** to the [**attributeID**](/windows/desktop/ADSchema/a-attributeid) or [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) of the forward link.</span></span> <span data-ttu-id="ec5fe-108">Der Schema Cache muss erneut geladen werden, nachdem der Forward-Link und vor dem Erstellen des Backlinks erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-108">The schema cache must be reloaded after creating the forward link and before creating the back link.</span></span> <span data-ttu-id="ec5fe-109">Andernfalls wird die **attributeId** oder der **ldapDisplayName** des vorwärts Links beim Erstellen des Backlinks nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-109">Otherwise, the forward link's **attributeId** or **ldapDisplayName** will not be found when the back link is created.</span></span> <span data-ttu-id="ec5fe-110">Der Schema Cache wird nach Bedarf neu geladen, ein paar Minuten nach dem durchgeführt einer Schema Änderung oder beim Neustart des DC.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-110">The schema cache is reloaded on demand, a few minutes after a schema change is made, or when the DC is restarted.</span></span> <span data-ttu-id="ec5fe-111">Erstellen Sie alle vorwärts Verknüpfungen, laden Sie den Schema Cache neu, und erstellen Sie dann alle Backlinks.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-111">Create all forward links, reload the schema cache and then create all back links.</span></span>

<span data-ttu-id="ec5fe-112">Wenn Sie z. b. die neuen Attribute **myforwardlinkattr** und **mybacklinkattr** erstellt haben und diese verknüpfen möchten:</span><span class="sxs-lookup"><span data-stu-id="ec5fe-112">For example, when you have created the new attributes **myForwardLinkAttr** and **myBackLinkAttr**, and wish to link them:</span></span>

> [!Note]  
> <span data-ttu-id="ec5fe-113">Die OIDs in diesem Beispiel sind erfunden.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-113">The OIDs in this example are contrived.</span></span> <span data-ttu-id="ec5fe-114">Anweisungen zum Abrufen von OIDs für neue Attribute finden Sie unter Abrufen [eines Objekt Bezeichners von Microsoft](obtaining-an-object-identifier-from-microsoft.md) .</span><span class="sxs-lookup"><span data-stu-id="ec5fe-114">See [Obtaining an Object Identifier from Microsoft](obtaining-an-object-identifier-from-microsoft.md) for instructions on obtaining OIDs for new attributes.</span></span>

 

1.  <span data-ttu-id="ec5fe-115">Legen Sie diese Attribute für das Attribut fest, das der Forward-Link sein soll:</span><span class="sxs-lookup"><span data-stu-id="ec5fe-115">Set these attributes on the attribute that is to be the forward link:</span></span>
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  <span data-ttu-id="ec5fe-116">Erneutes Laden des Schemas.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-116">Reload the Schema.</span></span>
3.  <span data-ttu-id="ec5fe-117">Legen Sie diese Attribute für das Attribut fest, das als Backlink festgelegt werden soll:</span><span class="sxs-lookup"><span data-stu-id="ec5fe-117">Set these attributes on the attribute that is to be the back link:</span></span>
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a><span data-ttu-id="ec5fe-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec5fe-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec5fe-119">Verknüpfte Attribute</span><span class="sxs-lookup"><span data-stu-id="ec5fe-119">Linked Attributes</span></span>](linked-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec5fe-120">Erweitern des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec5fe-120">How to Extend the Schema</span></span>](how-to-extend-the-schema.md)
</dt> </dl>

 

 