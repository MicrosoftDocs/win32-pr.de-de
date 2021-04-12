---
title: Klassen-und Attribut anzeigen Amen
description: Dieses Thema enthält Informationen zu und Richtlinien für Klassen-und Attribut anzeigen Amen.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- Anzeige Spezifizierer anzeigen, Klassen-und Attribut anzeigen Amen
- Klassen Anzeige Namen AD
- anzeigen amen des Attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472669"
---
# <a name="class-and-attribute-display-names"></a><span data-ttu-id="552eb-106">Klassen-und Attribut anzeigen Amen</span><span class="sxs-lookup"><span data-stu-id="552eb-106">Class and Attribute Display Names</span></span>

<span data-ttu-id="552eb-107">Der Anzeige Bezeichner für eine Objektklasse enthält die folgenden Attribute, die verwendet werden können, um die lokalisierten anzeigen Amen anzugeben, die in der Benutzeroberfläche für Objekte dieser Klasse verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="552eb-107">The display specifier for an object class contains the following attributes that can be used to specify the localized display names used in the UI for objects of that class:</span></span>

-   <span data-ttu-id="552eb-108">Das **classdisplayname** -Attribut ist eine Einzelwert-Unicode-Zeichenfolge, die den Klassen anzeigen Amen angibt.</span><span class="sxs-lookup"><span data-stu-id="552eb-108">The **classDisplayName** attribute is a single-value Unicode string that specifies the class display name.</span></span>
-   <span data-ttu-id="552eb-109">Das **attributeDisplayNames** -Attribut ist eine mehrwertige Eigenschaft, die die Namen angibt, die in der Benutzeroberfläche für Attribute der Objektklasse verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="552eb-109">The **attributeDisplayNames** attribute is a multi-value property that specifies the names to use in the UI for attributes of the object class.</span></span>

<span data-ttu-id="552eb-110">Die **attributeDisplayNames** -Werte sind Unicode-Zeichen folgen. jedes Element besteht aus einem durch Trennzeichen getrennten namens paar:</span><span class="sxs-lookup"><span data-stu-id="552eb-110">The **attributeDisplayNames** values are Unicode strings; each element consists of a comma-delimited name pair:</span></span>


```C++
<attribute name>,<display text>
```



<span data-ttu-id="552eb-111">In diesem Beispiel ist " &lt; Attribut Name &gt; " der **ldapDisplayName** des Attributs, und " &lt; Anzeige Text &gt; " ist der Text, der als Name dieses Attributs in der Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="552eb-111">In this example, "&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute and "&lt;display text&gt;" is the text to display as the name of that attribute in the user interface.</span></span>

## <a name="guidelines-for-class-and-attribute-display-names"></a><span data-ttu-id="552eb-112">Richtlinien für Klassen-und Attribut anzeigen Amen</span><span class="sxs-lookup"><span data-stu-id="552eb-112">Guidelines for Class and Attribute Display Names</span></span>

<span data-ttu-id="552eb-113">Da viele Lieferanten Klassen mit neuen Attributen erweitern oder vollständig neue Klassen erstellen können, ist es wichtig, dass die anzeigen amen der Klasse und des Attributs eindeutig sind und keine Konflikte verursachen.</span><span class="sxs-lookup"><span data-stu-id="552eb-113">Because many vendors may extend classes with new attributes or creating entirely new classes, it is important that the class and attribute display names are unambiguous and do not result in conflicts.</span></span>

<span data-ttu-id="552eb-114">Jeder Anbieter sollte dem Namen der Klassen Anzeige einen eindeutigen, auf dem Herstellernamen basierenden Bezeichner als Präfix voranstellen.</span><span class="sxs-lookup"><span data-stu-id="552eb-114">Each vendor should prefix the class display name with a unique friendly identifier based on the vendor name.</span></span> <span data-ttu-id="552eb-115">Wenn z. b. das fiktive Unternehmen Fabrikam Inc. eine neue Klasse erstellt, die von der "Contact"-Klasse abgeleitet ist, können Sie einen eindeutigen Klassen anzeigen Amen mit dem Namen "Fabrikam Contact" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="552eb-115">For example, if the fictitious company, Fabrikam Inc., creates a new class derived from the "contact" class, they can have a unique class display name "Fabrikam Contact."</span></span>

<span data-ttu-id="552eb-116">Wenn ein Anbieter eine vorhandene Klasse mit neuen Attributen erweitert, sollte der Anzeige Name des Attributs erneut eindeutig identifiziert werden, sodass keine Konflikte mit anderen Attribut anzeigen Amen auftreten.</span><span class="sxs-lookup"><span data-stu-id="552eb-116">If a vendor extends an existing class with new attributes, they should again uniquely identify the attribute display name so that no conflicts occur with other attribute display names.</span></span> <span data-ttu-id="552eb-117">Auch hier empfiehlt es sich, den Attribut anzeigen Amen mit dem eindeutigen, auf dem Herstellernamen basierenden Bezeichner als präfixvorgang festzulegen.</span><span class="sxs-lookup"><span data-stu-id="552eb-117">Again, prefixing the attribute display name with unique friendly identifier based on the vendor name is good practice.</span></span> <span data-ttu-id="552eb-118">Wenn beispielsweise das Fabrikam-Unternehmen die User-Klasse mit einem neuen HR-Attribut erweitert, könnte es das Attribut eindeutig als "Fabrikam HR-Informationen" anzeigen.</span><span class="sxs-lookup"><span data-stu-id="552eb-118">For example, if the Fabrikam company extends the user class with a new HR attribute, they could uniquely display the attribute as "Fabrikam HR Information."</span></span>

<span data-ttu-id="552eb-119">Außerdem sollte jeder Anbieter aus Lokalisierungs Sicht die Klassen-und Attribut Anzeige Namen in jeder Sprache lokalisieren, die von Windows 2000 unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="552eb-119">In addition, from a localization perspective, each vendor should localize the class and attribute display names into each language supported by Windows 2000.</span></span>

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a><span data-ttu-id="552eb-120">Hinzufügen eines Werts zum attributeDisplayNames-Attribut</span><span class="sxs-lookup"><span data-stu-id="552eb-120">Adding a Value to the attributeDisplayNames Attribute</span></span>

<span data-ttu-id="552eb-121">**So fügen Sie dem **attributeDisplayNames** -Attribut einen Name-Zuordnungswert hinzu**</span><span class="sxs-lookup"><span data-stu-id="552eb-121">**To add a name mapping value to the **attributeDisplayNames** attribute**</span></span>

1.  <span data-ttu-id="552eb-122">Bestimmen Sie, ob der Name Zuordnungswert für das Attribut vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="552eb-122">Determine if the name mapping value for the attribute exists.</span></span> <span data-ttu-id="552eb-123">Wenn ein Name für die Namenszuordnung ersetzt werden soll, löschen Sie zuerst den vorhandenen Wert, indem Sie die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode verwenden, wobei der *lncontrolcode* -Parameter auf **ADS \_ Property \_ Delete** und der *vprop* -Parameter auf den zu entfernenden Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="552eb-123">If a name mapping value is to be replaced, first deleted the existing value, using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method, with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="552eb-124">Verwenden Sie nicht die **ADS- \_ Eigenschaft \_ Clear** oder **ADS \_ Property \_ Update** für *lncontrolcode*.</span><span class="sxs-lookup"><span data-stu-id="552eb-124">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="552eb-125">Erstellen Sie die Zeichenfolge, die den anzeigen amen des Attributs darstellt.</span><span class="sxs-lookup"><span data-stu-id="552eb-125">Create the string that represents the attribute display name.</span></span> <span data-ttu-id="552eb-126">Ein Beispiel finden Sie im obigen Format.</span><span class="sxs-lookup"><span data-stu-id="552eb-126">For an example, see the format above.</span></span>
3.  <span data-ttu-id="552eb-127">Verwenden Sie die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode, bei der der *lncontrolcode* -Parameter auf **ADS- \_ Eigenschaft \_ Append** festgelegt ist, um den neuen Wert hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="552eb-127">Use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND** to add the new value.</span></span>
4.  <span data-ttu-id="552eb-128">Ruft [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) auf, um die Änderungen im Verzeichnis zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="552eb-128">Call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>

<span data-ttu-id="552eb-129">Weitere Informationen zum Benennen neuer Klassen und Attribute finden Sie unter [Benennen von Attributen und Klassen](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="552eb-129">For more information about naming new classes and attributes, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span>

 

 