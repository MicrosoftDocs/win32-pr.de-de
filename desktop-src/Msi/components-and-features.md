---
description: Der Windows Installer organisiert eine Installation der Konzepte von Komponenten und Features.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Komponenten und Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130293"
---
# <a name="components-and-features"></a><span data-ttu-id="9de2b-103">Komponenten und Features</span><span class="sxs-lookup"><span data-stu-id="9de2b-103">Components and Features</span></span>

<span data-ttu-id="9de2b-104">Der Windows Installer organisiert eine Installation der Konzepte von Komponenten und Features.</span><span class="sxs-lookup"><span data-stu-id="9de2b-104">The Windows Installer organizes an installation around the concepts of components and features.</span></span>

<span data-ttu-id="9de2b-105">Ein Feature ist ein Teil der Gesamtfunktionalität der Anwendung, die ein Benutzer unabhängig voneinander installieren kann.</span><span class="sxs-lookup"><span data-stu-id="9de2b-105">A feature is a part of the application's total functionality that a user may decide to install independently.</span></span> <span data-ttu-id="9de2b-106">Weitere Informationen finden Sie unter [Windows Installer Features](windows-installer-features.md).</span><span class="sxs-lookup"><span data-stu-id="9de2b-106">For more information, see [Windows Installer Features](windows-installer-features.md).</span></span>

<span data-ttu-id="9de2b-107">Eine Komponente ist ein Teil der zu installierenden Anwendung oder des Produkts.</span><span class="sxs-lookup"><span data-stu-id="9de2b-107">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="9de2b-108">Das Installationsprogramm installiert oder entfernt eine Komponente immer als ein zusammenhängendes Element vom Computer eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9de2b-108">The installer always installs or removes a component from a user's computer as a coherent piece.</span></span> <span data-ttu-id="9de2b-109">Komponenten werden in der Regel für den Benutzer ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="9de2b-109">Components are usually hidden from the user.</span></span> <span data-ttu-id="9de2b-110">Wenn ein Benutzer eine Funktion für die Installation auswählt, legt das Installationsprogramm fest, welche Komponenten installiert werden müssen, um dieses Feature bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9de2b-110">When a user selects a feature for installation, the installer determines which components must be installed to provide that feature.</span></span> <span data-ttu-id="9de2b-111">Weitere Informationen finden Sie unter [Windows Installer-Komponenten](windows-installer-components.md).</span><span class="sxs-lookup"><span data-stu-id="9de2b-111">For more information, see [Windows Installer Components](windows-installer-components.md).</span></span>

<span data-ttu-id="9de2b-112">Autoren von Installationspaketen müssen entscheiden, wie die Anwendung in Funktionen und Komponenten aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9de2b-112">Authors of installation packages need to decide how to divide their application into features and components.</span></span> <span data-ttu-id="9de2b-113">Die Auswahl der Features hängt hauptsächlich von der Funktionalität der Anwendung aus der Perspektive des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="9de2b-113">The selection of features is primarily determined by the application's functionality from the user's perspective.</span></span> <span data-ttu-id="9de2b-114">Da Komponenten in der Regel über mehrere Anwendungen oder sogar über Produkte hinweg gemeinsam genutzt werden müssen, empfiehlt es sich, dass die Autoren eine Standardmethode für die Auswahl von Komponenten befolgen.</span><span class="sxs-lookup"><span data-stu-id="9de2b-114">Because components commonly must be shared across applications, or even across products, it is recommended that authors follow a standard method for selecting components.</span></span> <span data-ttu-id="9de2b-115">Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="9de2b-115">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

 

 



