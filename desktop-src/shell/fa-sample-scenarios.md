---
description: Im folgenden Beispiel wird ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Dateizuordnungsbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b92922bb907c4dd90b3e2bdc3d16c8e8b52e6a
ms.sourcegitcommit: b0d03febac36ff77cba034615b94ea103311398d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/19/2021
ms.locfileid: "107715788"
---
# <a name="file-association-example"></a><span data-ttu-id="a575e-103">Dateizuordnungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="a575e-103">File Association Example</span></span>

<span data-ttu-id="a575e-104">Im folgenden Beispiel erstellt ein hypothetisches Softwareentwicklungsunternehmen namens Litware, Inc. einen neuen Audioplayer namens LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="a575e-104">In the following example, a hypothetical software development company called Litware, Inc. creates a new audio player called LitwarePlayer.</span></span> <span data-ttu-id="a575e-105">Litware möchte eine Dateizuordnung zwischen LitwarePlayer und seinem primären Dateityp entwerfen. Dabei wird ein neu entwickeltes Audioformat verwendet, mit dem eine gesamte Audio-CD ohne Qualitätsverlust in weniger als 10 KB Arbeitsspeicher gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a575e-105">Litware wants to design a file association between LitwarePlayer and its primary file type, which uses a newly developed audio format that enables an entire audio CD to be stored in less than 10 kilobytes of memory with no loss of quality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a575e-106">Dieses Thema gilt nicht für Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a575e-106">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="a575e-107">Die Funktionsweise von Standarddateizuordnungen hat sich in Windows 10 geändert.</span><span class="sxs-lookup"><span data-stu-id="a575e-107">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="a575e-108">Weitere Informationen finden Sie im Abschnitt Änderungen an der Verarbeitung von **Standard-Apps durch Windows 10** in [diesem Beitrag](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="a575e-108">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

## <a name="designing-a-new-file-association"></a><span data-ttu-id="a575e-109">Entwerfen einer neuen Dateizuordnung</span><span class="sxs-lookup"><span data-stu-id="a575e-109">Designing a New File Association</span></span>

<span data-ttu-id="a575e-110">Das Unternehmen sollte die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="a575e-110">The company should take the following steps.</span></span>

1.  <span data-ttu-id="a575e-111">**Entscheiden Sie, ob der neue Dateityp als öffentlich oder privat behandelt werden soll.**</span><span class="sxs-lookup"><span data-stu-id="a575e-111">**Decide if the new file type should be treated as public or private.**</span></span> <span data-ttu-id="a575e-112">Dieser neue Dateityp ist ein Medientyp.</span><span class="sxs-lookup"><span data-stu-id="a575e-112">This new file type is a media type.</span></span> <span data-ttu-id="a575e-113">Da Benutzer Mediendateien auf verschiedenen Plattformen austauschen und es möglicherweise andere Anwendungen gibt, die das LitwarePlayer-Format lesen müssen, ist ein [öffentlicher](fa-file-types.md) Dateityp am besten geeignet.</span><span class="sxs-lookup"><span data-stu-id="a575e-113">Because users exchange media files across various platforms and there might be other applications that need to read the LitwarePlayer format, a [public](fa-file-types.md) file type is the most appropriate.</span></span>
2.  <span data-ttu-id="a575e-114">**Bestimmen Sie, ob dieser Dateityp bereits definiert ist.**</span><span class="sxs-lookup"><span data-stu-id="a575e-114">**Determine whether this file type is already defined.**</span></span> <span data-ttu-id="a575e-115">Überprüfen Sie die MIME-Datenbank der Internet Assigned Numbers Authority (IANA) und andere öffentliche Dateitypdatenbanken im Internet, um zu ermitteln, ob kein vergleichbarer Dateityp definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a575e-115">Check the Internet Assigned Numbers Authority (IANA) MIME database, and other public file type databases on the Internet to determine that no comparable file type has been defined.</span></span> <span data-ttu-id="a575e-116">Da es sich um ein neues Dateiformat handelt, müssen Sie einen neuen Dateityp definieren.</span><span class="sxs-lookup"><span data-stu-id="a575e-116">Because this is a new file format, you need to define a new file type.</span></span>
3.  <span data-ttu-id="a575e-117">**Definieren Sie eine Dateinamenerweiterung für den neuen Dateityp.**</span><span class="sxs-lookup"><span data-stu-id="a575e-117">**Define a file name extension for the new file type.**</span></span> <span data-ttu-id="a575e-118">Die Entwickler wählen die `.opa-ltw-audio` aus, die ihre Herstellerabkürzung und einen Hinweis dazu enthält, was die Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="a575e-118">The developers choose the `.opa-ltw-audio`, which incorporates their vendor abbreviation and a hint about the what the file contains.</span></span> <span data-ttu-id="a575e-119">Untersuchungen stellen fest, dass die Erweiterung nicht von anderen Personen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a575e-119">Research determines that the extension is not being used by anyone else.</span></span> <span data-ttu-id="a575e-120">Gemäß den aktuellen Empfehlungen wird keine kurze Erweiterung definiert.</span><span class="sxs-lookup"><span data-stu-id="a575e-120">Following current recommendations, no short extension is defined.</span></span>
4.  <span data-ttu-id="a575e-121">**Definieren Sie einen MIME-Typ für den Dateityp, und registrieren Sie ihn bei der IANA.**</span><span class="sxs-lookup"><span data-stu-id="a575e-121">**Define a MIME type for the file type and register it with the IANA.**</span></span> <span data-ttu-id="a575e-122">Litware definiert den neuen MIME-Typ als *audio/LitwarePlayer.1* und bereitet eine MIME-Typanwendung gemäß den Richtlinien unter RFC-Nummern 2045, 2046, 2047 und 2048 vor.</span><span class="sxs-lookup"><span data-stu-id="a575e-122">Litware defines the new MIME type as *audio/LitwarePlayer.1* and prepares a MIME type application, following the guidelines laid out in Request for Comments (RFC) numbers 2045, 2046, 2047, and 2048.</span></span> <span data-ttu-id="a575e-123">Anschließend übermitteln sie die Anwendung an die IANA, die der Datenbank mit registrierten MIME-Typen den neuen Dateityp hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="a575e-123">They then submit the application to the IANA, which adds the new file type to the database of registered MIME types.</span></span>
5.  <span data-ttu-id="a575e-124">**Bestimmen Sie, ob eine ProgID für den Dateityp vorhanden ist.**</span><span class="sxs-lookup"><span data-stu-id="a575e-124">**Determine whether a ProgID exists for the file type.**</span></span> <span data-ttu-id="a575e-125">Da es sich um einen neuen Dateityp handelt, ist dafür [keine ProgID](fa-progids.md) vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a575e-125">Because this is a new file type, no [ProgID](fa-progids.md) exists for it.</span></span> <span data-ttu-id="a575e-126">Litware setzt auf das Entwerfen einer neuen ProgID für LitwarePlayer.</span><span class="sxs-lookup"><span data-stu-id="a575e-126">Litware sets about designing a new ProgID for LitwarePlayer.</span></span> <span data-ttu-id="a575e-127">Sie entscheiden sich für den Benutzerfreundlichen Namen "LitwarePlayer Audio Player" (der als Ressource in der LitwarePlayer.exe-Datei gespeichert ist) und entwerfen ein Standardsymbol für Dateien, die LitwarePlayer zugeordnet sind (auch in LitwarePlayer.exe).</span><span class="sxs-lookup"><span data-stu-id="a575e-127">They decide on the friendly name "LitwarePlayer Audio Player" (which is stored as a resource in the LitwarePlayer.exe file), and they design a default icon to use for files associated with LitwarePlayer (also stored in LitwarePlayer.exe).</span></span> <span data-ttu-id="a575e-128">Da LitwarePlayer eine neue Anwendung ist, ist dies eine ProgID der Version 1.</span><span class="sxs-lookup"><span data-stu-id="a575e-128">Because LitwarePlayer is a new application, this is a version 1 ProgID.</span></span>
6.  <span data-ttu-id="a575e-129">**Registrieren Sie die ProgID.**</span><span class="sxs-lookup"><span data-stu-id="a575e-129">**Register the ProgID.**</span></span> <span data-ttu-id="a575e-130">Wenn LitwarePlayer installiert ist, erstellt das Installationsprogramm den folgenden [ProgID-Eintrag](fa-progids.md) in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a575e-130">When LitwarePlayer is installed, the installation program creates the following [ProgID](fa-progids.md) entry in the registry.</span></span>

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

    <span data-ttu-id="a575e-131">Im Befehlsschlüssel wird %1 als Pfad zur datei übergeben, die wieder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a575e-131">In the command key, %1 is passed as the path to the file to play.</span></span>

7.  <span data-ttu-id="a575e-132">**Registrieren Sie die Dateierweiterung für den Dateityp.**</span><span class="sxs-lookup"><span data-stu-id="a575e-132">**Register the file name extension for the file type.**</span></span> <span data-ttu-id="a575e-133">Wenn LitwarePlayer installiert ist, erstellt das Installationsprogramm die folgenden Einträge in der Registrierung für die benutzerdefinierte Dateityperweiterung.</span><span class="sxs-lookup"><span data-stu-id="a575e-133">When LitwarePlayer is installed, the installation program creates the following entries in the registry for its custom file type extension.</span></span>

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> <span data-ttu-id="a575e-134">Wenn eine Dateiassozierung erstellt oder geändert wird, benachrichtigen Sie das System, dass eine Änderung vorgenommen wurde, indem Sie [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)aufrufen und das SHCNE \_ ASSOCCHANGED-Ereignis angeben.</span><span class="sxs-lookup"><span data-stu-id="a575e-134">Whenever a file association is created or changed, notify the system that a change has been made by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the SHCNE\_ASSOCCHANGED event.</span></span> <span data-ttu-id="a575e-135">Wenn dies nicht erfolgt, erkennt die Shell möglicherweise keine Änderungen, die vorgenommen wurden, bevor das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a575e-135">If this is not done, the Shell might not recognize any changes made until the system restarts.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="a575e-136">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a575e-136">Additional Resources</span></span>

-   [<span data-ttu-id="a575e-137">Einführung in Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a575e-137">Introduction to File Associations</span></span>](fa-intro.md)
-   [<span data-ttu-id="a575e-138">Registrieren eines Internetbrowsers oder E-Mail-Clients mit dem Windows-Startmenü</span><span class="sxs-lookup"><span data-stu-id="a575e-138">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
-   <span data-ttu-id="a575e-139">[Registrieren einer Anwendung für ein URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a575e-139">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="a575e-140">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a575e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a575e-141">Bewährte Methoden für Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a575e-141">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="a575e-142">Richtlinien für die Verwaltung von Standardanwendungen in Windows Vista und höher</span><span class="sxs-lookup"><span data-stu-id="a575e-142">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="a575e-143">Standardprogramme</span><span class="sxs-lookup"><span data-stu-id="a575e-143">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="a575e-144">Festlegen von Programmzugriff und Computerstandard (SPAD)</span><span class="sxs-lookup"><span data-stu-id="a575e-144">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
