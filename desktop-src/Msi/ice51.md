---
description: ICE51 prüft, ob ein Titel für Schriftart Ressourcen Dateien bereitgestellt wurde.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217353"
---
# <a name="ice51"></a><span data-ttu-id="3e5a2-103">ICE51</span><span class="sxs-lookup"><span data-stu-id="3e5a2-103">ICE51</span></span>

<span data-ttu-id="3e5a2-104">ICE51 prüft, ob ein Titel für Schriftart Ressourcen Dateien bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-104">ICE51 checks that a title has been provided for font resource files.</span></span>

<span data-ttu-id="3e5a2-105">Sie müssen einen Titel für eine Schriftart Ressource angeben, die keinen eingebetteten Namen besitzt.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-105">You must provide a title for a font resource that does not have an embedded name.</span></span> <span data-ttu-id="3e5a2-106">Nur die Font-Ressourcen Dateien. TTC,. ttf und OTF erfordern keinen Titel, da diese Dateien einen eingebetteten Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-106">Only .ttc, .ttf, and .otf font resource files do not require a title, because these files contain an embedded name.</span></span> <span data-ttu-id="3e5a2-107">Geben Sie keinen Titel für eine Schriftart Ressource an, die einen eingebetteten Namen enthält, da das System die Schriftart dann zweimal registriert.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-107">Do not provide a title for a font resource that contains an embedded name because the system then registers the font twice.</span></span>

<span data-ttu-id="3e5a2-108">**[Windows Installer 4,5 und früher](not-supported-in-windows-installer-4-5.md):** ICE51 überprüft keine. OTF-Schriftart Ressourcen Dateien.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-108">**[Windows Installer 4.5 and earlier](not-supported-in-windows-installer-4-5.md):** ICE51 does not check .otf font resource files.</span></span>

## <a name="result"></a><span data-ttu-id="3e5a2-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="3e5a2-109">Result</span></span>

<span data-ttu-id="3e5a2-110">ICE51 gibt einen Fehler aus, wenn die Schriftarten Ressourcen Dateien ". TTC", ". ttf" und "otf" mit Titeln vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-110">ICE51 posts an error if there are any .ttc, .ttf, and .otf font resource files with titles.</span></span> <span data-ttu-id="3e5a2-111">ICE51 gibt eine Warnung aus, wenn andere Schriftart Ressourcen Dateien ohne Titel vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-111">ICE51 posts a warning if there are any other font resource files without a title.</span></span>

## <a name="example"></a><span data-ttu-id="3e5a2-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3e5a2-112">Example</span></span>

<span data-ttu-id="3e5a2-113">ICE51 würde die folgende Warnung für das gezeigte Beispiel melden.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-113">ICE51 would report the following warning for the example shown.</span></span>

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

<span data-ttu-id="3e5a2-114">ICE51 würde die folgende Fehlermeldung für das gezeigte Beispiel melden.</span><span class="sxs-lookup"><span data-stu-id="3e5a2-114">ICE51 would report the following error message for the example shown.</span></span>

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

<span data-ttu-id="3e5a2-115">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="3e5a2-115">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="3e5a2-116">File</span><span class="sxs-lookup"><span data-stu-id="3e5a2-116">File</span></span>  | <span data-ttu-id="3e5a2-117">FileName</span><span class="sxs-lookup"><span data-stu-id="3e5a2-117">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="3e5a2-118">Font1</span><span class="sxs-lookup"><span data-stu-id="3e5a2-118">Font1</span></span> | <span data-ttu-id="3e5a2-119">font1. ttf</span><span class="sxs-lookup"><span data-stu-id="3e5a2-119">font1.ttf</span></span> |
| <span data-ttu-id="3e5a2-120">Font2</span><span class="sxs-lookup"><span data-stu-id="3e5a2-120">Font2</span></span> | <span data-ttu-id="3e5a2-121">font2. FON</span><span class="sxs-lookup"><span data-stu-id="3e5a2-121">font2.fon</span></span> |



 

[<span data-ttu-id="3e5a2-122">Schriftart Tabelle</span><span class="sxs-lookup"><span data-stu-id="3e5a2-122">Font Table</span></span>](font-table.md)



| <span data-ttu-id="3e5a2-123">Datei\_</span><span class="sxs-lookup"><span data-stu-id="3e5a2-123">File\_</span></span> | <span data-ttu-id="3e5a2-124">FontTitle</span><span class="sxs-lookup"><span data-stu-id="3e5a2-124">FontTitle</span></span>          |
|--------|--------------------|
| <span data-ttu-id="3e5a2-125">Font1</span><span class="sxs-lookup"><span data-stu-id="3e5a2-125">Font1</span></span>  | <span data-ttu-id="3e5a2-126">Eine wirklich coole Schriftart</span><span class="sxs-lookup"><span data-stu-id="3e5a2-126">A Really Cool Font</span></span> |
| <span data-ttu-id="3e5a2-127">Font2</span><span class="sxs-lookup"><span data-stu-id="3e5a2-127">Font2</span></span>  |                    |



 

## <a name="related-topics"></a><span data-ttu-id="3e5a2-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e5a2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e5a2-129">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="3e5a2-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



