---
description: In Windows 7 und höher können Sie den Eintrag Unterbefehle in der Registrierung verwenden, um Kaskadierende Menüs mithilfe der in diesem Thema beschriebenen Prozedur zu erstellen.
title: Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag Unterbefehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994694"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="3199b-103">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "Unterbefehle"</span><span class="sxs-lookup"><span data-stu-id="3199b-103">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="3199b-104">In Windows 7 und höher können Sie den Eintrag Unterbefehle in der Registrierung verwenden, um Kaskadierende Menüs mithilfe der in diesem Thema beschriebenen Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3199b-104">In Windows 7 and later, you can use the SubCommands entry in the registry to create cascading menus by using the procedure given in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="3199b-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="3199b-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="3199b-106">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="3199b-106">Step 1:</span></span>

<span data-ttu-id="3199b-107">Erstellen Sie einen neuen Unterschlüssel unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell**, wobei *ProgID* der Dateityp ist, für den Sie ein Cascading-Menü hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="3199b-107">Create a new subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**, where *ProgID* is the file type for which you want to add a cascading menu.</span></span> <span data-ttu-id="3199b-108">Sie können den neuen Unterschlüssel beliebig benennen.</span><span class="sxs-lookup"><span data-stu-id="3199b-108">You can name this new subkey anything you'd like.</span></span> <span data-ttu-id="3199b-109">Im restlichen Teil dieses Themas nennen wir es *cascademenu*, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3199b-109">For the remainder of this topic, we'll call it *CascadeMenu*, as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a><span data-ttu-id="3199b-110">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="3199b-110">Step 2:</span></span>

<span data-ttu-id="3199b-111">Fügen Sie dem Unterschlüssel *cascademenu* einen Eintrag mit dem Namen "MUIVerb", dem Typ " **reg \_ SZ** " oder " **reg \_ Expand \_ SZ**", hinzu.</span><span class="sxs-lookup"><span data-stu-id="3199b-111">Add an entry named "MUIVerb", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="3199b-112">Weisen Sie diesem Eintrag einen Zeichen folgen Wert zu, z. b. "Menü" Test Cascade "</span><span class="sxs-lookup"><span data-stu-id="3199b-112">Assign this entry a string value such as "Test Cascade Menu".</span></span> <span data-ttu-id="3199b-113">Normalerweise wird diese Zeichenfolge als Ressourcen Verweis in der Form " @file , Resource" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3199b-113">Normally, this string is provided as a resource reference in the form "@file, resource".</span></span> <span data-ttu-id="3199b-114">Der (standardmäßige) Wert für den Unterschlüssel *caskadetten Menu* darf nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3199b-114">The (Default) value for the *CascadeMenu* subkey should not be set.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a><span data-ttu-id="3199b-115">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="3199b-115">Step 3:</span></span>

<span data-ttu-id="3199b-116">Fügen Sie dem Unterschlüssel *caskadetten Menu* einen Eintrag mit dem Namen "Unterbefehle" vom Typ " **reg \_ SZ** " oder " **reg \_ Expand \_ SZ**" hinzu.</span><span class="sxs-lookup"><span data-stu-id="3199b-116">Add an entry named "SubCommands", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="3199b-117">Weisen Sie diesem Eintrag eine durch Semikolons getrennte Liste der Verben zu, die im Menü in der gewünschten Reihenfolge angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3199b-117">Assign this entry a semicolon-delimited list of the verbs that should appear on the menu, in their desired order of appearance.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a><span data-ttu-id="3199b-118">Schritt 4:</span><span class="sxs-lookup"><span data-stu-id="3199b-118">Step 4:</span></span>

<span data-ttu-id="3199b-119">Füllen Sie den **commandstore** -Unterschlüssel mit Verb-Implementierungen für alle benutzerdefinierten statischen Verb-Implementierungs Methoden aus, die Sie im Eintrag für die Unterbefehle verwendet haben. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3199b-119">Populate the **CommandStore** subkey with verb implementations for any custom static verb implementation methods that you've used in your SubCommands entry; for example:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a><span data-ttu-id="3199b-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3199b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3199b-121">Erstellen von statischen kaskadierenden Menüs</span><span class="sxs-lookup"><span data-stu-id="3199b-121">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
</dt> </dl>

 

 



