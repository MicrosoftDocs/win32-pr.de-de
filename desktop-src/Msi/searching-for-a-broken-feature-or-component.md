---
description: Das Installationsprogramm kann die Resilienz von Anwendungen erhöhen, indem beschädigte Komponenten automatisch neu installiert werden.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Suchen nach einer unterbrochenen Funktion oder Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216561"
---
# <a name="searching-for-a-broken-feature-or-component"></a><span data-ttu-id="e33f4-103">Suchen nach einer unterbrochenen Funktion oder Komponente</span><span class="sxs-lookup"><span data-stu-id="e33f4-103">Searching for a Broken Feature or Component</span></span>

<span data-ttu-id="e33f4-104">Das Installationsprogramm kann die [Resilienz](resiliency.md) von Anwendungen erhöhen, indem beschädigte Komponenten automatisch neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="e33f4-104">The installer can increase application [resiliency](resiliency.md) by automatically reinstalling damaged components.</span></span> <span data-ttu-id="e33f4-105">Insbesondere das Installationsprogramm installiert eine Komponente oder ein Feature neu, wenn es feststellt, dass die in der Spalte KEYPATH der [Komponenten Tabelle](component-table.md) angegebene Datei oder der Registrierungsschlüssel fehlt.</span><span class="sxs-lookup"><span data-stu-id="e33f4-105">Specifically, the installer reinstalls a component or feature if it finds that the file or registry key specified in the KeyPath column of the [Component table](component-table.md) is missing.</span></span>

<span data-ttu-id="e33f4-106">Wenn der KEYPATH der Komponente einer Funktion in der Quelle beschädigt ist, oder wenn bei der Erstellung des KEYPATH in der Datenbank ein Fehler auftritt, versucht das Installationsprogramm möglicherweise, ein Installationspaket zu öffnen und die Funktion bei jedem Aktivieren der Verknüpfung der Funktion erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="e33f4-106">If the KeyPath of a feature's component is damaged in the source, or if there is an error in how the KeyPath is authored in the database, the installer may attempt to open an installation package and reinstall the feature each time the feature's shortcut is activated.</span></span>

<span data-ttu-id="e33f4-107">Überprüfen Sie das Ereignisprotokoll auf zwei Einträge wie die folgende, um die Ursache für wiederholte Versuche zur erneuten Installation eines Features oder einer Anwendung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e33f4-107">To determine the cause of repeated attempts to reinstall a feature or application, check the Event Log for two entries such as the following.</span></span>

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

<span data-ttu-id="e33f4-108">Die erste Meldung gibt an, welche Komponente im Paket des Produkts installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e33f4-108">The first message states which component in the product's package was being installed.</span></span> <span data-ttu-id="e33f4-109">Dies ist die Komponente, auf die in der Spalte Komponente der Verknüpfungs \_ [Tabelle](shortcut-table.md)verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e33f4-109">This is the component referenced in the Component\_ column of the [Shortcut table](shortcut-table.md).</span></span>

<span data-ttu-id="e33f4-110">Die zweite Meldung gibt an, bei welcher Komponente eine Fehlererkennung auftritt.</span><span class="sxs-lookup"><span data-stu-id="e33f4-110">The second message states which component is failing detection.</span></span> <span data-ttu-id="e33f4-111">Dies ist die Komponente mit dem fehlenden oder beschädigten KEYPATH, der die Neuinstallation auslöst.</span><span class="sxs-lookup"><span data-stu-id="e33f4-111">This is the component with the missing or damaged KeyPath that's triggering the reinstall.</span></span>

 

 



