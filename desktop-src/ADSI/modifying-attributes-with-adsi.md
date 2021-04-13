---
title: Ändern von Attributen mit ADSI
description: Um Attributwerte zu ändern, stellt ADSI die Methoden IADs. Put und IADs. PutEx bereit. Mit diesen Methoden werden die Daten im Client seitigen Cache geändert. Die IADs. * tinfo-Methode muss aufgerufen werden, um die Änderungen im Verzeichnis zu übertragen.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Ändern von Attributen mit ADSI
- Attribute ADSI, ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391013"
---
# <a name="modifying-attributes-with-adsi"></a><span data-ttu-id="8f500-107">Ändern von Attributen mit ADSI</span><span class="sxs-lookup"><span data-stu-id="8f500-107">Modifying Attributes with ADSI</span></span>

<span data-ttu-id="8f500-108">Um Attributwerte zu ändern, stellt ADSI die Methoden [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) bereit.</span><span class="sxs-lookup"><span data-stu-id="8f500-108">To modify attribute values, ADSI provides the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) methods.</span></span> <span data-ttu-id="8f500-109">Mit diesen Methoden werden die Daten im Client seitigen Cache geändert.</span><span class="sxs-lookup"><span data-stu-id="8f500-109">These methods modify the data on the client-side cache.</span></span> <span data-ttu-id="8f500-110">Die [**IADs. \* tinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode muss aufgerufen werden, um die Änderungen im Verzeichnis zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="8f500-110">The [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method must be called to commit the changes to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="8f500-111">Wenn für mehrere Attribut Änderungen ein Commit in einem einzelnen [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)\*-Befehl ausgeführt wird, wenn ein einzelnes Attribut nicht geändert werden kann, wird keines der Attribute geändert.</span><span class="sxs-lookup"><span data-stu-id="8f500-111">When multiple attribute changes are committed in a single call to [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), if any single attribute cannot be modified, none of the attributes will be modified.</span></span> <span data-ttu-id="8f500-112">Wenn Sie z. b. die Attribute " [**SN**](/windows/desktop/ADSchema/a-sn) " und " [**givenName**](/windows/desktop/ADSchema/a-givenname) " ändern und das " [**telefonienumber**](/windows/desktop/ADSchema/a-telephonenumber) "-Attribut eines Benutzer Objekts ohne nachfolgende Aufrufe der **SetInfo** -Methode löschen, werden die Änderungen beim Aufrufen von **SetInfo** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="8f500-112">For example, if you modify the [**sn**](/windows/desktop/ADSchema/a-sn) and [**givenName**](/windows/desktop/ADSchema/a-givenname) attributes and clear the [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) attribute of a user object without any subsequent calls to the **SetInfo** method, the changes are entered when you call **SetInfo**.</span></span> <span data-ttu-id="8f500-113">Wenn eine oder mehrere der Änderungen nicht zulässig sind und daher nicht ausgeführt werden können, werden keine der an den Attributen vorgenommenen Änderungen beim \*\*Abrufen von "\*\*\*" eingegeben.</span><span class="sxs-lookup"><span data-stu-id="8f500-113">If one or more of the modifications are not allowed and therefore cannot be performed, then none of the collective modifications made to the attributes are entered during the call to **SetInfo**.</span></span>

 

<span data-ttu-id="8f500-114">Die [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) -Methode nimmt einen Attributnamen und einen Variant-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="8f500-114">The [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method takes an attribute name and a variant parameter.</span></span> <span data-ttu-id="8f500-115">Verwenden Sie diese Methode, um Attribute festzulegen, die sowohl einzelne als auch mehrere Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="8f500-115">Use this method to set attributes that contain both single and multiple values.</span></span>

<span data-ttu-id="8f500-116">Die [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode bietet Kontrolle über Vorgänge für mehrwertige Attribute.</span><span class="sxs-lookup"><span data-stu-id="8f500-116">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method provides control over operations on multi-valued attributes.</span></span> <span data-ttu-id="8f500-117">Sie können vorhandene Werte anfügen, löschen, aktualisieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="8f500-117">You can append, delete, update, and clear existing values.</span></span> <span data-ttu-id="8f500-118">Die **IADs. PutEx** -Methode erwartet immer ein Variant-Array von Attributwerten.</span><span class="sxs-lookup"><span data-stu-id="8f500-118">The **IADs.PutEx** method always expects a variant array of attribute values.</span></span> <span data-ttu-id="8f500-119">Sie können diese Methode jedoch auch verwenden, um ein Attribut mit einem einzelnen Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8f500-119">However, you can use this method to set an attribute with a single value as well.</span></span>

<span data-ttu-id="8f500-120">Die [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode verwendet die Vorgänge, die durch die Enumeration der [**ADS- \_ Eigenschafts \_ Operation \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8f500-120">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the operations specified by the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

 

 