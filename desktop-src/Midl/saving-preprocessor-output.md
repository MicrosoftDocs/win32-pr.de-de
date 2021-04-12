---
title: Speichern der Präprozessorausgabe
description: Das Anzeigen der Präprozessorausgabe kann eine effektive Methode zur Problembehandlung sein, z. b. Wenn eine ungültige IDL-, c-oder c-präprozessorsyntax auftritt oder wenn gefälschte-D-Werte in der Mittell-Befehlszeile zu einem Fehler in der Mittell melden.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- Mittlerer l-compilermittell, Speichern der Präprozessorausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388424"
---
# <a name="saving-preprocessor-output"></a><span data-ttu-id="2fa63-104">Speichern der Präprozessorausgabe</span><span class="sxs-lookup"><span data-stu-id="2fa63-104">Saving Preprocessor Output</span></span>

<span data-ttu-id="2fa63-105">Das Anzeigen der Präprozessorausgabe kann eine effektive Methode zur Problembehandlung sein, z. b. Wenn eine ungültige IDL-, c-oder c-präprozessorsyntax auftritt oder wenn gefälschte-D-Werte in der Mittell-Befehlszeile zu einem Fehler in der Mittell melden.</span><span class="sxs-lookup"><span data-stu-id="2fa63-105">Viewing preprocessor output can be an effective troubleshooting method, such as when invalid IDL, C, or C-preprocessor syntax occurs, or when bogus -D values on the MIDL command line result in MIDL reporting arcane errors.</span></span> <span data-ttu-id="2fa63-106">Entwickler können auch die Präprozessorausgabe überprüfen, um zu bestimmen, welche Dateien und Definitionen im compilereingabestream vorhanden waren, z. b. Wenn ein schwieriger Fall des Konflikts mit der Typneudefinition aufgelöst werden muss.</span><span class="sxs-lookup"><span data-stu-id="2fa63-106">Developers may also want to examine preprocessor output to determine which files and definitions were present in the compiler input stream, such as when a difficult case of type redefinition conflict must be resolved.</span></span> <span data-ttu-id="2fa63-107">Oder seltener möchten bestimmte Entwickler möglicherweise private Switches für den Präprozessor mit [**/cpp \_ opt**](-cpp-opt.md)erzwingen, oder Sie möchten sehen, wie die Switches funktionieren.</span><span class="sxs-lookup"><span data-stu-id="2fa63-107">Or less commonly, certain developers may want to force private switches on the preprocessor with [**/cpp\_opt**](-cpp-opt.md), or may want to see how the switches work.</span></span>

<span data-ttu-id="2fa63-108">Die einfachste und am wenigsten verborgene Methode zum Abrufen der vorverarbeiteten Dateien aus einer Mittell-Kompilierung ist die Verwendung des Schalters " [**-savepp**](-savepp.md) ".</span><span class="sxs-lookup"><span data-stu-id="2fa63-108">The easiest and the least obtrusive way to obtain the preprocessed files from a MIDL compile run is to use the [**-savePP**](-savepp.md) switch.</span></span> <span data-ttu-id="2fa63-109">Mit dem Schalter " **-savepp** " wird verhindert, dass die temporären Dateien, die vom Präprozessor an die mittlere Zeit zurückgeleitet werden, von der Mitte gelöscht werden</span><span class="sxs-lookup"><span data-stu-id="2fa63-109">The **-savePP** switch simply prevents MIDL from deleting the temporary files that the preprocessor passes back to MIDL.</span></span> <span data-ttu-id="2fa63-110">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2fa63-110">Consider the following:</span></span>

<span data-ttu-id="2fa63-111">**Mittel l-savepp-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1-Oicf-ERV Win32 Stub. idl**</span><span class="sxs-lookup"><span data-stu-id="2fa63-111">**midl -savePP -Id:\\nt\\public\\sdk\\inc -DNTENV=1 -Oicf -env win32 stub.idl**</span></span>

<span data-ttu-id="2fa63-112">Diese Direktive kompiliert Stub. idl, behält aber alle präprozessordateien bei.</span><span class="sxs-lookup"><span data-stu-id="2fa63-112">This directive compiles Stub.idl, yet preserves all preprocessor files.</span></span>

> [!Note]  
> <span data-ttu-id="2fa63-113">In mittlerer l werden separate präprozessorausführungen für die IDL-und ACF-Datei (falls vorhanden) sowie für jede importierte Datei ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fa63-113">MIDL spawns separate preprocessor runs for IDL and ACF file (if present) as well as for every imported file.</span></span>

 

<span data-ttu-id="2fa63-114">Bei einer DCOM-Kompilierung werden in der Regel mehrere präprozessordateien erstellt, auch wenn Sie von der mittleren l als virtueller zusammenhängender Eingabedaten Strom verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2fa63-114">For a DCOM compile, several preprocessor files are typically produced, even though they are processed by MIDL as a virtual contiguous input stream.</span></span> <span data-ttu-id="2fa63-115">In einer typischen Windows-Programmierumgebung befinden sich die temporären Dateien im temporären Verzeichnis als Dateinamen wie z \* . b. Mid. tmp.</span><span class="sxs-lookup"><span data-stu-id="2fa63-115">In a typical Windows programming environment, the temporary files can be found in the Temp directory as file names such as MID\*.tmp.</span></span> <span data-ttu-id="2fa63-116">Wenn Sie die Präprozessorausgabe beibehalten, empfiehlt es sich, die aktuellen Dateien im Temp-Verzeichnis zu überwachen, um zu ermitteln, welche Dateien mit welcher präprozessorlaufzeit verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2fa63-116">If preserving preprocessor output, it is good practice to watch for recent files in the Temp directory to identify which files are associated with which preprocessor run.</span></span>

<span data-ttu-id="2fa63-117">In einfachen Fällen, z. b. wenn die kompilierte IDL-Datei keine anderen Dateien direkt oder indirekt importiert oder wenn die Datei der obersten Ebene untersucht wird, kann der Präprozessor direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2fa63-117">In simple cases, such as when the compiled IDL file does not import other files directly or indirectly, or when examining the top-level file, the preprocessor can be invoked directly.</span></span> <span data-ttu-id="2fa63-118">Wenn Sie den C/C++-Präprozessor direkt ausführen, können Fehler angezeigt werden, die durch die mittlere</span><span class="sxs-lookup"><span data-stu-id="2fa63-118">Executing C/C++ preprocessor directly can reveal errors masked or confused by MIDL.</span></span> <span data-ttu-id="2fa63-119">Die folgenden beiden präprozessorbefehlszeilen können z. b. für die oben genannte Mittel l-Zeile verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="2fa63-119">For example, the following two preprocessor command lines can be used for the previously quoted MIDL line:</span></span>

<span data-ttu-id="2fa63-120">**cl/E/nologo-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1 Stub. idl > Stub. PP**</span><span class="sxs-lookup"><span data-stu-id="2fa63-120">**cl /E /nologo -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl > stub.pp**</span></span>

<span data-ttu-id="2fa63-121">**cl/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1 Stub. idl**</span><span class="sxs-lookup"><span data-stu-id="2fa63-121">**cl /E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl**</span></span>

<span data-ttu-id="2fa63-122">In den ersten beiden Beispielen sind **/E** [**/nologo**](-nologo.md) die Schalter, die von der mittleren l beim Aufrufen des Präprozessors hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2fa63-122">In the first of these two examples, **/E** [**/nologo**](-nologo.md) are the switches that MIDL adds when invoking the preprocessor.</span></span> <span data-ttu-id="2fa63-123">Die Präprozessorausgabe wird an stdout (der Bildschirm) gesendet und erfordert daher eine Umleitung zu einer Datei zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="2fa63-123">The preprocessor output is sent to stdout (the screen), and therefore requires redirection to a file for examination.</span></span> <span data-ttu-id="2fa63-124">Im zweiten dieser Beispiele weist **/P** den Präprozessor an, die Ausgabe an eine. i-Datei umzuleiten. \* in diesem Fall würde eine Datei "Stub. i" im aktuellen Verzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="2fa63-124">In the second of these examples, **/P** directs the preprocessor to redirect the output to a \*.i file; in this case a Stub.i file would be created in the current directory.</span></span>

<span data-ttu-id="2fa63-125">Der Schalter " [**/cpp \_ opt**](-cpp-opt.md) " kann auch verwendet werden, um eine vorverarbeitete Datei abzurufen, aber die zuvor erwähnten Methoden sind schwierig und untergeordnet.</span><span class="sxs-lookup"><span data-stu-id="2fa63-125">The [**/cpp\_opt**](-cpp-opt.md) switch can also be used to obtain a preprocessed file, but is difficult and inferior to the previously mentioned methods.</span></span> <span data-ttu-id="2fa63-126">Im folgenden Beispiel wird auch eine Stub. i-Datei erstellt, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2fa63-126">The following example also produces a Stub.i file, as did the previous example.</span></span> <span data-ttu-id="2fa63-127">Die Anführungszeichen im folgenden Beispiel sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="2fa63-127">The quotes in the following example are essential:</span></span>

<span data-ttu-id="2fa63-128">**Mittel l-Oicf-Win32-cpp \_ Opt "/E/P-ID: \\ NT \\ Public \\ SDK \\ Inc-dntenv = 1" Stub. idl**</span><span class="sxs-lookup"><span data-stu-id="2fa63-128">**Midl -Oicf -win32 -cpp\_opt "/E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1" stub.idl**</span></span>

 

 




