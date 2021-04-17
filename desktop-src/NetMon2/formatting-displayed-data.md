---
description: Netzwerkmonitor oder Ihre Parser-DLL kann die Daten formatieren, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Formatieren von angezeigten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525145"
---
# <a name="formatting-displayed-data"></a><span data-ttu-id="960d5-103">Formatieren von angezeigten Daten</span><span class="sxs-lookup"><span data-stu-id="960d5-103">Formatting Displayed Data</span></span>

<span data-ttu-id="960d5-104">Netzwerkmonitor oder Ihre Parser-DLL kann die Daten formatieren, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="960d5-104">Network Monitor or your parser DLL can format the data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="960d5-105">Netzwerkmonitor stellt einen generischen Formatierer bereit, der die grundlegenden Dienste bereitstellt, die zum Anzeigen der meisten Datentypen in einem Protokoll erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="960d5-105">Network Monitor provides a generic formatter that provides the basic services needed to display most data types that exist within a protocol.</span></span> <span data-ttu-id="960d5-106">Der generische Formatierer unterstützt jedoch nicht alle Datentypen.</span><span class="sxs-lookup"><span data-stu-id="960d5-106">However, the generic formatter does not support all data types.</span></span> <span data-ttu-id="960d5-107">Beispielsweise unterstützt das generische Formatierer Folgendes nicht:</span><span class="sxs-lookup"><span data-stu-id="960d5-107">For example, the generic formatter does not support the following:</span></span>

-   <span data-ttu-id="960d5-108">Mehrere Adresstypen.</span><span class="sxs-lookup"><span data-stu-id="960d5-108">Several address types.</span></span>
-   <span data-ttu-id="960d5-109">Quell-und Zielanzeige Name.</span><span class="sxs-lookup"><span data-stu-id="960d5-109">Source and destination-friendly names.</span></span>
-   <span data-ttu-id="960d5-110">Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="960d5-110">Object identifiers.</span></span>
-   <span data-ttu-id="960d5-111">Große ganzzahlige Datentypen.</span><span class="sxs-lookup"><span data-stu-id="960d5-111">Large integer data types.</span></span>
-   <span data-ttu-id="960d5-112">Datentypen mit geringer Ganzzahl mit variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="960d5-112">Variable length small integer data types.</span></span>

<span data-ttu-id="960d5-113">Im folgenden Beispiel werden zwei formatierte Zeichen folgen für die Eigenschaft Berechtigungs-ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="960d5-113">The following example identifies two formatted strings for the Privilege ID property.</span></span>

-   <span data-ttu-id="960d5-114">Die erste Codezeile zeigt die Ausgabe des generischen Formatierers.</span><span class="sxs-lookup"><span data-stu-id="960d5-114">The first line of code shows the output of the generic formatter.</span></span> <span data-ttu-id="960d5-115">Die Ausgabe basiert auf dem Datentyp.</span><span class="sxs-lookup"><span data-stu-id="960d5-115">The output is based on the data type.</span></span>
-   <span data-ttu-id="960d5-116">Die zweite Codezeile zeigt die Ausgabe eines benutzerdefinierten Formatierers mit einer Zeichenfolge für die Eigenschafts Daten.</span><span class="sxs-lookup"><span data-stu-id="960d5-116">The second line of code shows the output of a custom formatter with a string to the property data.</span></span>

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> <span data-ttu-id="960d5-117">Verwenden Sie nach Möglichkeit den generischen Formatierer, um Ihre Daten anzuzeigen, da Sie die Größe Ihrer Parser-DLL steuern können und bessere plattformübergreifende Funktionen für Ihre Parser-DLL bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="960d5-117">When possible, use the generic formatter to display your data because it allows you to control the size of your parser DLL, and provides better cross-platform capabilities for your parser DLL.</span></span>

 

 

 



