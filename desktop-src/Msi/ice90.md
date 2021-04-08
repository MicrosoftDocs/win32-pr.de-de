---
description: ICE90 gibt eine Warnung aus, wenn feststellt, dass das Verzeichnis einer Verknüpfung als öffentliche Eigenschaft angegeben wurde.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864224"
---
# <a name="ice90"></a><span data-ttu-id="8c324-103">ICE90</span><span class="sxs-lookup"><span data-stu-id="8c324-103">ICE90</span></span>

<span data-ttu-id="8c324-104">ICE90 gibt eine Warnung aus, wenn feststellt, dass das Verzeichnis einer Verknüpfung als öffentliche Eigenschaft angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8c324-104">ICE90 posts a warning if it finds that a shortcut's directory has been specified as a public property.</span></span> <span data-ttu-id="8c324-105">Die Namen [öffentlicher Eigenschaften](public-properties.md) werden in Großbuchstaben geschrieben.</span><span class="sxs-lookup"><span data-stu-id="8c324-105">The names of [Public Properties](public-properties.md) are written in uppercase letters.</span></span> <span data-ttu-id="8c324-106">Eine von einer öffentlichen Eigenschaft angegebene Verknüpfung funktioniert möglicherweise nicht, wenn sich der Wert der [**ALLUSERS**](allusers.md) -Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="8c324-106">A shortcut specified by a public property may not work if the value of the [**ALLUSERS**](allusers.md) property changes.</span></span>

<span data-ttu-id="8c324-107">Diese benutzerdefinierte Ice-Aktion überprüft die Verknüpfungs Tabelle und verwendet die Verzeichnis Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8c324-107">This ICE custom action validates the Shortcut table and uses the Directory table.</span></span> <span data-ttu-id="8c324-108">Wenn die Verzeichnis Tabelle nicht vorhanden ist, wird Sie ohne Überprüfung der Verknüpfungs Tabelle zurückgegeben, und es werden keine Fehler oder Warnungen ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c324-108">If the Directory table is not present, it returns without validating the Shortcut table and posts no errors or warnings.</span></span>

## <a name="result"></a><span data-ttu-id="8c324-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="8c324-109">Result</span></span>

<span data-ttu-id="8c324-110">ICE90 gibt die folgende Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="8c324-110">ICE90 posts the following warning.</span></span>



| <span data-ttu-id="8c324-111">ICE90-Fehler</span><span class="sxs-lookup"><span data-stu-id="8c324-111">ICE90 error</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="8c324-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c324-112">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="8c324-113">Die Verknüpfung ' \[ 1 \] ' weist ein Verzeichnis auf, das eine öffentliche Eigenschaft (Alle Caps) und das Benutzerprofil Verzeichnis ist.</span><span class="sxs-lookup"><span data-stu-id="8c324-113">The shortcut '\[1\]' has a directory that is a public property (ALL CAPS) and is under user profile directory.</span></span> <span data-ttu-id="8c324-114">Dies führt zu einem Problem, wenn der Wert der [**ALLUSERS**](allusers.md) -Eigenschaft in der UI-Sequenz geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8c324-114">This results in a problem if the value of the [**ALLUSERS**](allusers.md) property changes in the UI sequence.</span></span> | <span data-ttu-id="8c324-115">Das Verzeichnis einer Verknüpfung wurde als öffentliche Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="8c324-115">A shortcut's directory has been specified as a public property.</span></span> |



 

## <a name="example"></a><span data-ttu-id="8c324-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8c324-116">Example</span></span>

<span data-ttu-id="8c324-117">ICE90 meldet folgende Warnung für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8c324-117">ICE90 reports the following warning for the example:</span></span>

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

<span data-ttu-id="8c324-118">In diesem Beispiel befindet sich mydir unter einem Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="8c324-118">In this example, MYDIR is under a users profile.</span></span> <span data-ttu-id="8c324-119">ICE90 gibt eine Warnung aus, da der Speicherort des Zielverzeichnisses von der öffentlichen Eigenschaft mydir angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c324-119">ICE90 posts a warning because the location of the target directory is specified by a public property, MYDIR.</span></span> <span data-ttu-id="8c324-120">Ein Benutzer darf die Eigenschaft mydir oder [**ALLUSERS**](allusers.md) ändern.</span><span class="sxs-lookup"><span data-stu-id="8c324-120">A user may change MYDIR or [**ALLUSERS**](allusers.md) property.</span></span> <span data-ttu-id="8c324-121">Wenn für den [Installations Kontext](installation-context.md)pro Computer " **ALLUSERS** " festgelegt ist und sich "MyDir" unter einem Benutzerprofil befindet, wird die Verknüpfungs Datei in "MyDir" unter das Profil "alle Benutzer" und nicht auf das Profil eines bestimmten Benutzers kopiert.</span><span class="sxs-lookup"><span data-stu-id="8c324-121">If **ALLUSERS** is set for the per-machine [installation context](installation-context.md), and MYDIR is under a users profile, the shortcut file in MYDIR are copied under the "All Users" profile and not a particular user's profile.</span></span> <span data-ttu-id="8c324-122">Wenn für den pro-Benutzer-Installations Kontext **ALLUSERS** festgelegt ist, wird die Verknüpfungs Datei in mydir in das Profil eines bestimmten Benutzers kopiert und ist für andere Benutzer nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c324-122">If **ALLUSERS** is set for the per-user installation context, the shortcut file in MYDIR is copied into a particular user's profile and is not available to other users.</span></span>

<span data-ttu-id="8c324-123">Verknüpfungs [Tabelle](shortcut-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="8c324-123">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="8c324-124">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="8c324-124">Shortcut</span></span>  | <span data-ttu-id="8c324-125">Verzeichnis\_</span><span class="sxs-lookup"><span data-stu-id="8c324-125">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="8c324-126">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="8c324-126">Shortcut1</span></span> | <span data-ttu-id="8c324-127">"MyDir"</span><span class="sxs-lookup"><span data-stu-id="8c324-127">MYDIR</span></span>       |



 

<span data-ttu-id="8c324-128">[Verzeichnis Tabelle](directory-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="8c324-128">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="8c324-129">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8c324-129">Directory</span></span> | <span data-ttu-id="8c324-130">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8c324-130">Directory\_Parent</span></span> |
|-----------|-------------------|
| <span data-ttu-id="8c324-131">"MyDir"</span><span class="sxs-lookup"><span data-stu-id="8c324-131">MYDIR</span></span>     | <span data-ttu-id="8c324-132">Programmmenufolder</span><span class="sxs-lookup"><span data-stu-id="8c324-132">ProgramMenuFolder</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8c324-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c324-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c324-134">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="8c324-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



