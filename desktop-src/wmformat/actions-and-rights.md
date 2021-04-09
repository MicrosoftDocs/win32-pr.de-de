---
title: Aktionen und Rechte
description: Aktionen und Rechte
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Digital Rights Management (DRM), Aktionen
- DRM (Digital Rights Management), Aktionen
- Digital Rights Management (DRM), Rechte
- DRM (Digital Rights Management), Rechte
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Lizenzen, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036430"
---
# <a name="actions-and-rights"></a><span data-ttu-id="b0226-113">Aktionen und Rechte</span><span class="sxs-lookup"><span data-stu-id="b0226-113">Actions and Rights</span></span>

<span data-ttu-id="b0226-114">Wenn eine Datei mithilfe von Windows Media DRM geschützt wird, ist ihre Verwendung vollständig eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="b0226-114">When a file is protected by using Windows Media DRM, its use is completely restricted.</span></span> <span data-ttu-id="b0226-115">Lizenzen können ausgestellt werden, um es einem Benutzer zu ermöglichen, den Inhalt auf bestimmte Weise zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0226-115">Licenses can be issued to enable a user to use the content in specific ways.</span></span> <span data-ttu-id="b0226-116">Jede Art, in der ein Benutzer den Inhalt verwenden kann, wird durch eine Aktion beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0226-116">Each way in which a user might use the content is described by an action.</span></span> <span data-ttu-id="b0226-117">Die Wiedergabe einer Datei auf einem Computer ist beispielsweise eine Aktion.</span><span class="sxs-lookup"><span data-stu-id="b0226-117">For example, playing a file on a computer is an action.</span></span>

<span data-ttu-id="b0226-118">Eine Lizenz, die eine bestimmte Aktion ermöglicht, wird als Recht zum Erteilen einer Berechtigung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b0226-118">A license that enables a given action is said to grant a right.</span></span> <span data-ttu-id="b0226-119">Beispielsweise kann eine Lizenz das Recht zum Abspielen von Inhalten auf einem Computer erteilen.</span><span class="sxs-lookup"><span data-stu-id="b0226-119">For example, a license can grant the right to play content on a computer.</span></span>

<span data-ttu-id="b0226-120">Aktionen und Rechte verweisen auf die gleichen Methoden wie zum Verwenden von Inhalt.</span><span class="sxs-lookup"><span data-stu-id="b0226-120">Actions and rights refer to the same ways of using content.</span></span> <span data-ttu-id="b0226-121">Der Unterschied besteht darin, dass sich die-Aktion auf die Verwendung bezieht, während sich die Rechte auf die Berechtigung bezieht.</span><span class="sxs-lookup"><span data-stu-id="b0226-121">The difference is that the action refers to the use while the right refers to the permission.</span></span> <span data-ttu-id="b0226-122">Trotz dieser Unterscheidung werden die Wörter Action und Right häufig austauschbar in dieser Dokumentation und in anderen Dokumenten verwendet, in denen Windows Media DRM beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b0226-122">Despite this distinction, the words action and right are often used interchangeably in this documentation and in other documents that describe Windows Media DRM.</span></span>

<span data-ttu-id="b0226-123">Die Aktionen, die von Windows Media DRM-rechten gesteuert werden, sind im Abschnitt [Rechte Konstanten](rights-constants.md) dieser Dokumentation aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0226-123">The actions governed by Windows Media DRM rights are listed in the [Rights Constants](rights-constants.md) section of this documentation.</span></span>

<span data-ttu-id="b0226-124">Bestimmte Methoden der erweiterten APIs des Windows Media DRM-Clients verwenden verschiedene Konstanten, um auf die grundlegenden DRM-Rechte zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="b0226-124">Certain methods of the Windows Media DRM Client Extended APIs use different constants to refer to the basic DRM rights.</span></span> <span data-ttu-id="b0226-125">Beispielsweise verwendet die [**iwmdrmlicensequery:: querylicensestate**](iwmdrmlicensequery-querylicensestate.md) -Methode eine Reihe von Zeichen folgen, die für die Lizenz Zustände spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="b0226-125">For example, the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method uses a set of strings specific to license states.</span></span> <span data-ttu-id="b0226-126">Obwohl diese Konstanten andere Zeichen folgen als die grundlegenden Rechte Konstanten definieren, verweisen Sie auf die gleichen Rechte in der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="b0226-126">Even though these constants are defining different strings than the basic rights constants, they refer to the same rights in the license.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0226-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0226-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0226-128">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="b0226-128">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




