---
description: ICE97 überprüft, ob zwei Komponenten eine freigegebene Komponente nicht im selben Verzeichnis isolieren.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348684"
---
# <a name="ice97"></a><span data-ttu-id="12c18-103">ICE97</span><span class="sxs-lookup"><span data-stu-id="12c18-103">ICE97</span></span>

<span data-ttu-id="12c18-104">ICE97 überprüft, ob zwei Komponenten eine freigegebene Komponente nicht im selben Verzeichnis isolieren.</span><span class="sxs-lookup"><span data-stu-id="12c18-104">ICE97 verifies that two components do not isolate a shared component to the same directory.</span></span>

## <a name="result"></a><span data-ttu-id="12c18-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="12c18-105">Result</span></span>

<span data-ttu-id="12c18-106">ICE97 gibt die folgenden Warnungen aus.</span><span class="sxs-lookup"><span data-stu-id="12c18-106">ICE97 posts the following warnings.</span></span>



| <span data-ttu-id="12c18-107">ICE97-Warnung</span><span class="sxs-lookup"><span data-stu-id="12c18-107">ICE97 Warning</span></span>                                                                                                                                                                    | <span data-ttu-id="12c18-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12c18-108">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="12c18-109">Mit dieser Komponente \[ 1 \] wird die freigegebene Komponente in demselben Verzeichnis \[ 2 \] wie ein anderes installiert, das Komponenten Regeln unterbricht, wenn mindestens eine Komponente für die Installation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="12c18-109">This component \[1\] installs the Shared component into the same directory \[2\] as another, which breaks component rules if both (or more) components are selected for install.</span></span> | <span data-ttu-id="12c18-110">Zwei Komponenten dürfen eine freigegebene Komponente nicht in dasselbe Verzeichnis isolieren.</span><span class="sxs-lookup"><span data-stu-id="12c18-110">Two components must not isolate a shared component to the same directory.</span></span> |



 

<span data-ttu-id="12c18-111">Beispielsweise werden Component1 und Component2, die componentshared gemeinsam verwenden, im gleichen Verzeichnis installiert.</span><span class="sxs-lookup"><span data-stu-id="12c18-111">For example, Component1 and Component2, which share ComponentShared, are installed to the same directory.</span></span> <span data-ttu-id="12c18-112">Beide geben componentshared als isolierte Komponente an.</span><span class="sxs-lookup"><span data-stu-id="12c18-112">Both specify ComponentShared as an isolated component.</span></span> <span data-ttu-id="12c18-113">Aufgrund der Isolierung werden die Dateien in componentshared zweimal in den Verzeichnis \_ Verweis für Component1 und Component2 kopiert.</span><span class="sxs-lookup"><span data-stu-id="12c18-113">Because of the isolation, the files in ComponentShared are copied twice into the Directory\_ reference for Component1 and Component2.</span></span> <span data-ttu-id="12c18-114">Die Komponenten verfügen jetzt über einen Verweis Zähler für die Kopie der Dateien.</span><span class="sxs-lookup"><span data-stu-id="12c18-114">The components now have one reference count on the copy of files.</span></span> <span data-ttu-id="12c18-115">Dies verstößt gegen die installerkomponentenregeln.</span><span class="sxs-lookup"><span data-stu-id="12c18-115">This is in violation of the Installer component rules.</span></span> <span data-ttu-id="12c18-116">Wenn Component1 deinstalliert wird, werden die Dateien der isolierten Komponenten entfernt, und Component2 ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="12c18-116">If Component1 is uninstalled, the isolated components files are removed and Component2 is broken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12c18-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12c18-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12c18-118">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="12c18-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



