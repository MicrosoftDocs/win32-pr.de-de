---
description: Dateizuordnungen definieren, wie die Shell einen Dateityp im System behandelt.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Funktionsweise von Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215961"
---
# <a name="how-file-associations-work"></a><span data-ttu-id="a63d2-103">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a63d2-103">How File Associations Work</span></span>

<span data-ttu-id="a63d2-104">Dateizuordnungen definieren, wie die Shell einen [Dateityp](fa-file-types.md) im System behandelt.</span><span class="sxs-lookup"><span data-stu-id="a63d2-104">File associations define how the Shell treats a [file type](fa-file-types.md) on the system.</span></span>

<span data-ttu-id="a63d2-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="a63d2-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a63d2-106">Informationen zu Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a63d2-106">About File Associations</span></span>](#about-file-associations)
-   [<span data-ttu-id="a63d2-107">Beim implementieren oder Ändern von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a63d2-107">When You Should Implement or Modify File Associations</span></span>](#when-you-should-implement-or-modify-file-associations)
-   [<span data-ttu-id="a63d2-108">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a63d2-108">How File Associations Work</span></span>](#how-file-associations-work)
-   [<span data-ttu-id="a63d2-109">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a63d2-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="a63d2-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a63d2-110">Related topics</span></span>](#related-topics)

## <a name="about-file-associations"></a><span data-ttu-id="a63d2-111">Informationen zu Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a63d2-111">About File Associations</span></span>

<span data-ttu-id="a63d2-112">Dateizuordnungen steuern die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="a63d2-112">File associations control the following functionality:</span></span>

-   <span data-ttu-id="a63d2-113">Welche Anwendung gestartet wird, wenn ein Benutzer auf eine Datei doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="a63d2-113">Which application launches when a user double-clicks a file.</span></span>
-   <span data-ttu-id="a63d2-114">Welches Symbol standardmäßig für eine Datei angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a63d2-114">Which icon appears for a file by default.</span></span>
-   <span data-ttu-id="a63d2-115">Gibt an, wie der Dateityp im Windows-Explorer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a63d2-115">How the file type appears when viewed in Windows Explorer.</span></span>
-   <span data-ttu-id="a63d2-116">Welche Befehle im Kontextmenü einer Datei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a63d2-116">Which commands appear in a file's shortcut menu.</span></span>
-   <span data-ttu-id="a63d2-117">Andere Funktionen der Benutzeroberfläche, z. b. Quick Infos, Kachel Informationen und der Detailbereich.</span><span class="sxs-lookup"><span data-stu-id="a63d2-117">Other UI features, such as tooltips, tile info, and the details pane.</span></span>

<span data-ttu-id="a63d2-118">Anwendungsentwickler können Dateizuordnungen verwenden, um zu steuern, wie die Shell benutzerdefinierte Dateitypen behandelt, oder um einer Anwendung vorhandene Dateitypen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a63d2-118">Application developers can use file associations to control how the Shell treats custom file types, or to associate an application with existing file types.</span></span> <span data-ttu-id="a63d2-119">Wenn beispielsweise eine Anwendung installiert ist, kann die Anwendung überprüfen, ob vorhandene Dateizuordnungen vorhanden sind, und diese Dateizuordnungen erstellen oder überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a63d2-119">For example, when an application is installed, the application can check for the presence of existing file associations, and either create or override those file associations.</span></span>

<span data-ttu-id="a63d2-120">Benutzer können einige Aspekte von Dateizuordnungen steuern, um anzupassen, wie die Shell einen Dateityp behandelt, indem Sie entweder die Option mit der Benutzeroberfläche **Öffnen** und die Registrierung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a63d2-120">Users can control some aspects of file associations to customize how the Shell treats a file type either by using the **Open With** UI, or editing the registry.</span></span>

<span data-ttu-id="a63d2-121">Im Windows-Explorer-Fenster, das im Screenshot unten angezeigt wird, zeigt die Shell basierend auf dem Symbol, das dem Dateityp zugeordnet ist, unterschiedliche Symbole für jede Datei an.</span><span class="sxs-lookup"><span data-stu-id="a63d2-121">In the Windows Explorer window shown in the screen shot below, the Shell displays different icons for each file, based on the icon associated with the file type.</span></span> <span data-ttu-id="a63d2-122">Wenn der Benutzer auf das **Bitmapbild der Datei Stichprobe** doppelklickt, wird Paint gestartet und zum Öffnen der Datei verwendet, da Paint auf diesem System mit BMP-Dateien verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a63d2-122">If the user double-clicks the file **Sample Bitmap Image**, the Shell launches Paint and uses it to open the file because on this system, Paint is associated with .bmp files.</span></span> <span data-ttu-id="a63d2-123">Personen können diese Aktionen mithilfe von Dateizuordnungen steuern.</span><span class="sxs-lookup"><span data-stu-id="a63d2-123">People can control these actions using file associations.</span></span>

![Darstellung der Funktionsweise von Dateizuordnungen in der Praxis](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a><span data-ttu-id="a63d2-125">Beim implementieren oder Ändern von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a63d2-125">When You Should Implement or Modify File Associations</span></span>

<span data-ttu-id="a63d2-126">Anwendungen können Dateien für verschiedene Zwecke verwenden: einige Dateien werden ausschließlich von der Anwendung verwendet, und es wird in der Regel nicht von Benutzern darauf zugegriffen, während andere Dateien vom Benutzer erstellt und häufig geöffnet, gesucht und in der Shell angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a63d2-126">Applications can use files for various purposes: some files are used exclusively by the application, and are not typically accessed by users, while other files are created by the user and are often opened, searched for, and viewed from the Shell.</span></span>

<span data-ttu-id="a63d2-127">Wenn Ihr benutzerdefinierter Dateityp ausschließlich von der Anwendung verwendet wird, sollten Sie Dateizuordnungen für ihn implementieren.</span><span class="sxs-lookup"><span data-stu-id="a63d2-127">Unless your custom file type is used exclusively by the application, you should implement file associations for it.</span></span> <span data-ttu-id="a63d2-128">Als allgemeine Regel implementieren Sie Dateizuordnungen für Ihren benutzerdefinierten Dateityp, wenn Sie davon ausgehen, dass der Benutzer in irgendeiner Weise direkt mit diesen Dateien interagieren soll.</span><span class="sxs-lookup"><span data-stu-id="a63d2-128">As a general rule, implement file associations for your custom file type if you expect the user to interact directly with these files in any way.</span></span> <span data-ttu-id="a63d2-129">Dazu gehört die Verwendung der Shell zum Durchsuchen und Öffnen der Dateien, zum Durchsuchen des Inhalts oder der Eigenschaften der Dateien und zum Anzeigen der Vorschau der Dateien.</span><span class="sxs-lookup"><span data-stu-id="a63d2-129">That includes using the Shell to browse and open the files, searching the content or properties of the files, and previewing the files.</span></span>

<span data-ttu-id="a63d2-130">Wenn die Anwendung einen vorhandenen Dateityp verarbeitet, ändern Sie die Datei Zuordnung nur, wenn Sie die Art und Weise ändern möchten, wie die Shell alle Dateien dieses Typs verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a63d2-130">If your application is handling an existing file type, do not modify the file association unless you want to modify the way the Shell handles all files of this type.</span></span>

## <a name="how-file-associations-work"></a><span data-ttu-id="a63d2-131">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="a63d2-131">How File Associations Work</span></span>

<span data-ttu-id="a63d2-132">Dateien werden in der Shell als shellelemente verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a63d2-132">Files are exposed in the Shell as Shell items.</span></span> <span data-ttu-id="a63d2-133">Um Dateizuordnungen zu steuern, können Anwendungsentwickler eine Zuordnung zwischen dem Dateityp und den Handlern (COM-Objekte, die Funktionalität für die shellelemente des Dateityps bereitstellen) registrieren.</span><span class="sxs-lookup"><span data-stu-id="a63d2-133">To control file associations, application developers can register a mapping between the file type and the handlers (COM objects that provide functionality for the file type's Shell items).</span></span> <span data-ttu-id="a63d2-134">Wenn die Shell die Dateizuordnungen eines Dateityps Abfragen muss, erstellt Sie ein Array von Registrierungs Schlüsseln, die die Zuordnungen für den Dateityp enthalten, und überprüft diese Schlüssel auf die zu verwendenden Dateizuordnungen.</span><span class="sxs-lookup"><span data-stu-id="a63d2-134">When the Shell needs to query for the file associations of a file type, it creates an array of registry keys containing the associations for the file type, and checks these keys for the appropriate file associations to use.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a63d2-135">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a63d2-135">Additional Resources</span></span>

-   <span data-ttu-id="a63d2-136">Konzeptionelle Hintergrundinformationen zu Dateizuordnungen finden Sie unter [Übersicht über Verben und Dateizuordnungen](fa-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="a63d2-136">For conceptual background on file associations, see [Overview of Verbs and File Associations](fa-verbs.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a63d2-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a63d2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a63d2-138">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="a63d2-138">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="a63d2-139">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="a63d2-139">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="a63d2-140">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="a63d2-140">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="a63d2-141">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="a63d2-141">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="a63d2-142">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="a63d2-142">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="a63d2-143">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a63d2-143">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="a63d2-144">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="a63d2-144">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="a63d2-145">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="a63d2-145">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



