---
description: Der Wert der Zusammenfassungs Eigenschaft "Revisionsnummer" im Zusammenfassungs Informationsdaten Strom muss bei der Lokalisierung einer Datenbank in einen neuen, eindeutigen Wert geändert werden, da die Installations Datenbank geändert wird. Siehe Paket Codes.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Aktualisieren eines Zusammenfassungs Informationsdaten Stroms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393773"
---
# <a name="updating-a-summary-information-stream"></a><span data-ttu-id="6a448-104">Aktualisieren eines Zusammenfassungs Informationsdaten Stroms</span><span class="sxs-lookup"><span data-stu-id="6a448-104">Updating a Summary Information Stream</span></span>

<span data-ttu-id="6a448-105">Der Wert der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " im [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) muss bei der Lokalisierung einer Datenbank in einen neuen, eindeutigen Wert geändert werden, da die Installations Datenbank geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6a448-105">The value of the [**Revision Number Summary**](revision-number-summary.md) Property in the [summary information stream](summary-information-stream.md) must be changed to a new, unique value when localizing a database, because the installation database is being changed.</span></span> <span data-ttu-id="6a448-106">Siehe [Paket Codes](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6a448-106">See [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="6a448-107">Der Wert der [**Template Summary**](template-summary.md) -Eigenschaft im Zusammenfassungs Informationsdaten Strom muss in den numerischen sprach Bezeichner (langid) der neuen Sprache geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6a448-107">The value of the [**Template Summary**](template-summary.md) Property in the summary information stream must be changed to the numeric language identifier (LANGID) of the new language.</span></span>

<span data-ttu-id="6a448-108">Wenn die beschreibenden Text Zeichenfolgen im Zusammenfassungs Informationsdaten Strom in die neue Sprache lokalisiert werden, muss die [**Codepage-Zusammenfassungs**](codepage-summary.md) Eigenschaft auf die richtige Codepage für die neue Sprache festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6a448-108">If the descriptive text strings in the summary information stream are localized to the new language, the [**Codepage Summary**](codepage-summary.md) Property must be set to the correct code page for the new language.</span></span>

<span data-ttu-id="6a448-109">Sie können den Zusammenfassungs Datenstrom des lokalisierten Pakets mit dem gleichen Verfahren wie beim [Hinzufügen von Zusammenfassungs Informationen](adding-summary-information.md)ändern.</span><span class="sxs-lookup"><span data-stu-id="6a448-109">You may modify the summary information stream of the localized package by the same procedure as in [Adding Summary Information](adding-summary-information.md).</span></span> <span data-ttu-id="6a448-110">Ein Beispiel für die Verwendung der Methoden zur Daten Bank Zusammenfassung finden Sie auch im Windows Installer SDK als Dienst WiSumInf.vbs.</span><span class="sxs-lookup"><span data-stu-id="6a448-110">An example demonstrating the use of the database summary information methods is also provided in the Windows Installer SDK as the utility WiSumInf.vbs.</span></span> <span data-ttu-id="6a448-111">Weitere Informationen zu WiSumInf.vbs finden Sie unter [Verwalten von Zusammenfassungs Informationen](manage-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="6a448-111">For more information about WiSumInf.vbs, see [Manage Summary Information](manage-summary-information.md).</span></span>

[<span data-ttu-id="6a448-112">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="6a448-112">Continue</span></span>](adding-localized-resources.md)

 

 



