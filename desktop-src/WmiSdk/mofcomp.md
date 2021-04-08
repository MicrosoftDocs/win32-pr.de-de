---
description: Der MOF-Compiler (Managed Object Format) analysiert eine Datei, die MOF-Anweisungen enthält, und fügt die Klassen und Klassen Instanzen, die in der Datei definiert sind, dem WMI-Repository hinzu.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: Mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863324"
---
# <a name="mofcomp"></a><span data-ttu-id="5013b-103">Mofcomp</span><span class="sxs-lookup"><span data-stu-id="5013b-103">mofcomp</span></span>

<span data-ttu-id="5013b-104">Der [*MOF-Compiler (Managed Object Format)*](gloss-m.md) analysiert eine Datei, die MOF-Anweisungen enthält, und fügt die Klassen und Klassen Instanzen, die in der Datei definiert sind, dem WMI-Repository hinzu.</span><span class="sxs-lookup"><span data-stu-id="5013b-104">The [*Managed Object Format (MOF)*](gloss-m.md) compiler parses a file containing MOF statements and adds the classes and class instances defined in the file to the WMI repository.</span></span> <span data-ttu-id="5013b-105">MOF-Dateien werden normalerweise während der Installation der Systeme, mit denen Sie bereitgestellt werden, automatisch kompiliert, aber Sie können MOF-Dateien auch mit diesem Tool kompilieren.</span><span class="sxs-lookup"><span data-stu-id="5013b-105">MOF files are usually automatically compiled during the installation of the systems with which they are provided, but you can also compile MOF files by using this tool.</span></span>

<span data-ttu-id="5013b-106">Weitere Informationen zum Suchen und Verwenden von mofcomp.exe finden [Sie unter Verwenden von WMI-Verwaltungs Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="5013b-106">For more information about locating and using mofcomp.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span> <span data-ttu-id="5013b-107">Weitere Informationen zum Entfernen von Klassen und Instanzen aus dem WMI-Repository finden Sie im [**pragma deleteclass**](pragma-deleteclass.md) -Präprozessorbefehl.</span><span class="sxs-lookup"><span data-stu-id="5013b-107">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="5013b-108">Im folgenden Codebeispiel wird gezeigt, wie der MOF-Compiler für eine Datei ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5013b-108">The following code example shows how to run the MOF compiler on a file.</span></span>

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a><span data-ttu-id="5013b-109">Switches</span><span class="sxs-lookup"><span data-stu-id="5013b-109">Switches</span></span>

<dl> <dt>

<span data-ttu-id="5013b-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-AutoRecover**</span><span class="sxs-lookup"><span data-stu-id="5013b-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-111">Fügt die benannte MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden.</span><span class="sxs-lookup"><span data-stu-id="5013b-111">Adds the named MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="5013b-112">Die Liste der Auto Wiederherstellen-MOF-Dateien wird im Registrierungsschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="5013b-112">The list of autorecover MOF files is stored in the registry key:</span></span>

<span data-ttu-id="5013b-113">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**</span><span class="sxs-lookup"><span data-stu-id="5013b-113">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM\\**</span></span>

<span data-ttu-id="5013b-114">Die in diesem Registrierungs Eintrag aufgeführten MOF-Dateien müssen sich auf dem lokalen Computer befinden, da MOF-Dateien, die den **Auto Wiederherstellen** -Befehl verwenden, keine MOF-Dateien wiederherstellen können, die sich auf einem Remote Computer befinden</span><span class="sxs-lookup"><span data-stu-id="5013b-114">The MOF files listed in this registry entry must reside on the local computer because MOF files that use the **autorecover** command cannot recover MOF files located on a remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="5013b-115">Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung in der MOF-Datei ( [*Managed Object Format*](gloss-m.md) ).</span><span class="sxs-lookup"><span data-stu-id="5013b-115">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format*](gloss-m.md) (MOF) file.</span></span>

 

</dd> <dt>

<span data-ttu-id="5013b-116"><span id="-check"></span><span id="-CHECK"></span>**-Überprüfen**</span><span class="sxs-lookup"><span data-stu-id="5013b-116"><span id="-check"></span><span id="-CHECK"></span>**-check**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-117">Fordert an, dass der Compiler eine Syntax nur überprüft und entsprechende Fehlermeldungen druckt.</span><span class="sxs-lookup"><span data-stu-id="5013b-117">Requests that the compiler perform a syntax check only and print appropriate error messages.</span></span> <span data-ttu-id="5013b-118">Mit diesem Schalter kann kein anderer Switch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5013b-118">No other switch can be used with this switch.</span></span> <span data-ttu-id="5013b-119">Bei Verwendung dieses Schalters wird keine Verbindung mit Windows-Verwaltungsinstrumentation (WMI) hergestellt, und es werden keine Änderungen am WMI-Repository vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="5013b-119">When this switch is used, no connection to Windows Management Instrumentation (WMI) is established and no modifications to the WMI repository are made.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _Wert von NamespacePath_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<**_namespacepath_*_>_*</span></span>
</dt> <dd><span data-ttu-id="5013b-121">Fordert an, dass der Compiler die MOF-Datei in den Namespace lädt, der als *Wert von NamespacePath* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5013b-121">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="5013b-122">Das kompilierte MOF wird in den Standard-Standard Namespace "Standard" geladen, \\ sofern dieser Schalter nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5013b-122">The compiled MOF is loaded into the default Mofcomp namespace, root\\default, unless this switch is used.</span></span> <span data-ttu-id="5013b-123">Sie können auch den **\# pragma-Namespace** des Präprozessorbefehls ("_Namespace Pfad_*_")_* in der MOF-Datei einfügen, um denselben Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="5013b-123">You can also insert the preprocessor command **\#pragma namespace ("**_namespace path_*_")_* in the MOF file to achieve the same effect.</span></span> <span data-ttu-id="5013b-124">Wenn sowohl der **-N: Switch-** als auch der \# <a href="pragma-namespace.md">pragma-Namespace</a> -Befehl verwendet werden, hat der \# **pragma-Namespace** **Auto Wiederherstellen** Priorität.</span><span class="sxs-lookup"><span data-stu-id="5013b-124">If both the **-N:** switch and the \#<a href="pragma-namespace.md">pragma namespace</a> command are used, \#**pragma namespace** **autorecover** takes priority.</span></span> <span data-ttu-id="5013b-125">In diesem Fall besteht die einzige Möglichkeit zum Kompilieren der MOF-Datei in einen anderen Namespace darin, die MOF-Datei zu bearbeiten und den \# **pragma-Namespace** -Befehl zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5013b-125">In this case, the only way to compile the MOF into another namespace is to edit the MOF file and change the \#**pragma namespace** command.</span></span> <span data-ttu-id="5013b-126">Ein Remote Computer kann mithilfe von \\ \\ MachineName root default angegeben werden \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="5013b-126">A remote computer can be specified using \\\\machinename\\root\\default.</span></span></dd> <dt>

<span data-ttu-id="5013b-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Klasse: "kreateonly"**</span><span class="sxs-lookup"><span data-stu-id="5013b-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-128">Fordert an, dass der Compiler keine Änderungen an vorhandenen Klassen vornimmt.</span><span class="sxs-lookup"><span data-stu-id="5013b-128">Requests that the compiler not make any changes to existing classes.</span></span> <span data-ttu-id="5013b-129">Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn eine in der MOF-Datei angegebene Klasse bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5013b-129">When this switch is used, the compile operation terminates if a class specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Class: ForceUpdate**</span><span class="sxs-lookup"><span data-stu-id="5013b-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-131">Erzwingt das Aktualisieren von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5013b-131">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="5013b-132">Angenommen, ein Klassen Qualifizierer ist in einer untergeordneten Klasse definiert, und die Basisklasse versucht, denselben Qualifizierer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5013b-132">For example, suppose a class qualifier is defined in a child class and the base class tries to add the same qualifier.</span></span> <span data-ttu-id="5013b-133">In **-Class: der ForceUpdate** -Modus löst der MOF-Compiler diesen Konflikt durch Löschen des in Konflikt stehenden Qualifizierers in der untergeordneten Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="5013b-133">In **-class:forceupdate** mode, the MOF compiler resolves this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="5013b-134">Wenn die untergeordnete Klasse über Instanzen verfügt, schlägt das erzwungene Update fehl.</span><span class="sxs-lookup"><span data-stu-id="5013b-134">If the child class has instances, the forced update fails.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-Klasse: safeupdate**</span><span class="sxs-lookup"><span data-stu-id="5013b-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-136">Ermöglicht das Aktualisieren von Klassen auch dann, wenn untergeordnete Klassen vorhanden sind, solange die Änderung keine Konflikte mit untergeordneten Klassen verursacht.</span><span class="sxs-lookup"><span data-stu-id="5013b-136">Allows updates of classes even if there are child classes, as long as the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="5013b-137">Dieses Flag ermöglicht beispielsweise das Hinzufügen einer neuen Eigenschaft zur Basisklasse, die nicht zuvor in untergeordneten Klassen erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="5013b-137">For example, this flag allows adding a new property to the base class that was not previously mentioned in child classes.</span></span> <span data-ttu-id="5013b-138">Wenn die untergeordneten Klassen Instanzen aufweisen, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="5013b-138">If the child classes have instances, the update fails.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-Klasse: updateonly**</span><span class="sxs-lookup"><span data-stu-id="5013b-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-140">Fordert an, dass der Compiler keine neuen Klassen erstellt.</span><span class="sxs-lookup"><span data-stu-id="5013b-140">Requests that the compiler not create any new classes.</span></span> <span data-ttu-id="5013b-141">Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn keine in der MOF-Datei angegebene Klasse vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5013b-141">When this switch is used, the compile operation terminates if a class specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-Instanz: updateonly**</span><span class="sxs-lookup"><span data-stu-id="5013b-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-143">Fordert an, dass der Compiler keine neuen Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="5013b-143">Requests that the compiler not create any new instances.</span></span> <span data-ttu-id="5013b-144">Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn keine in der MOF-Datei angegebene Instanz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5013b-144">When this switch is used, the compile operation terminates if an instance specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance: "kreateonly"**</span><span class="sxs-lookup"><span data-stu-id="5013b-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-146">Fordert an, dass der Compiler keine Änderungen an vorhandenen Instanzen vornimmt.</span><span class="sxs-lookup"><span data-stu-id="5013b-146">Requests that the compiler not make any changes to existing instances.</span></span> <span data-ttu-id="5013b-147">Wenn dieser Schalter verwendet wird, wird der Kompilierungs Vorgang beendet, wenn eine in der MOF-Datei angegebene Instanz bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5013b-147">When this switch is used, the compile operation terminates if an instance specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _Dateiname_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<**_filename_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-149">Fordert an, dass der Compiler eine binäre Version der MOF-Datei mit dem Namen *filename* erstellt, ohne Änderungen am WMI-Repository vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="5013b-149">Requests that the compiler create a binary version of the MOF file with the name *filename* without making any modifications to the WMI repository.</span></span>

<span data-ttu-id="5013b-150">Wenn Sie die Option **-B: <** _filename_ verwenden, *_>_* um eine binäre MOF-Datei zu erstellen, werden nur standardmäßige qualifizierervarianten im WMI-Repository gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5013b-150">If you use the **-B:<**_filename_*_>_* option to create a binary MOF file, only default qualifier flavors are stored in the WMI repository.</span></span>

<span data-ttu-id="5013b-151">Das binäre MOF-Format ist das zwischen Format für die Kombination eines WDM-Treibers mit dem MOF als Ressource.</span><span class="sxs-lookup"><span data-stu-id="5013b-151">Binary MOF format is the intermediate format for combining a WDM-driver with the MOF as a resource.</span></span> <span data-ttu-id="5013b-152">Die binäre MOF stellt Klassen und Instanzen wie eine MOF-Datei des Texts dar und wird komprimiert, bevor Sie auf dem Datenträger gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="5013b-152">The binary MOF represents classes and instances just as a text MOF file does and is compressed before it is stored on disk.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span><span class="sxs-lookup"><span data-stu-id="5013b-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span></span>
</dt> <dd>

<span data-ttu-id="5013b-154">Fordert an, dass der Compiler eine WMI-Syntax Überprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="5013b-154">Requests that the compiler perform a WMI syntax check.</span></span> <span data-ttu-id="5013b-155">Der Schalter **-B:** muss mit diesem Switch verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5013b-155">The **-B:** switch must be used with this switch.</span></span> <span data-ttu-id="5013b-156">Der **-WMI-** Schalter wird nur zum entwickeln binärer MOF-Dateien verwendet, die von WDM-Gerätetreibern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5013b-156">The **-WMI** switch is only used for building binary MOF files for use by WDM device drivers.</span></span> <span data-ttu-id="5013b-157">Dieser Schalter Ruft eine separate binäre MOF-Datei Prüfung auf, die ausgeführt wird, nachdem die binäre MOF-Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5013b-157">This switch invokes a separate binary MOF file checker, which runs after the binary MOF file is created.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: <** _Kennwort_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<**_Password_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-159">Gibt *das Kennwort* als Kennwort für den Computerbenutzer an, das bei der Anmeldung eingegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5013b-159">Specifies *Password* as the password for the computer user to enter when logging on.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U: <** _Benutzername_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<**_UserName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-161">Gibt den *Benutzer* Namen als Namen des Benutzers an, der sich anmeldet.</span><span class="sxs-lookup"><span data-stu-id="5013b-161">Specifies *UserName* as the name of the user logging on.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A: <** _Autorität_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<**_Authority_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-163">Gibt die *Autorität* als Autorität (Domänen Name) an, die bei der Anmeldung bei WMI verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5013b-163">Specifies *Authority* as the authority (domain name) to use when logging on to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF: <** _Pfad_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-165">Der Name der sprach neutralen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5013b-165">Name of the language neutral output.</span></span> <span data-ttu-id="5013b-166">Wird mit dem Switch **--Zusatz** verwendet, um den Namen der sprach neutralen MOF-Datei anzugeben, die generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5013b-166">Used with the **-AMENDMENT** switch to specify the name of the language-neutral MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL: <** _Pfad_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-168">Der Name der sprachspezifischen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5013b-168">Name of the language specific output.</span></span> <span data-ttu-id="5013b-169">Wird mit dem Switch **--Zusatz** verwendet, um den Namen der sprachspezifischen MOF-Datei anzugeben, die generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5013b-169">Used with the **-AMENDMENT** switch to specify the name of the language-specific MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-Zusatz: <**  Gebiets Schema *_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<**_Locale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-171">Teilt die MOF-Datei in sprachneutrale und spezifische Versionen auf.</span><span class="sxs-lookup"><span data-stu-id="5013b-171">Splits the MOF file into language-neutral and -specific versions.</span></span> <span data-ttu-id="5013b-172">Der MOF-Compiler erstellt eine sprachneutrale Form der MOF-Datei, für die alle geänderten Qualifizierer entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="5013b-172">The MOF compiler creates a language-neutral form of the MOF file that has all amended qualifiers removed.</span></span> <span data-ttu-id="5013b-173">Außerdem wird eine lokalisierte Version der MOF-Datei mit einer MFL-Dateinamenerweiterung erstellt.</span><span class="sxs-lookup"><span data-stu-id="5013b-173">A localized version of the MOF file is also created with an MFL file name extension.</span></span> <span data-ttu-id="5013b-174">Der *locale* -Parameter gibt den Namen des untergeordneten Namespace an, der die lokalisierten Klassendefinitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="5013b-174">The *Locale* parameter specifies the name of the child namespace that contains the localized class definitions.</span></span> <span data-ttu-id="5013b-175">Das Format des *locale* -Parameters ist MS \_ xxx, wobei xxx der hexadezimale Wert der Windows-LCID ist.</span><span class="sxs-lookup"><span data-stu-id="5013b-175">The format of the *Locale* parameter is MS\_xxx where xxx is the hexadecimal value of the Windows LCID.</span></span> <span data-ttu-id="5013b-176">Beispielsweise ist das Gebiets Schema für amerikanisches Englisch MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="5013b-176">For example, the locale for American English is MS\_409.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-Er <** _resourceName_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <**_ResourceName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-178">Extrahiert binäres MOF aus einer benannten Ressource.</span><span class="sxs-lookup"><span data-stu-id="5013b-178">Extracts binary MOF from a named resource.</span></span> <span data-ttu-id="5013b-179">Mit diesem Switch wird die binäre MOF-Datei aus der-Klasse im WMI-Repository abgerufen, während der-B-Switch das binäre MOF-Format aus einer MOF-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="5013b-179">This switch gets the binary MOF from the class in the WMI repository while the -B switch creates the binary MOF format from a MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _resourcelocale_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<**_ResourceLocale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-181">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5013b-181">Optional.</span></span> <span data-ttu-id="5013b-182">Extrahiert die lokalisierten MOF-Beschreibungen aus der binären MOF-Datei, wenn Sie mit dem Schalter-er verwendet wird</span><span class="sxs-lookup"><span data-stu-id="5013b-182">Extracts the localized MOF descriptions from the binary MOF when used with -ER switch.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_Die_*_>_*</span><span class="sxs-lookup"><span data-stu-id="5013b-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="5013b-184">Der Name der Datei, die analysiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5013b-184">Name of the file to parse.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="5013b-185">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5013b-185">Return Values</span></span>

<span data-ttu-id="5013b-186">Beim ersten Vorgang führt der MOF-Compiler eine Syntax Überprüfung für die MOF-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="5013b-186">As its first operation, the MOF compiler performs a syntax check on the MOF file.</span></span> <span data-ttu-id="5013b-187">Wenn der Compiler Fehler findet, wird eine Fehlermeldung ausgegeben, und der Prozess wird beendet.</span><span class="sxs-lookup"><span data-stu-id="5013b-187">If the compiler finds any errors, it prints an error message and the process terminates.</span></span>

<span data-ttu-id="5013b-188">Der MOF-Compiler kann die folgenden Werte zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="5013b-188">The MOF compiler can return the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5013b-189"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="5013b-189"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="5013b-190">Der MOF-Kompilierungs Vorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5013b-190">MOF compile operation was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-191"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="5013b-191"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="5013b-192">Der MOF-Compiler konnte keine Verbindung mit dem WMI-Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="5013b-192">The MOF compiler could not connect with the WMI server.</span></span> <span data-ttu-id="5013b-193">Dies ist entweder auf einen Semantik Fehler, wie z. b. eine Inkompatibilität mit dem vorhandenen WMI-Repository oder ein tatsächlicher Fehler, wie z. b. das Starten des WMI-Servers.</span><span class="sxs-lookup"><span data-stu-id="5013b-193">This is either because of a semantic error such as an incompatibility with the existing WMI repository or an actual error such as the failure of the WMI server to start.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-194"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="5013b-194"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="5013b-195">Mindestens ein Befehls Zeilenschalter war ungültig.</span><span class="sxs-lookup"><span data-stu-id="5013b-195">One or more command-line switches were not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5013b-196"><span id="3"></span>€</span><span class="sxs-lookup"><span data-stu-id="5013b-196"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="5013b-197">Ein MOF-Syntax Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5013b-197">A MOF syntax error occurred.</span></span>

</dd> </dl>

<span data-ttu-id="5013b-198">Wenn die MOF-Datei ordnungsgemäß analysiert wird, aber versucht wird, einen Vorgang auszuführen, der durch einen Befehls Zeilenschalter unzulässig ist, gibt der Compiler einen Fehlercode zurück, der von WMI generiert wurde, und nicht die Rückgabecodes, die in der obigen Liste aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5013b-198">If the MOF file is parsed correctly, but an attempt is made to perform an operation that is forbidden by a command-line switch, the compiler returns an error code generated by WMI instead of any of the return codes listed in the list preceding.</span></span> <span data-ttu-id="5013b-199">Beispielsweise wird ein WMI-Fehlercode zurückgegeben, wenn der Schalter **-instance: updateonly** angegeben wird und die MOF-Datei versucht, eine Instanz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5013b-199">For example, a WMI error code is returned when the **-instance:updateonly** switch is specified and the MOF file attempts to create an instance.</span></span>

<span data-ttu-id="5013b-200">Wenn die [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) -Präprozessoranweisung nicht in der Datei enthalten ist, wird die folgende Warnung zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="5013b-200">If the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement is not in the file, then the following warning is returned:</span></span>

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a><span data-ttu-id="5013b-201">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5013b-201">Remarks</span></span>

<span data-ttu-id="5013b-202">Der MOF-Compiler ist im Verzeichnis% windir% \\ system32 \\ WBEM verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5013b-202">The MOF Compiler is available in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="5013b-203">Sie müssen die MOF-Datei als Parameter des MOF-Compilers angeben.</span><span class="sxs-lookup"><span data-stu-id="5013b-203">You must specify the MOF file as the parameter of the MOF Compiler.</span></span> <span data-ttu-id="5013b-204">Sie können auch einen AutoRecover-Schalter angeben, wenn die MOF-Datei automatisch erneut kompiliert werden soll, wenn das CIM-Repository jemals automatisch wieder hergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5013b-204">You can also specify an Autorecover switch if you want the MOF file to be automatically recompiled if the CIM Repository ever has to be automatically recovered.</span></span> <span data-ttu-id="5013b-205">Wenn Sie weitere Informationen erhalten, geben Sie " **MUF Comp/?**</span><span class="sxs-lookup"><span data-stu-id="5013b-205">For more information, type **Mofcomp /?**</span></span> <span data-ttu-id="5013b-206">an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="5013b-206">at the command prompt.</span></span>

<span data-ttu-id="5013b-207">Eine MOF-Datei, die den Unicode-Zeichensatz verwendet, enthält eine Signatur als die ersten zwei Bytes der Datei.</span><span class="sxs-lookup"><span data-stu-id="5013b-207">A MOF file that uses the Unicode character set contains a signature as the first two bytes of the file.</span></span> <span data-ttu-id="5013b-208">Diese Signatur ist entweder u + FFFE oder u + FEFF, abhängig von der Byte Reihenfolge der Datei.</span><span class="sxs-lookup"><span data-stu-id="5013b-208">This signature is either U+FFFE or U+FEFF, depending on the byte ordering of the file.</span></span>

<span data-ttu-id="5013b-209">Wenn beim Analyse-Prozess keine Fehler auftreten, stellt der MOF-Compiler eine Verbindung mit dem WMI-Server her, der auf dem lokalen Computer ausgeführt wird, es sei denn, der Schalter **-Check** ist angegeben</span><span class="sxs-lookup"><span data-stu-id="5013b-209">When no errors occur in the parsing process, the MOF compiler connects to the WMI server running on the local computer unless the **-check** switch is specified.</span></span> <span data-ttu-id="5013b-210">Klassen und Instanzen, die in der MOF-Datei definiert sind, werden dem WMI-Repository hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5013b-210">Classes and instances defined in the MOF file are added to the WMI repository.</span></span>

<span data-ttu-id="5013b-211">Wenn beim Aktualisieren des WMI-Repository ein Fehler auftritt, versucht der Compiler nicht, das Repository in seinen Zustand zurückzusetzen, bevor der Compiler mit der Verarbeitung begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="5013b-211">When an error occurs in updating the WMI repository, the compiler makes no attempt to return the repository to its state before the compiler began processing.</span></span>

<span data-ttu-id="5013b-212">**Windows 8:** Bei der Installation eines Anbieters behandelt "MUF Comp" die \[ Schlüssel \] -und \[ statischen \] Qualifizierer unabhängig von ihren tatsächlichen Werten als "true", wenn Sie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5013b-212">**Windows 8:** When installing a provider, mofcomp treats the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="5013b-213">Andere Qualifizierer werden als false behandelt, wenn Sie vorhanden sind, aber nicht explizit auf true festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5013b-213">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="5013b-214">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5013b-214">Requirements</span></span>



| <span data-ttu-id="5013b-215">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5013b-215">Requirement</span></span> | <span data-ttu-id="5013b-216">Wert</span><span class="sxs-lookup"><span data-stu-id="5013b-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5013b-217">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5013b-217">Minimum supported client</span></span><br/> | <span data-ttu-id="5013b-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5013b-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5013b-219">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5013b-219">Minimum supported server</span></span><br/> | <span data-ttu-id="5013b-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5013b-220">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5013b-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5013b-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5013b-222">**pragma-Namespace**</span><span class="sxs-lookup"><span data-stu-id="5013b-222">**pragma namespace**</span></span>](pragma-namespace.md)
</dt> <dt>

[<span data-ttu-id="5013b-223">Kompilieren von MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="5013b-223">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="5013b-224">Kompilieren lokalisierter MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="5013b-224">Compiling Localized MOF Files</span></span>](compiling-localized-mof-files.md)
</dt> <dt>

[<span data-ttu-id="5013b-225">Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="5013b-225">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="5013b-226">**Imufcompiler:: CompileFile**</span><span class="sxs-lookup"><span data-stu-id="5013b-226">**IMOFCompiler::CompileFile**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

