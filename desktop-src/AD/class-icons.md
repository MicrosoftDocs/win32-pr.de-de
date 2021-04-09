---
title: Klassen Symbole
description: Das Symbol, das zum Darstellen eines Klassen Objekts verwendet wird, kann im IconPath-Attribut im displaySpecifier-Container angegeben werden.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- Klassen Anzeige Namen AD, Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948588"
---
# <a name="class-icons"></a><span data-ttu-id="81c09-104">Klassen Symbole</span><span class="sxs-lookup"><span data-stu-id="81c09-104">Class Icons</span></span>

<span data-ttu-id="81c09-105">Das Symbol, das zum Darstellen eines Klassen Objekts verwendet wird, kann im **IconPath** -Attribut im displaySpecifier-Container angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81c09-105">The icon used to represent a class object can be specified in the **iconPath** attribute in the DisplaySpecifiers container.</span></span> <span data-ttu-id="81c09-106">Darüber hinaus kann jede Klasse mehrere Symbol Zustände speichern.</span><span class="sxs-lookup"><span data-stu-id="81c09-106">Moreover, each class can store multiple icon states.</span></span> <span data-ttu-id="81c09-107">Beispielsweise kann eine Ordner Klasse Symbole für den Status "geöffnet", "geschlossen" und "deaktiviert" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="81c09-107">For example, a folder class can have icons for the open, closed, and disabled states.</span></span> <span data-ttu-id="81c09-108">Die aktuelle Implementierung akzeptiert maximal sechzehn verschiedene Symbol Zustände pro Klasse.</span><span class="sxs-lookup"><span data-stu-id="81c09-108">The current implementation accepts a maximum of sixteen different icon states per class.</span></span>

<span data-ttu-id="81c09-109">Das **IconPath** -Attribut kann auf zwei Arten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81c09-109">The **iconPath** attribute can be specified in one of two ways.</span></span>


```C++
<state>,<icon file name>
```



<span data-ttu-id="81c09-110">oder</span><span class="sxs-lookup"><span data-stu-id="81c09-110">or</span></span>


```C++
<state>,<module file name>,<resource ID>
```



<span data-ttu-id="81c09-111">In diesen Beispielen &lt; ist "State &gt; " eine ganze Zahl mit einem Wert zwischen 0 und 15.</span><span class="sxs-lookup"><span data-stu-id="81c09-111">In these examples, the "&lt;state&gt;" is an integer with a value between 0 and 15.</span></span> <span data-ttu-id="81c09-112">Der Wert 0 wird als Standard-oder Closed-Zustand des Symbols definiert.</span><span class="sxs-lookup"><span data-stu-id="81c09-112">The value 0 is defined to be the default or closed state of the icon.</span></span> <span data-ttu-id="81c09-113">Der Wert 1 wird als offener Zustand des Symbols definiert.</span><span class="sxs-lookup"><span data-stu-id="81c09-113">The value 1 is defined to be the open state of the icon.</span></span> <span data-ttu-id="81c09-114">Der Wert 2 ist der deaktivierte Zustand.</span><span class="sxs-lookup"><span data-stu-id="81c09-114">The value 2 is the disabled state.</span></span> <span data-ttu-id="81c09-115">Alle anderen Werte sind Anwendungs definiert.</span><span class="sxs-lookup"><span data-stu-id="81c09-115">All other values are application-defined.</span></span>

<span data-ttu-id="81c09-116">Der Name der Symbol &lt; Datei &gt; ist der Pfad und Dateiname einer Symbol Datei, die das Symbolbild enthält.</span><span class="sxs-lookup"><span data-stu-id="81c09-116">The "&lt;icon file name&gt;" is the path and file name of an icon file that contains the icon image.</span></span>

<span data-ttu-id="81c09-117">Der " &lt; Modul Dateiname &gt; " ist der Pfad und Dateiname eines Moduls, z. b. eine exe-oder DLL-Datei, die das Symbolbild in einer Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="81c09-117">The "&lt;module file name&gt;" is the path and file name of a module, such as an EXE or DLL, that contains the icon image in a resource.</span></span> <span data-ttu-id="81c09-118">Die " &lt; Ressourcen-ID &gt; " ist eine ganze Zahl, die den Ressourcen Bezeichner der Symbol Ressource im Modul angibt.</span><span class="sxs-lookup"><span data-stu-id="81c09-118">The "&lt;resource ID&gt;" is an integer that specifies the resource identifier of the icon resource within the module.</span></span>

## <a name="adding-a-value-to-the-iconpath-attribute"></a><span data-ttu-id="81c09-119">Hinzufügen eines Werts zum **IconPath** -Attribut</span><span class="sxs-lookup"><span data-stu-id="81c09-119">Adding a Value to the **iconPath** Attribute</span></span>

<span data-ttu-id="81c09-120">Um dem **IconPath** -Attribut einen Wert hinzuzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="81c09-120">To add a value to the **iconPath** attribute, perform the following steps.</span></span>

1.  <span data-ttu-id="81c09-121">Stellen Sie fest, ob der Wert für das Attribut vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="81c09-121">Determine if the value for the attribute exists.</span></span> <span data-ttu-id="81c09-122">Wenn ein Wert ersetzt werden soll, löschen Sie zuerst den vorhandenen Wert mithilfe der [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode, wobei der Parameter *lncontrolcode* auf **ADS \_ Property \_ Delete** und der *vprop* -Parameter auf den zu entfernenden Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="81c09-122">If a value is to be replaced, first, delete the existing value using the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_DELETE** and the *vProp* parameter set to the value to be removed.</span></span> <span data-ttu-id="81c09-123">Verwenden Sie nicht die **ADS- \_ Eigenschaft \_ Clear** oder **ADS \_ Property \_ Update** für *lncontrolcode*.</span><span class="sxs-lookup"><span data-stu-id="81c09-123">Do not use **ADS\_PROPERTY\_CLEAR** or **ADS\_PROPERTY\_UPDATE** for *lnControlCode*.</span></span>
2.  <span data-ttu-id="81c09-124">Erstellen Sie die Zeichenfolge, die die Attribut Symbol Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="81c09-124">Create the string that represents the attribute icon data.</span></span> <span data-ttu-id="81c09-125">Ein Beispiel finden Sie im obigen Format.</span><span class="sxs-lookup"><span data-stu-id="81c09-125">For an example, see the format above.</span></span>
3.  <span data-ttu-id="81c09-126">Wenn Sie den neuen Wert hinzufügen möchten, verwenden Sie die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode, wobei der *lncontrolcode* -Parameter auf **ADS- \_ Eigenschaft \_ Append** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="81c09-126">To add the new value, use the [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method with the *lnControlCode* parameter set to **ADS\_PROPERTY\_APPEND**.</span></span>
4.  <span data-ttu-id="81c09-127">Um die Änderungen im Verzeichnis zu übertragen, nennen Sie [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="81c09-127">To commit changes to the directory, call [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 