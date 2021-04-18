---
title: Erkennen von Windows-Media Player aus einer Anwendung
description: Erkennen von Windows-Media Player aus einer Anwendung
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, erkennen von Anwendungen
- Erkennen von Windows-Media Player aus Anwendungen
- Registrierung, erkennen von Windows-Media Player aus Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337809"
---
# <a name="detecting-windows-media-player-from-an-application"></a><span data-ttu-id="6ba70-106">Erkennen von Windows-Media Player aus einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="6ba70-106">Detecting Windows Media Player from an Application</span></span>

<span data-ttu-id="6ba70-107">Sie können ermitteln, welche Version von Windows Media Player installiert ist, indem Sie den folgenden Registrierungsschlüssel überprüfen:</span><span class="sxs-lookup"><span data-stu-id="6ba70-107">You can determine what version of Windows Media Player is installed by checking the following registry key:</span></span>

<span data-ttu-id="6ba70-108">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Active Setup \\ installierte Komponenten**</span><span class="sxs-lookup"><span data-stu-id="6ba70-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Active Setup\\Installed Components**</span></span>

<span data-ttu-id="6ba70-109">Informationen zu Windows Media Player 6,4 finden Sie unter Key **{22d6f 312-b0f 6-11D0-94ab-0080c74c7e95}**.</span><span class="sxs-lookup"><span data-stu-id="6ba70-109">For Windows Media Player 6.4, look at key **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.</span></span>

<span data-ttu-id="6ba70-110">Informationen zu Windows Media Player 7 oder höher finden Sie unter Key **{6BF 52a52-394a-11d3-b153-00c04f 79faa6}**.</span><span class="sxs-lookup"><span data-stu-id="6ba70-110">For Windows Media Player 7 or later, look at key **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.</span></span>

<span data-ttu-id="6ba70-111">Unter einem dieser Schlüssel, wenn die **isinstemstation**</span><span class="sxs-lookup"><span data-stu-id="6ba70-111">Under either of these keys, if the **IsInstalled**</span></span><dl> <dt>

<span data-ttu-id="6ba70-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6ba70-112">Data type</span></span>
</dt> <dd><span data-ttu-id="6ba70-113">DWORD</span><span class="sxs-lookup"><span data-stu-id="6ba70-113">DWORD</span></span></dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

<span data-ttu-id="6ba70-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6ba70-114">Data type</span></span>
</dt> <dd><span data-ttu-id="6ba70-115">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6ba70-115">string</span></span></dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a><span data-ttu-id="6ba70-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ba70-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ba70-117">**Neuverteilen von Windows Media Player-Software**</span><span class="sxs-lookup"><span data-stu-id="6ba70-117">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




