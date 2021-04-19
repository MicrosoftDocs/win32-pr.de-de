---
title: Registrierungs Einstellung für automatische Übernahme
description: Registrierungs Einstellung für automatische Übernahme
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341872"
---
# <a name="silent-acquisition-registry-setting"></a><span data-ttu-id="3d507-103">Registrierungs Einstellung für automatische Übernahme</span><span class="sxs-lookup"><span data-stu-id="3d507-103">Silent Acquisition Registry Setting</span></span>

<span data-ttu-id="3d507-104">Microsoft Windows Media Player verwendet den folgenden Registrierungs Wert, um zu bestimmen, ob die automatische Übernahme aktiviert werden soll, einen Status, in dem der Player die Nutzungsrechte automatisch herunterlädt, wenn der Benutzer geschützte Inhalte wieder gibt oder synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="3d507-104">Microsoft Windows Media Player uses the following registry value to determine whether to enable silent acquisition, a state in which the player downloads usage rights automatically when the user plays or syncs protected content.</span></span>

<span data-ttu-id="3d507-105">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Media Player** \\ **Preferences** \\ **silenterwerbs**</span><span class="sxs-lookup"><span data-stu-id="3d507-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**MediaPlayer**\\**Preferences**\\**SilentAcquisition**</span></span>

<span data-ttu-id="3d507-106">Der silenterwerbs-Wert weist die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="3d507-106">The SilentAcquisition value has the following form:</span></span>



| <span data-ttu-id="3d507-107">Name</span><span class="sxs-lookup"><span data-stu-id="3d507-107">Name</span></span>              | <span data-ttu-id="3d507-108">type</span><span class="sxs-lookup"><span data-stu-id="3d507-108">Type</span></span>           | <span data-ttu-id="3d507-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d507-109">Description</span></span>                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d507-110">Silenterwerbs</span><span class="sxs-lookup"><span data-stu-id="3d507-110">SilentAcquisition</span></span> | <span data-ttu-id="3d507-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3d507-111">**REG\_DWORD**</span></span> | <span data-ttu-id="3d507-112">Legen Sie diesen Wert auf 1 fest, um die automatische Erfassung zu aktivieren, oder auf 0, um die automatische Erfassung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3d507-112">Set this value to 1 to enable silent acquisition, or set it to 0 to disable silent acquisition.</span></span> <span data-ttu-id="3d507-113">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="3d507-113">The default is 1.</span></span> |



 

<span data-ttu-id="3d507-114">Um einen Wert anzugeben, kann der Benutzer Windows Media Player starten, das Dialogfeld **Optionen** öffnen, auf die Registerkarte **Datenschutz** klicken und dann das Kontrollkästchen **Nutzungsrechte automatisch beim wiedergeben oder Synchronisieren einer Datei herunterladen** deaktivieren bzw. deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3d507-114">To specify a value, the user can start Windows Media Player, open the **Options** dialog box, click the **Privacy** tab, and then select or clear the **Download usage rights automatically when I play or sync a file** check box.</span></span> <span data-ttu-id="3d507-115">Wenn Sie dieses Kontrollkästchen aktivieren, wird silentacquisition auf 1 festgelegt. Wenn Sie das Kontrollkästchen deaktivieren, wird es auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d507-115">Selecting this check box sets SilentAcquisition to 1; clearing the check box sets it to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d507-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d507-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d507-117">**Registrierungs Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="3d507-117">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




