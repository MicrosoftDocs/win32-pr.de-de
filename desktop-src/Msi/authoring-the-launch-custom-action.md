---
description: Der Quellcode für eine benutzerdefinierte Beispiel Aktion mit dem Namen "Launch", die den Beispiel Spezifikationen entspricht, wird vom Windows Installer SDK als Datei "Tutorial. cpp" bereitgestellt.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Erstellen der benutzerdefinierten Aktion "starten"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959507"
---
# <a name="authoring-the-launch-custom-action"></a><span data-ttu-id="c9aed-103">Erstellen der benutzerdefinierten Aktion "starten"</span><span class="sxs-lookup"><span data-stu-id="c9aed-103">Authoring the Launch Custom Action</span></span>

<span data-ttu-id="c9aed-104">Der Quellcode für eine benutzerdefinierte Beispiel Aktion mit dem Namen "Launch", die den Beispiel Spezifikationen entspricht, wird vom Windows Installer SDK als Datei "Tutorial. cpp" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c9aed-104">The source code for a sample custom action named Launch, which meets the sample specifications, is provided by the Windows Installer SDK as the file Tutorial.cpp.</span></span> <span data-ttu-id="c9aed-105">Durch diese benutzerdefinierte Aktion wird [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) verwendet, um eine Zeichenfolge zu formatieren, die Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c9aed-105">This custom action makes use of [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) to format a string containing properties.</span></span> <span data-ttu-id="c9aed-106">Die Eigenschaft \[ \# filekey wird \] in den vollständigen Pfad der HTML-Datei aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c9aed-106">The property \[\#FileKey\] resolves to the full path of the HTML file.</span></span> <span data-ttu-id="c9aed-107">Erstellen Sie die Datei Tutorial.dll mithilfe der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="c9aed-107">Use the source file to create the file Tutorial.dll.</span></span> <span data-ttu-id="c9aed-108">Der Einstiegspunkt für diese dll ist "launchtutorial".</span><span class="sxs-lookup"><span data-stu-id="c9aed-108">The entry point to this DLL is LaunchTutorial.</span></span>

<span data-ttu-id="c9aed-109">Das Beispiel zum Starten einer benutzerdefinierten Aktion ruft eine in C++ geschriebene dll auf und wird aus einem temporären binären Stream generiert.</span><span class="sxs-lookup"><span data-stu-id="c9aed-109">The sample custom action Launch calls a DLL written in C++ and is generated from a temporary binary stream.</span></span> <span data-ttu-id="c9aed-110">Benutzerdefinierte Aktionen dieses Typs umfassen die Basistyps msidbcustomaktiontypedll und msidbcustomaktiontypebinarydata, die einen numerischen Basis-Typ gleich 1 angeben.</span><span class="sxs-lookup"><span data-stu-id="c9aed-110">Custom actions of this type include the base type constants msidbCustomActionTypeDll and msidbCustomActionTypeBinaryData, which give a base numeric type equal to 1.</span></span> <span data-ttu-id="c9aed-111">Siehe [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="c9aed-111">See [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="c9aed-112">Da die Spezifikationen erfordern, dass die Installation fortgesetzt wird, wenn die benutzerdefinierte Aktion fehlschlägt, schließt Launch auch die optionale Konstante **msidbcustomaction typecontinue** ein, die 64 ist.</span><span class="sxs-lookup"><span data-stu-id="c9aed-112">Because the specifications require that the installation continue if the custom action fails, Launch also includes the optional constant **msidbCustomActionTypeContinue**, which is 64.</span></span> <span data-ttu-id="c9aed-113">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c9aed-113">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span> <span data-ttu-id="c9aed-114">Der gesamte numerische Starttyp ist 65.</span><span class="sxs-lookup"><span data-stu-id="c9aed-114">The total numeric type of Launch is 65.</span></span>

<span data-ttu-id="c9aed-115">Fahren Sie mit [dem Hinzufügen von Start zu den Tabellen CustomAction und Binary](adding-launch-to-the-customaction-and-binary-tables.md)fort.</span><span class="sxs-lookup"><span data-stu-id="c9aed-115">Continue to [Adding Launch to the CustomAction and Binary Tables](adding-launch-to-the-customaction-and-binary-tables.md).</span></span>

 

 



