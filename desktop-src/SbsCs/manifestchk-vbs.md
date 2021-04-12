---
description: Die VBScript-Datei Manifestchk.vbs ist ein Überprüfungs Tool, das im Microsoft Windows Software Development Kit (SDK) zur Validierung von Anwendungs-und assemblymanifestressdateien bereitgestellt wird.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393594"
---
# <a name="manifestchkvbs"></a><span data-ttu-id="abfc6-103">Manifestchk.vbs</span><span class="sxs-lookup"><span data-stu-id="abfc6-103">Manifestchk.vbs</span></span>

<span data-ttu-id="abfc6-104">Die VBScript-Datei Manifestchk.vbs ist ein Überprüfungs Tool, das im Microsoft Windows Software Development Kit (SDK) zur Validierung von Anwendungs-und assemblymanifestressdateien bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="abfc6-104">The VBScript file Manifestchk.vbs is a validation tool provided in the Microsoft Windows Software Development Kit (SDK) that validates application and assembly manifest files.</span></span>

<span data-ttu-id="abfc6-105">Das Ausführen dieses Beispiels erfordert den Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="abfc6-105">Running this sample requires Windows Script Host.</span></span> <span data-ttu-id="abfc6-106">Weitere Informationen zu Windows Script Host finden Sie im Abschnitt Windows Script Host des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="abfc6-106">For more information about Windows Script Host, see the Windows Script Host section of the Windows SDK.</span></span> <span data-ttu-id="abfc6-107">Windows Script Host ist tatsächlich zwei Hosts.</span><span class="sxs-lookup"><span data-stu-id="abfc6-107">Windows Script Host is actually two hosts.</span></span> <span data-ttu-id="abfc6-108">CScript.exe ist die Version, mit der Sie Skripts von der Eingabeaufforderung aus ausführen können.</span><span class="sxs-lookup"><span data-stu-id="abfc6-108">CScript.exe is the version that enables you to run scripts from the command prompt.</span></span> <span data-ttu-id="abfc6-109">CScript.exe stellt Befehls Zeilenschalter für das Festlegen von Skript Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="abfc6-109">CScript.exe provides command-line switches for setting script properties.</span></span>

<span data-ttu-id="abfc6-110">Das Befehlszeilen Format lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="abfc6-110">The command-line format is the following:</span></span>

<span data-ttu-id="abfc6-111">**Cscript//nologo manifestchk.vbs/s:** *\[ Laufwerk: \] \[ Pfad \] Schema Dateiname* **/m:** *\[ Laufwerk: \] \[ path \] ManifestFileName* **\[ /q \] /t:** *Option*</span><span class="sxs-lookup"><span data-stu-id="abfc6-111">**Cscript //nologo manifestchk.vbs /s:** *\[drive:\]\[path\]schemafilename* **/m:** *\[drive:\]\[path\]manifestfilename* **\[/q\] /t:** *option*</span></span>

<span data-ttu-id="abfc6-112">Die für Manifestchk.vbs definierten Flags werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="abfc6-112">The flags defined for Manifestchk.vbs are described in the following table.</span></span>



| <span data-ttu-id="abfc6-113">Flag</span><span class="sxs-lookup"><span data-stu-id="abfc6-113">Flag</span></span> | <span data-ttu-id="abfc6-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abfc6-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abfc6-115">/s</span><span class="sxs-lookup"><span data-stu-id="abfc6-115">/s</span></span>   | <span data-ttu-id="abfc6-116">Gibt den Namen der Manifest-Schema Datei an, anhand derer überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="abfc6-116">Specifies the manifest schema file name to validate manifests against.</span></span> <span data-ttu-id="abfc6-117">Weitere Informationen finden Sie im Schema unter [Manifest-Datei Schema](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="abfc6-117">See the schema at [Manifest File Schema](manifest-file-schema.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="abfc6-118">/m</span><span class="sxs-lookup"><span data-stu-id="abfc6-118">/m</span></span>   | <span data-ttu-id="abfc6-119">Gibt den zu validierenden Manifest-Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="abfc6-119">Specifies the manifest file name to validate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="abfc6-120">/q</span><span class="sxs-lookup"><span data-stu-id="abfc6-120">/q</span></span>   | <span data-ttu-id="abfc6-121">Unterdrückt die gesamte Ausgabe in der Konsole.</span><span class="sxs-lookup"><span data-stu-id="abfc6-121">Suppresses all output to the console.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="abfc6-122">/t</span><span class="sxs-lookup"><span data-stu-id="abfc6-122">/t</span></span>   | <span data-ttu-id="abfc6-123">Gibt den Typ der Manifest-Datei an.</span><span class="sxs-lookup"><span data-stu-id="abfc6-123">Specifies the type of manifest file.</span></span> <span data-ttu-id="abfc6-124">Gültige Werte sind: am Validate das [Manifest-Datei Schema](manifest-file-schema.md) eines Assemblymanifests oder [](assembly-manifests.md) [Anwendungs Manifests](application-manifests.md) .</span><span class="sxs-lookup"><span data-stu-id="abfc6-124">The valid values are: AM   Validate the [manifest file schema](manifest-file-schema.md) of an [assembly manifest](assembly-manifests.md) or [application manifest](application-manifests.md)</span></span><br/> <span data-ttu-id="abfc6-125">PC überprüft das [Schema der Verleger Konfigurationsdatei](publisher-configuration-file-schema.md) einer [Verleger Konfigurationsdatei](publisher-configuration-files.md) .</span><span class="sxs-lookup"><span data-stu-id="abfc6-125">PC   Validate the [publisher configuration file schema](publisher-configuration-file-schema.md) of a [publisher configuration file](publisher-configuration-files.md)</span></span><br/> <span data-ttu-id="abfc6-126">AC überprüft das Anwendungs Konfigurationsdatei-Schema einer [Anwendungs Konfigurationsdatei](application-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="abfc6-126">AC   Validate the application configuration file schema of an [application configuration file](application-configuration-files.md).</span></span><br/> |



 

<span data-ttu-id="abfc6-127">Wenn das/q-Flag nicht angegeben ist, zeigt Manifestchk.vbs ausführliche Informationen zum ersten Fehler an, der in der Datei aufgetreten ist, und zeigt eine Meldung an, die angibt, ob der Überprüfungs Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="abfc6-127">If the /q flag is not specified, Manifestchk.vbs displays detailed information about the first error encountered in the file, and displays a message stating whether the validation process was successful or not.</span></span>

<span data-ttu-id="abfc6-128">Dieses Hilfsprogramm prüft folgendes:</span><span class="sxs-lookup"><span data-stu-id="abfc6-128">This utility checks for the following:</span></span>

-   <span data-ttu-id="abfc6-129">Eine gültige Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="abfc6-129">A valid command line.</span></span>
-   <span data-ttu-id="abfc6-130">MSXML Version 3 ist installiert.</span><span class="sxs-lookup"><span data-stu-id="abfc6-130">That MSXML version 3 is installed.</span></span>
-   <span data-ttu-id="abfc6-131">Das Manifest verwendet wohl geformtes XML.</span><span class="sxs-lookup"><span data-stu-id="abfc6-131">That the manifest uses well-formed XML.</span></span>
-   <span data-ttu-id="abfc6-132">, Dass das Manifest mit dem bereitgestellten Schema übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="abfc6-132">That the manifest agrees with the provided schema.</span></span> <span data-ttu-id="abfc6-133">Beachten Sie, dass Manifestchk.vbs die Manifestressource nur anhand der Angaben im bereitgestellten Schema überprüft.</span><span class="sxs-lookup"><span data-stu-id="abfc6-133">Note that Manifestchk.vbs verifies the manifest file based only on what is specified in the provided schema.</span></span> <span data-ttu-id="abfc6-134">Ein Beispiel für ein Manifest-Schema finden Sie unter [Manifest-Datei Schema](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="abfc6-134">For an example of a manifest schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="abfc6-135">Cscript.exe gibt den Wert 0 (null) zurück, wenn der Überprüfungsprozess erfolgreich war, und 1, wenn er nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="abfc6-135">Cscript.exe returns a value of 0 if the validation process was successful and 1 if it was not successful.</span></span> <span data-ttu-id="abfc6-136">Wenn ein Fehler in einem Befehlszeilenargument vorliegt, wird 2 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abfc6-136">It returns 2 if there is an error in a command line argument.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abfc6-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="abfc6-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abfc6-138">Parallele assemblyentwicklungtools</span><span class="sxs-lookup"><span data-stu-id="abfc6-138">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




