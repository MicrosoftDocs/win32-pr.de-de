---
description: Im folgenden Beispiel wird ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Beispiel für Datei Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4104c9bc241fed4bc698bd150b03d32a70e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127868"
---
# <a name="file-association-example"></a><span data-ttu-id="7342b-103">Beispiel für Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="7342b-103">File Association Example</span></span>

<span data-ttu-id="7342b-104">Im folgenden Beispiel erstellt ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc. einen neuen Audioplayer namens litwareplayer.</span><span class="sxs-lookup"><span data-stu-id="7342b-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="7342b-105">Litware möchte eine Datei Zuordnung zwischen litwareplayer und dessen primärem Dateityp entwerfen, der ein neu entwickeltes Audioformat verwendet, das eine gesamte AudioCD in weniger als 10 Kilobyte Arbeitsspeicher ohne Qualitätsverlust speichern kann.</span><span class="sxs-lookup"><span data-stu-id="7342b-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7342b-106">Dieses Thema gilt nicht für Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7342b-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="7342b-107">Die Art und Weise, wie standardmäßige Dateizuordnungen in Windows 10 geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7342b-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="7342b-108">Weitere Informationen finden Sie im Abschnitt zu den **Änderungen in Windows 10** für die Behandlung von Standard-apps in [diesem Beitrag](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="7342b-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="7342b-109">Entwerfen einer neuen Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="7342b-109">Designing a New File Association</span></span>

<span data-ttu-id="7342b-110">Das Unternehmen sollte die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="7342b-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="7342b-111">**Entscheiden Sie, ob der neue Dateityp als öffentlich oder privat behandelt werden soll.**</span><span class="sxs-lookup"><span data-stu-id="7342b-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="7342b-112">Dieser neue Dateityp ist ein Medientyp.</span><span class="sxs-lookup"><span data-stu-id="7342b-112">This new file type is a media type.</span></span> <span data-ttu-id="7342b-113">Da Benutzer Mediendateien auf verschiedenen Plattformen austauschen und es möglicherweise andere Anwendungen gibt, die das litwareplayer-Format lesen müssen, ist ein [öffentlicher](fa-file-types.md) Dateityp die geeignetste.</span><span class="sxs-lookup"><span data-stu-id="7342b-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="7342b-114">**Bestimmen Sie, ob dieser Dateityp bereits definiert ist.**</span><span class="sxs-lookup"><span data-stu-id="7342b-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="7342b-115">Überprüfen Sie die Internet Assigned Numbers Authority (IANA)-MIME-Datenbank und andere öffentliche Dateityp Datenbanken im Internet, um zu bestimmen, dass kein vergleichbarer Dateityp definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7342b-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="7342b-116">Da es sich um ein neues Dateiformat handelt, müssen Sie einen neuen Dateityp definieren.</span><span class="sxs-lookup"><span data-stu-id="7342b-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="7342b-117">**Definieren Sie eine Dateinamenerweiterung für den neuen Dateityp.**</span><span class="sxs-lookup"><span data-stu-id="7342b-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="7342b-118">Die Entwickler wählen den aus `.opa-ltw-audio` , der seine Hersteller Abkürzung und einen Hinweis zum Inhalt der Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="7342b-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="7342b-119">Research stellt fest, dass die Erweiterung nicht von anderen Personen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7342b-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="7342b-120">Im Anschluss an die aktuellen Empfehlungen ist keine kurze Erweiterung definiert.</span><span class="sxs-lookup"><span data-stu-id="7342b-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="7342b-121">**Definieren Sie einen MIME-Typ für den Dateityp, und registrieren Sie ihn bei der IANA.**</span><span class="sxs-lookup"><span data-stu-id="7342b-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="7342b-122">Litware definiert den neuen MIME-Typ als *Audiodatei/litwareplayer. 1* und bereitet eine MIME-Typanwendung vor, indem er die in Request for Comments (RFC)-Nummern 2045, 2046, 2047 und 2048 aufgeführten Richtlinien unter folgt.</span><span class="sxs-lookup"><span data-stu-id="7342b-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="7342b-123">Anschließend übermitteln Sie die Anwendung an die IANA, mit der der neue Dateityp der Datenbank registrierter MIME-Typen hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7342b-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="7342b-124">**Stellen Sie fest, ob eine ProgID für den Dateityp vorhanden ist.**</span><span class="sxs-lookup"><span data-stu-id="7342b-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="7342b-125">Da es sich um einen neuen Dateityp handelt, ist keine [ProgID](fa-progids.md) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7342b-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="7342b-126">Litware legt fest, wie eine neue ProgID für litwareplayer entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="7342b-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="7342b-127">Sie entscheiden sich für den anzeigen Amen "litwareplayer-Audioplayer" (der als Ressource in der LitwarePlayer.exe-Datei gespeichert ist) und entwerfen ein Standard Symbol für Dateien, die mit litwareplayer verknüpft sind (ebenfalls in LitwarePlayer.exe gespeichert).</span><span class="sxs-lookup"><span data-stu-id="7342b-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="7342b-128">Da litwareplayer eine neue Anwendung ist, ist dies eine ProgID der Version 1.</span><span class="sxs-lookup"><span data-stu-id="7342b-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="7342b-129">**Registrieren Sie die ProgID.**</span><span class="sxs-lookup"><span data-stu-id="7342b-129">**Register the ProgID.**</span></span> <span data-ttu-id="7342b-130">Wenn litwareplayer installiert ist, erstellt das Installationsprogramm den folgenden [ProgID](fa-progids.md) -Eintrag in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7342b-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    <span data-ttu-id="7342b-131">In der Befehlstaste wird %1 als Pfad zur wieder zugebende Datei übermittelt.</span><span class="sxs-lookup"><span data-stu-id="7342b-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="7342b-132">**Registrieren Sie die Dateinamenerweiterung für den Dateityp.**</span><span class="sxs-lookup"><span data-stu-id="7342b-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="7342b-133">Wenn litwareplayer installiert ist, erstellt das Installationsprogramm die folgenden Einträge für die benutzerdefinierte Dateityp Erweiterung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7342b-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="7342b-134">Wenn eine Datei Zuordnung erstellt oder geändert wird, Benachrichtigen Sie das System, dass durch Aufrufen von [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)eine Änderung vorgenommen wurde, und geben Sie dabei das shcne- \_ Ereignis "assocchanged" an.</span><span class="sxs-lookup"><span data-stu-id="7342b-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="7342b-135">Wenn dies nicht der Fall ist, erkennt die Shell möglicherweise keine Änderungen, die bis zum Systemneustart vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="7342b-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="7342b-136">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7342b-136">Additional Resources</span></span>

-   [<span data-ttu-id="7342b-137">Einführung in Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="7342b-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="7342b-138">Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü</span><span class="sxs-lookup"><span data-stu-id="7342b-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="7342b-139">[Registrieren einer Anwendung in einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7342b-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="7342b-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7342b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7342b-141">Bewährte Methoden für Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="7342b-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="7342b-142">Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="7342b-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="7342b-143">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="7342b-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="7342b-144">Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)</span><span class="sxs-lookup"><span data-stu-id="7342b-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
