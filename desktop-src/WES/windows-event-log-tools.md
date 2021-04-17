---
title: Windows-Ereignisprotokoll Tools
description: Das Windows-Ereignisprotokoll stellt die folgenden Tools bereit, die Sie zum Erstellen Ihres Anbieters verwenden können.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390097"
---
# <a name="windows-event-log-tools"></a><span data-ttu-id="1b9de-103">Windows-Ereignisprotokoll Tools</span><span class="sxs-lookup"><span data-stu-id="1b9de-103">Windows Event Log Tools</span></span>

<span data-ttu-id="1b9de-104">Das Windows-Ereignisprotokoll stellt die folgenden Tools bereit, die Sie zum Erstellen Ihres Anbieters verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1b9de-104">Windows Event Log provides the following tools that you use to build your provider.</span></span>



| <span data-ttu-id="1b9de-105">Tool</span><span class="sxs-lookup"><span data-stu-id="1b9de-105">Tool</span></span>                                                           | <span data-ttu-id="1b9de-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b9de-106">Description</span></span>                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b9de-107">**Nachrichten Compiler (MC.exe)**</span><span class="sxs-lookup"><span data-stu-id="1b9de-107">**Message Compiler (MC.exe)**</span></span>](message-compiler--mc-exe-.md)  | <span data-ttu-id="1b9de-108">Ein Befehlszeilen-Hilfsprogramm, mit dem Instrumentierungs Manifeste und Nachrichtentext Dateien kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="1b9de-108">A command line utility used to compile instrumentation manifests and message text files.</span></span> |
| <span data-ttu-id="1b9de-109">WevtUtil.exe</span><span class="sxs-lookup"><span data-stu-id="1b9de-109">WevtUtil.exe</span></span>                                                   | <span data-ttu-id="1b9de-110">Ein Befehlszeilen-Hilfsprogramm, das hauptsächlich zum Registrieren Ihres Anbieters auf dem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b9de-110">A command line utility used primarily to register your provider on the computer.</span></span> <span data-ttu-id="1b9de-111">Sie können Sie auch verwenden, um Metadateninformationen über den Anbieter, seine Ereignisse und die Kanäle zu erhalten, in denen Ereignisse protokolliert werden, und um Ereignisse aus einer Kanal-oder Protokolldatei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="1b9de-111">You can also use it to get metadata information about the provider, its events, and the channels to which it logs events, and to query events from a channel or log file.</span></span> <span data-ttu-id="1b9de-112">Das WevtUtil.exe Tool ist in% windir% \\ system32 enthalten.</span><span class="sxs-lookup"><span data-stu-id="1b9de-112">The WevtUtil.exe tool is included in %windir%\\System32.</span></span> <span data-ttu-id="1b9de-113">Geben Sie "wevtutil/?" ein, um Nutzungsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b9de-113">For usage information, enter "wevtutil /?"</span></span> <span data-ttu-id="1b9de-114">an einer Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="1b9de-114">at a command prompt.</span></span><br/> <span data-ttu-id="1b9de-115">Dieser Befehl ist auf Mitglieder der Gruppe "Administratoren" beschränkt und muss mit erhöhten Rechten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1b9de-115">This command is limited to members of the Administrators group and must be run with elevated privileges.</span></span>|
