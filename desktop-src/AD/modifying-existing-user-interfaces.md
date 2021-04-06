---
title: Ändern vorhandener Benutzeroberflächen
description: Im Ergebnisbereich des MMC-Snap-Ins "Active Directory-Benutzer und-Computer" werden mehrere Spalten mit Attributdaten für Objekte in einem Container angezeigt, z. b. die Attribute "Name" und "Description".
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Ändern vorhandener Benutzeroberflächen anzeigen
- AD-Snap-in "Benutzer und Computer", Ändern der Anzeige
- AD-Snap-in "Benutzer und Computer", Hinzufügen von Spalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855407"
---
# <a name="modifying-existing-user-interfaces"></a><span data-ttu-id="0e8b1-106">Ändern vorhandener Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="0e8b1-106">Modifying Existing User Interfaces</span></span>

<span data-ttu-id="0e8b1-107">Im Ergebnisbereich des MMC-Snap-Ins "Active Directory-Benutzer und-Computer" werden mehrere Spalten mit Attributdaten für Objekte in einem Container angezeigt, z. b. die Attribute " **Name** " und " **Description** ".</span><span class="sxs-lookup"><span data-stu-id="0e8b1-107">The results pane of the Active Directory Users and Computers MMC snap-in displays several columns of attribute data for objects within a container, such as the **Name** and **Description** attributes.</span></span> <span data-ttu-id="0e8b1-108">Das Snap-in ermöglicht dem Benutzer das Hinzufügen und Entfernen der Spalten, die im Ergebnisbereich des Snap-Ins angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-108">The snap-in enables the user to add and remove the columns displayed in the results pane of the snap-in.</span></span>

<span data-ttu-id="0e8b1-109">Um die Anzeige zu ändern, verwendet der Benutzer das Pulldownmenü **anzeigen** und wählt **Spalten hinzufügen/entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-109">To change the display, the user uses the **View** pull-down menu and selects **Add/Remove Columns**.</span></span> <span data-ttu-id="0e8b1-110">Im Dialogfeld **Spalten hinzufügen/entfernen** finden Sie eine Liste der Spalten, aus denen der Benutzer auswählen kann, um ihn im Ergebnisbereich anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-110">In the **Add/Remove Columns** dialog box, there is a list of columns that the user can choose from to display in the results pane.</span></span>

<span data-ttu-id="0e8b1-111">Das MMC-Snap-in "Active Directory-Benutzer und-Computer", das in Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition und Windows Server 2003, Datacenter Edition enthalten ist, bietet die Möglichkeit, die Liste der Spalten zu ändern, die im Ergebnisbereich des Snap-Ins für einen Container angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-111">The Active Directory Users and Computers MMC snap-in that is included with Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition, provides the ability to modify the list of columns that can be displayed in the results pane of the snap-in for a container.</span></span> <span data-ttu-id="0e8b1-112">Diese Funktion ist nur vorhanden, wenn das-Snap-in auf eine Gesamtstruktur mit Windows Server 2003-Schema ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-112">This feature only exists if the snap-in is targeted at a forest with Windows Server 2003 schema.</span></span>

<span data-ttu-id="0e8b1-113">Um der Liste eine Spalte hinzuzufügen, fügen Sie dem **extraColumns** -Attribut des Anzeige Spezifizierers einen Wert für den Objekttyp hinzu, dem das Attribut zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-113">To add a column to the list, add a value to the **extraColumns** attribute of the display specifier for the object type that the attribute is associated with.</span></span> <span data-ttu-id="0e8b1-114">Das **extraColumns** -Attribut ist ein mehr wertiges Zeichen folgen Attribut, bei dem jede Zeichenfolge das folgende Format hat.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-114">The **extraColumns** attribute is a multi-valued string attribute where each string is in the following format.</span></span>


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



<span data-ttu-id="0e8b1-115">In der folgenden Tabelle sind die Inhalte dieser Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-115">The following table lists the contents of these values.</span></span>



| <span data-ttu-id="0e8b1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0e8b1-116">Value</span></span>                        | <span data-ttu-id="0e8b1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e8b1-117">Description</span></span>                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8b1-118">" &lt; ldapDisplayName &gt; "</span><span class="sxs-lookup"><span data-stu-id="0e8b1-118">"&lt;ldapdisplayname&gt;"</span></span>    | <span data-ttu-id="0e8b1-119">Enthält eine Zeichenfolge, die den **ldapDisplayName** des Attributs darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-119">Contains a string that represents the **ldapDisplayName** of the attribute.</span></span>                                                         |
| <span data-ttu-id="0e8b1-120">" &lt; Spalten Kopfzeile &gt; "</span><span class="sxs-lookup"><span data-stu-id="0e8b1-120">"&lt;column header&gt;"</span></span>      | <span data-ttu-id="0e8b1-121">Enthält eine Zeichenfolge, die den Text darstellt, der im Header der Spalte angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-121">Contains a string that represents the text displayed in the header for the column.</span></span>                                                  |
| <span data-ttu-id="0e8b1-122">" &lt; Standard Sichtbarkeit &gt; "</span><span class="sxs-lookup"><span data-stu-id="0e8b1-122">"&lt;default visibility&gt;"</span></span> | <span data-ttu-id="0e8b1-123">Enthält einen numerischen Wert, der 0 (null) ist, wenn das Attribut standardmäßig ausgeblendet ist, oder 1, wenn das Attribut standardmäßig sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-123">Contains a numeric value that is 0 if the attribute is hidden by default or 1 if the attribute is visible by default.</span></span>               |
| <span data-ttu-id="0e8b1-124">" &lt; Width &gt; "</span><span class="sxs-lookup"><span data-stu-id="0e8b1-124">"&lt;width&gt;"</span></span>              | <span data-ttu-id="0e8b1-125">Enthält die Breite der Spalte in Pixel.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-125">Contains the width of the column, in pixels.</span></span> <span data-ttu-id="0e8b1-126">Wenn dieser Wert-1 ist, wird die Breite der Spalte auf die Breite des Spalten Headers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-126">If this value is -1, the width of the column is set to the width of the column header.</span></span> |
| <span data-ttu-id="0e8b1-127">"nicht &lt; verwendet &gt; "</span><span class="sxs-lookup"><span data-stu-id="0e8b1-127">"&lt;unused&gt;"</span></span>             | <span data-ttu-id="0e8b1-128">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-128">Unused.</span></span> <span data-ttu-id="0e8b1-129">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-129">Must be zero.</span></span>                                                                                                               |



 

<span data-ttu-id="0e8b1-130">Um z. b. eine Spalte hinzuzufügen, die den kanonischen Namen für Objekte in einer Organisationseinheit anzeigt, wird ein Wert für das Attribut " **CanonicalName** " dem Attribut " **extraColumns** " des Objekts " **organizationalUnit-Display** " im Container "Anzeige spezifiker" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-130">For example, to add a column that will display the canonical name for objects in an organizational unit, a value for the **canonicalName** attribute is added to the **extraColumns** attribute of the **organizationalUnit-Display** object in the display specifiers container.</span></span> <span data-ttu-id="0e8b1-131">Die Zeichenfolge, die dem **extraColumns** -Attribut des **organizationalUnit-Display-** Objekts hinzugefügt wird, sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-131">The string added to the **extraColumns** attribute of the **organizationalUnit-Display** object will look like the following.</span></span>


```C++
canonicalName,Canonical Name,0,150,0
```



<span data-ttu-id="0e8b1-132">Im Dialogfeld **Spalten hinzufügen/entfernen** werden nur die Spalten angezeigt, die im **extraColumns** -Attribut des **displaySpecifier** -Objekts des angezeigten Container Typs enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-132">The **Add/Remove Columns** dialog box displays only the columns that are contained in the **extraColumns** attribute of the **displaySpecifier** object of the container type that is being displayed.</span></span> <span data-ttu-id="0e8b1-133">Wenn das **extraColumns** -Attribut keine Werte enthält, wird im Dialogfeld **Spalten hinzufügen/entfernen** ein fester Satz von Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-133">If the **extraColumns** attribute does not contain any values, the **Add/Remove Columns** dialog box will display a fixed set of columns.</span></span> <span data-ttu-id="0e8b1-134">Eine Kopie des fixierten Satzes von Spalten ist im **extraColumns** -Attribut des **default-Display-** Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-134">A copy of the fixed set of columns is contained in the **extraColumns** attribute of the **default-Display** object.</span></span>

<span data-ttu-id="0e8b1-135">Wenn Sie einer Spaltenliste für ein bestimmtes Objekt eine oder mehrere Spalten hinzufügen möchten, müssen Sie alle **extraColumns** -Werte aus dem **default-Display-** Objekt in das Zielobjekt kopieren und dann die benutzerdefinierten Spalten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-135">To add one or more columns to the list of columns for a specific object, you must copy all of the **extraColumns** values from the **default-Display** object to the target object and then add the custom columns.</span></span> <span data-ttu-id="0e8b1-136">Wenn Sie das **extraColumns** -Attribut für eine bestimmte Klasse angeben, werden diese Spalten von dieser Klasse verwendet und nicht mit den Spalten zusammengeführt, die in der **default-Display-** Klasse angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-136">If you specify the **extraColumns** attribute on a given class, then that class will use those columns and will not merge them with the columns that are specified in the **default-Display** class.</span></span> <span data-ttu-id="0e8b1-137">Folglich haben weitere Änderungen an der **default-Display-** Klasse keine Auswirkung auf dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-137">Therefore, further changes to the **default-Display** class will have no effect on that object.</span></span>

<span data-ttu-id="0e8b1-138">Wenn Sie eine benutzerdefinierte Spalte für alle Containertypen anzeigen möchten, für die keine benutzerdefinierten Spalten registriert sind, fügen Sie dem **extraColumns** -Attribut des **default-Display-** Objekts einen Wert für die Spalte hinzu.</span><span class="sxs-lookup"><span data-stu-id="0e8b1-138">To display a custom column for all container types that do not have any custom columns registered, add a value for the column to the **extraColumns** attribute of the **default-Display** object.</span></span>

 

 




