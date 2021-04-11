---
description: Der Windows Installer bietet viele integrierte Aktionen für die Ausführung des Installationsvorgangs. Eine Liste dieser Aktionen finden Sie in der Referenz zu Standard Aktionen.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042396"
---
# <a name="custom-actions"></a><span data-ttu-id="ebe4b-104">Benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="ebe4b-104">Custom Actions</span></span>

<span data-ttu-id="ebe4b-105">Der Windows Installer bietet viele integrierte Aktionen für die Ausführung des Installationsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-105">The Windows Installer provides many built-in actions for performing the installation process.</span></span> <span data-ttu-id="ebe4b-106">Eine Liste dieser Aktionen finden Sie in der [Referenz zu Standard Aktionen](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ebe4b-106">For a list of these actions, see the [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="ebe4b-107">Standard Aktionen sind ausreichend, um in den meisten Fällen eine Installation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-107">Standard actions are sufficient to execute an installation in most cases.</span></span> <span data-ttu-id="ebe4b-108">Es gibt jedoch Situationen, in denen der Entwickler eines Installationspakets es zum Schreiben einer benutzerdefinierten Aktion findet.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-108">However, there are situations where the developer of an installation package finds it necessary to write a custom action.</span></span> <span data-ttu-id="ebe4b-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ebe4b-109">For example:</span></span>

-   <span data-ttu-id="ebe4b-110">Sie möchten eine ausführbare Datei während der Installation starten, die auf dem Computer des Benutzers installiert ist oder mit der Anwendung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-110">You want to launch an executable during installation that is installed on the user's machine or that is being installed with the application.</span></span>
-   <span data-ttu-id="ebe4b-111">Sie möchten spezielle Funktionen während einer Installation, die in einer Dynamic Link Library (dll) definiert sind, aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-111">You want to call special functions during an installation that are defined in a dynamic-link library (DLL).</span></span>
-   <span data-ttu-id="ebe4b-112">Sie möchten Funktionen verwenden, die in den Entwicklungs Sprachen Microsoft Visual Basic Scripting Edition oder literalskript Text von Microsoft JScript während einer Installation geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-112">You want to use functions written in the development languages Microsoft Visual Basic Scripting Edition or Microsoft JScript literal script text during an installation.</span></span>
-   <span data-ttu-id="ebe4b-113">Sie möchten die Ausführung einiger Aktionen bis zu dem Zeitpunkt verzögern, zu dem das Installationsskript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-113">You want to defer the execution of some actions until the time when the installation script is being executed.</span></span>
-   <span data-ttu-id="ebe4b-114">Sie möchten einem ProgressBar-Steuerelement und einem timeremainung-Text Steuerelement Zeit-und Fortschrittsinformationen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-114">You want to add time and progress information to a ProgressBar control and a TimeRemaining Text control.</span></span>

<span data-ttu-id="ebe4b-115">In den folgenden Abschnitten werden benutzerdefinierte Aktionen beschrieben und erläutert, wie Sie in ein Installationspaket integriert werden:</span><span class="sxs-lookup"><span data-stu-id="ebe4b-115">The following sections describe custom actions and how to incorporate them into an installation package:</span></span>

-   [<span data-ttu-id="ebe4b-116">Informationen zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="ebe4b-116">About Custom Actions</span></span>](about-custom-actions.md)
-   [<span data-ttu-id="ebe4b-117">Verwenden von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="ebe4b-117">Using Custom Actions</span></span>](using-custom-actions.md)
-   [<span data-ttu-id="ebe4b-118">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="ebe4b-118">Custom Action Reference</span></span>](custom-action-reference.md)
-   [<span data-ttu-id="ebe4b-119">Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen</span><span class="sxs-lookup"><span data-stu-id="ebe4b-119">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)

 

 



