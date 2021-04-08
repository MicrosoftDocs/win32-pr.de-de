---
description: Wenn diese System Richtlinie pro Benutzer auf &\# 0034; 1&0034; festgelegt ist \# , können Benutzer und Administratoren, die eine Wartungs Installation eines Produkts ausführen, das Dialog Feld "Durchsuchen" nicht zum Durchsuchen von Medienquellen (z. b. CD-ROM) für die Quellen anderer installier barer Produkte verwenden.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: Disablemedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961092"
---
# <a name="disablemedia"></a><span data-ttu-id="a9c35-103">Disablemedia</span><span class="sxs-lookup"><span data-stu-id="a9c35-103">DisableMedia</span></span>

<span data-ttu-id="a9c35-104">Wenn diese [System Richtlinie](system-policy.md) pro Benutzer auf "1" festgelegt ist, können Benutzer und Administratoren, die eine Wartungs Installation eines Produkts ausführen, das Dialog Feld "Durchsuchen" nicht zum Durchsuchen von Medienquellen (z. b. CD-ROM) für die Quellen anderer installier barer Produkte verwenden.</span><span class="sxs-lookup"><span data-stu-id="a9c35-104">If this per-user [system policy](system-policy.md) is set to "1", users and administrators running a maintenance installation of one product are prevented from using the Browse Dialog to browse media sources, such as CD-ROM, for the sources of other installable products.</span></span> <span data-ttu-id="a9c35-105">Das Durchsuchen anderer Produkte wird verhindert, unabhängig davon, ob die Installation mit erweiterten Berechtigungen erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a9c35-105">Browsing for other products is prevented regardless of whether the installation is done with elevated privileges.</span></span> <span data-ttu-id="a9c35-106">Der Benutzer kann das Produkt weiterhin von einem Medium aus neu installieren, wenn der Benutzer über eine ordnungsgemäß bezeichnete Medienquelle verfügt.</span><span class="sxs-lookup"><span data-stu-id="a9c35-106">It is still possible for the user to reinstall the product from media if the user has a correctly labeled media source.</span></span>

## <a name="registry-key"></a><span data-ttu-id="a9c35-107">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="a9c35-107">Registry Key</span></span>

<span data-ttu-id="a9c35-108">**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="a9c35-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a9c35-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a9c35-109">Data Type</span></span>

<span data-ttu-id="a9c35-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a9c35-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c35-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9c35-111">Remarks</span></span>

<span data-ttu-id="a9c35-112">Beachten Sie, dass die [**disablemedia**](-disablemedia.md) -Eigenschaft eine andere Auswirkung hat als die disablemedia-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a9c35-112">Note that the [**DISABLEMEDIA**](-disablemedia.md) property has a different effect than the DisableMedia policy.</span></span> <span data-ttu-id="a9c35-113">Wenn Sie die System Richtlinie "disablemedia" festlegen, wird nur das Durchsuchen von Medienquellen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a9c35-113">Setting the DisableMedia system policy, only disables browsing to media sources.</span></span> <span data-ttu-id="a9c35-114">Durch Festlegen der **disablemedia** -Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert.</span><span class="sxs-lookup"><span data-stu-id="a9c35-114">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="a9c35-115">Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch trotzdem eine Medienquelle durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="a9c35-115">If browsing is enabled however, a user may still browse to a media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9c35-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a9c35-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9c35-117">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="a9c35-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



