---
description: In diesem Abschnitt wird die Erstellung von Kontextmenüs (Kontextmenüs) und die Implementierung von Kontextmenü-Handlern (Verb) erläutert.
title: Kontextmenüs und Kontextmenü Handler
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214437"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a><span data-ttu-id="36db2-103">Kontextmenüs und Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="36db2-103">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>

<span data-ttu-id="36db2-104">In diesem Abschnitt wird die Erstellung von Kontextmenüs (Kontextmenüs) und die Implementierung von Kontextmenü-Handlern (Verb) erläutert.</span><span class="sxs-lookup"><span data-stu-id="36db2-104">This section discusses the creation of shortcut (context) menus, and the implementation of shortcut menu (verb) handlers.</span></span>

<span data-ttu-id="36db2-105">Dieser Abschnitt zu Dateitypen und Dateizuordnungen ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="36db2-105">This section on file types and file associations is organized as follows:</span></span>

-   [<span data-ttu-id="36db2-106">Verben und Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="36db2-106">Verbs and File Associations</span></span>](fa-verbs.md)
-   [<span data-ttu-id="36db2-107">Auswählen einer statischen oder dynamischen Kontextmenü Methode</span><span class="sxs-lookup"><span data-stu-id="36db2-107">Choosing a Static or Dynamic Shortcut Menu Method</span></span>](shortcut-choose-method.md)
-   [<span data-ttu-id="36db2-108">Bewährte Methoden für Kontextmenü Handler und mehrere Verben</span><span class="sxs-lookup"><span data-stu-id="36db2-108">Best Practices for Shortcut Menu Handlers and Multiple Verbs</span></span>](verbs-best-practices.md)
-   [<span data-ttu-id="36db2-109">Erstellen von Kontextmenü Handlern</span><span class="sxs-lookup"><span data-stu-id="36db2-109">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
-   [<span data-ttu-id="36db2-110">Erstellen von statischen kaskadierenden Menüs</span><span class="sxs-lookup"><span data-stu-id="36db2-110">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
-   [<span data-ttu-id="36db2-111">Unterdrücken der Sichtbarkeit des Verbs</span><span class="sxs-lookup"><span data-stu-id="36db2-111">How to Suppress and Control Verb Visibility</span></span>](how-to-suppress-and-control-visibility.md)
-   [<span data-ttu-id="36db2-112">Verwenden des Verb Auswahl Modells</span><span class="sxs-lookup"><span data-stu-id="36db2-112">How to Employ the Verb Selection Model</span></span>](how-to-employ-the-verb-selection-model.md)
-   [<span data-ttu-id="36db2-113">Verwenden von Element Attributen</span><span class="sxs-lookup"><span data-stu-id="36db2-113">How to Use Item Attributes</span></span>](how-to-use-item-attributes.md)
-   [<span data-ttu-id="36db2-114">So implementieren Sie benutzerdefinierte Verben für Ordner über Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="36db2-114">How to Implement Custom Verbs for Folders through Desktop.ini</span></span>](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [<span data-ttu-id="36db2-115">Anpassen eines Kontextmenüs mithilfe dynamischer Verben</span><span class="sxs-lookup"><span data-stu-id="36db2-115">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
-   [<span data-ttu-id="36db2-116">Implementieren der IContextMenu-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="36db2-116">How to Implement the IContextMenu Interface</span></span>](how-to-implement-the-icontextmenu-interface.md)
-   [<span data-ttu-id="36db2-117">Verweis auf das Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="36db2-117">Shortcut Menu Reference</span></span>](context-menu-reference.md)

## <a name="additional-resources"></a><span data-ttu-id="36db2-118">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="36db2-118">Additional Resources</span></span>

<span data-ttu-id="36db2-119">Verwandte konzeptionelle Hintergrundinformationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="36db2-119">For related conceptual background, see the following topics:</span></span>

-   <span data-ttu-id="36db2-120">[Einführung in Dateizuordnungen](fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="36db2-120">[Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="36db2-121">Informationen zum Erweitern der Shell mit Dateityp Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="36db2-121">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>
-   <span data-ttu-id="36db2-122">Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="36db2-122">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

<span data-ttu-id="36db2-123">Weitere Informationen zur zugehörigen Referenz Dokumentation finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="36db2-123">For related reference documenation, see the following topics:</span></span>

-   <span data-ttu-id="36db2-124">Informationen zum Ausführen eines Verbs für ein shellelement finden Sie unter der [**invokeverb**](folderitem-invokeverb.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="36db2-124">To execute a verb on a Shell item, see the [**InvokeVerb**](folderitem-invokeverb.md) method.</span></span>
-   <span data-ttu-id="36db2-125">Weitere Informationen zum Abrufen einer Auflistung von Verben, die für ein shellelement ausgeführt werden können, finden Sie in der [**Verbs**](folderitem-verbs.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="36db2-125">To retrieve a collection of verbs that can be executed on a Shell item, see the [**Verbs**](folderitem-verbs.md) method.</span></span>
-   <span data-ttu-id="36db2-126">Informationen zum Ausführen eines Vorgangs für eine angegebene Datei finden Sie unter den Funktionen [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="36db2-126">To perform an operation on a specified file, see either the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) functions.</span></span>

 

 



