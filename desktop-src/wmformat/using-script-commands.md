---
title: Verwenden von Skript Befehlen
description: Verwenden von Skript Befehlen
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Media-Format-SDK, Skript Befehle
- Advanced Systems Format (ASF), Skript Befehle
- ASF (Advanced Systems Format), Skript Befehle
- Skripts, Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037045"
---
# <a name="using-script-commands"></a><span data-ttu-id="7c04e-107">Verwenden von Skript Befehlen</span><span class="sxs-lookup"><span data-stu-id="7c04e-107">Using Script Commands</span></span>

<span data-ttu-id="7c04e-108">Das Windows Media-Format-SDK unterstützt die Verwendung von Skript Befehlen, um Anwendungs Aktionen in ASF-Dateien zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7c04e-108">The Windows Media Format SDK supports the use of script commands to communicate application actions in ASF files.</span></span> <span data-ttu-id="7c04e-109">Jeder Skript Befehl besteht aus zwei Zeichen folgen, wobei es sich bei der ersten Zeichenfolge um den Befehlstyp handelt, bei dem es sich um die Befehlsdaten handelt.</span><span class="sxs-lookup"><span data-stu-id="7c04e-109">Each script command is made up of two strings, the first string is the type of command, the second is the command data.</span></span> <span data-ttu-id="7c04e-110">Beispielsweise können Sie den Skripttyp "URL" verwenden und eine gültige Internet-URL als Befehlsdaten übergeben.</span><span class="sxs-lookup"><span data-stu-id="7c04e-110">For example, you can use the script type "URL" and pass a valid Internet URL as the command data.</span></span> <span data-ttu-id="7c04e-111">Wenn eine Leseanwendung, die Skript Befehle vom Typ "URL" unterstützt, diesen Befehl empfängt, wird die angegebene Adresse in einem Browserfenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="7c04e-111">When a reading application that supports script commands of type "URL" receives this command, it will open the specified address in a browser window.</span></span>

<span data-ttu-id="7c04e-112">Das Windows Media-Format SDK bietet zwei Optionen zum Bereitstellen von Skripts in ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="7c04e-112">The Windows Media Format SDK provides two options for delivering script in ASF files.</span></span> <span data-ttu-id="7c04e-113">Sie können einen Skript Datenstrom erstellen oder Skript Befehle in den Header der Datei einschließen.</span><span class="sxs-lookup"><span data-stu-id="7c04e-113">You can create a script stream or you can include script commands in the header of the file.</span></span> <span data-ttu-id="7c04e-114">Skript Datenströme sind hilfreich, da die Skript Befehle in der Präsentationszeit sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="7c04e-114">Script streams are useful because the script commands are delivered in presentation time order.</span></span> <span data-ttu-id="7c04e-115">Wenn Sie Skript Befehle im Dateiheader verwenden, muss die Anwendung alle Skript Befehle abrufen, bevor die Wiedergabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7c04e-115">If you use script commands in the file header, your application will need to retrieve all of the script commands before starting playback.</span></span> <span data-ttu-id="7c04e-116">Sie müssen die Präsentations Zeiten von Skript Befehlen nachverfolgen und zum richtigen Zeitpunkt auf Sie reagieren.</span><span class="sxs-lookup"><span data-stu-id="7c04e-116">You must keep track of the presentation times of script commands and respond to them at the right time.</span></span>

<span data-ttu-id="7c04e-117">In den folgenden Abschnitten wird beschrieben, wie Skript Befehle in eine ASF-Datei eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7c04e-117">The following sections describe how to include script commands in an ASF file.</span></span>



| <span data-ttu-id="7c04e-118">`Section`</span><span class="sxs-lookup"><span data-stu-id="7c04e-118">Section</span></span>                                                                                                                | <span data-ttu-id="7c04e-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c04e-119">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="7c04e-120">So verwenden Sie einen Skript Datenstrom</span><span class="sxs-lookup"><span data-stu-id="7c04e-120">To Use a Script Stream</span></span>](to-use-a-script-stream.md)                                                                   | <span data-ttu-id="7c04e-121">Beschreibt das Einschließen von Skript Befehlen in einen Skript Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="7c04e-121">Describes how to include script commands in a script stream.</span></span> |
| [<span data-ttu-id="7c04e-122">So fügen Sie dem Header Skript Daten hinzu</span><span class="sxs-lookup"><span data-stu-id="7c04e-122">To Add Script Data to the Header</span></span>](to-add-script-data-to-the-header.md)                                               | <span data-ttu-id="7c04e-123">Beschreibt das Einschließen von Skript Befehlen in den Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="7c04e-123">Describes how to include script commands in the file header.</span></span> |
| [<span data-ttu-id="7c04e-124">Verwenden von Skript Befehlen, die von Windows Media Player unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="7c04e-124">Using Script Commands Supported by Windows Media Player</span></span>](using-script-commands-supported-by-windows-media-player.md) | <span data-ttu-id="7c04e-125">Beschreibt die Skript Befehle, die von Windows Media Player verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c04e-125">Describes the script commands used by Windows Media Player.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="7c04e-126">In früheren Versionen des Windows Media Format SDK wurden Skript Datenströme verwendet, um Webadressen zu öffnen, die dem Inhalt einer ASF-Datei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7c04e-126">In previous versions of the Windows Media Format SDK, script streams were used to open Web addresses corresponding to the content of an ASF file.</span></span> <span data-ttu-id="7c04e-127">Sie können jetzt Webstreams verwenden, um mit synchronisierten Webseiten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7c04e-127">You can now use Web streams to work with synchronized Web pages.</span></span> <span data-ttu-id="7c04e-128">Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="7c04e-128">For more information.</span></span> <span data-ttu-id="7c04e-129">siehe [Webstreams](web-streams.md).</span><span class="sxs-lookup"><span data-stu-id="7c04e-129">see [Web Streams](web-streams.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7c04e-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c04e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c04e-131">**Skriptbefehle**</span><span class="sxs-lookup"><span data-stu-id="7c04e-131">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="7c04e-132">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="7c04e-132">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




