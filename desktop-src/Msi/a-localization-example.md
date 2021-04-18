---
description: In diesem Beispiel wird veranschaulicht, wie Sie das Windows Installer Paket lokalisieren, das in einem Installations Beispiel beschrieben wird. Das ursprüngliche Installationspaket wird von der englischen Sprachversion in Französisch geändert.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Beispiel für eine Lokalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347965"
---
# <a name="a-localization-example"></a><span data-ttu-id="06973-104">Beispiel für eine Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="06973-104">A Localization Example</span></span>

<span data-ttu-id="06973-105">In diesem Beispiel wird veranschaulicht, wie Sie das Windows Installer Paket lokalisieren, das in [einem Installations Beispiel](an-installation-example.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="06973-105">This example illustrates how to localize the Windows Installer package described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="06973-106">Das ursprüngliche Installationspaket wird von der englischen Sprachversion in Französisch geändert.</span><span class="sxs-lookup"><span data-stu-id="06973-106">The original installation package is changed from an English into French language version.</span></span>

<span data-ttu-id="06973-107">Das Lokalisierungs Beispiel verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="06973-107">The localization sample has the following specifications:</span></span>

-   <span data-ttu-id="06973-108">Die Benutzeroberfläche für die Installation der Anwendung MNP2000 sollte von Englisch in Französisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="06973-108">The installation UI for the application MNP2000 should be changed from English to French.</span></span>
-   <span data-ttu-id="06973-109">Die französische Version von MNP2000 enthält Readme.txt-und Help.txt Dateien, die in französischer Sprache geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="06973-109">The French version of MNP2000 includes Readme.txt and Help.txt files written in the French language.</span></span>
-   <span data-ttu-id="06973-110">Die französische Version enthält eine Liste der Reise-Agents in Frankreich, die Tickets in der Red Park-Arena bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="06973-110">The French version includes a list of travel agents in France that can provide tickets to Red Park Arena.</span></span> <span data-ttu-id="06973-111">Diese Liste (bereitgestellt als neue Datei, Fre.txt) ist kein Teil der englischen Version.</span><span class="sxs-lookup"><span data-stu-id="06973-111">This list (provided as a new file, Fre.txt) is not a part of the English version.</span></span>

<span data-ttu-id="06973-112">Das allgemeine Verfahren zum Lokalisieren einer Installation wird im Abschnitt [lokalisieren eines Windows Installer Pakets](localizing-a-windows-installer-package.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="06973-112">The general procedure for localizing an installation is described in the section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="06973-113">Kopieren Sie die englische Version von MNP2000.msi und alle in [Planen der Installation](planning-the-installation.md) beschriebenen Quelldateien in einen neuen Ordner.</span><span class="sxs-lookup"><span data-stu-id="06973-113">Copy the English version of MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md) into a new folder.</span></span> <span data-ttu-id="06973-114">Ändern Sie den Namen der MNP2000.msi im Ordner in MNPFren.msi.</span><span class="sxs-lookup"><span data-stu-id="06973-114">Change the name of the MNP2000.msi in the folder to MNPFren.msi.</span></span> <span data-ttu-id="06973-115">In den folgenden Abschnitten ändern Sie diese Kopie, um die Anwendung in Französisch zu lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="06973-115">In the following sections you will modify this copy to localize the application into French.</span></span>

[<span data-ttu-id="06973-116">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="06973-116">Continue</span></span>](checking-the-installation-database-code-page.md)

 

 



