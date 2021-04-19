---
description: Es gibt mehrere Funktionen, die die Installation von Produktkomponenten und Features ändern. Im folgenden wird beschrieben, wie Features und Komponenten geändert werden.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Arbeiten mit Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363539"
---
# <a name="working-with-features-and-components"></a><span data-ttu-id="131ef-104">Arbeiten mit Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="131ef-104">Working with Features and Components</span></span>

<span data-ttu-id="131ef-105">Es gibt mehrere Funktionen, die die Installation von Produkt [Komponenten und Features](components-and-features.md)ändern.</span><span class="sxs-lookup"><span data-stu-id="131ef-105">There are several functions that change the installation of product [components and features](components-and-features.md).</span></span> <span data-ttu-id="131ef-106">Im folgenden wird beschrieben, wie Features und Komponenten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="131ef-106">The following describes how to change features and components.</span></span>

<span data-ttu-id="131ef-107">**So ändern Sie die Installation von Features und Komponenten**</span><span class="sxs-lookup"><span data-stu-id="131ef-107">**To change the installation of features and components**</span></span>

1.  <span data-ttu-id="131ef-108">Legen Sie die Installations Ebene für eine Komponente oder ein Feature fest, indem Sie die [**msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="131ef-108">Set the installation level for a component or feature by calling the [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) function.</span></span>

    <span data-ttu-id="131ef-109">Jeder Funktion in einem Paket wird eine Installations Ebene in der [Featuretabelle](feature-table.md)zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="131ef-109">Each feature in a package is assigned an installation level in the [Feature table](feature-table.md).</span></span> <span data-ttu-id="131ef-110">Wenn die Installations Ebene eines Features niedriger ist als die von [**msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)festgelegte Ebene, wird das Feature für die Installation ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="131ef-110">If the installation level of a feature is lower than the level set by [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), the feature is selected for installation.</span></span> <span data-ttu-id="131ef-111">Nachdem **msisetinstalllevel** aufgerufen wurde, können Sie explizit ändern, ob eine Funktion installiert ist.</span><span class="sxs-lookup"><span data-stu-id="131ef-111">After **MsiSetInstallLevel** is called, you can explicitly change whether a feature is installed.</span></span>

2.  <span data-ttu-id="131ef-112">Bestimmen Sie, welche Zustände für eine bestimmte Funktion verfügbar sind, indem Sie die [**msigetfeaturevalidstates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="131ef-112">Determine which states are available for a specified feature by calling the [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) function.</span></span>
3.  <span data-ttu-id="131ef-113">Abrufen der Speicherplatzanforderungen für eine angegebene Funktion und deren untergeordneter Funktionen durch Aufrufen der Funktion " [**msigetfeaturecost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) ".</span><span class="sxs-lookup"><span data-stu-id="131ef-113">Obtain the disk space requirements for a specified feature and its child features by calling the [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) function.</span></span>
4.  <span data-ttu-id="131ef-114">Rufen Sie den aktuellen Status eines Features oder einer Komponente ab, indem Sie die [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) -Funktion oder die [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="131ef-114">Obtain the current state of a feature or component by calling the [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) function or the [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) function.</span></span>
5.  <span data-ttu-id="131ef-115">Ändern Sie den Status des Features oder der Komponente mit der [**msisetfeaturestate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) -Funktion oder der [**msisetcomponentstate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="131ef-115">Change the state of the feature or component with the [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) function or the [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) function.</span></span>

 

 



