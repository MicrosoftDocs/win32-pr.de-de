---
description: In diesem Thema wird beschrieben, was Bibliotheken sind und wie Sie von Benutzern und Entwicklern profitieren können.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Informationen zu Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557755"
---
# <a name="about-libraries"></a><span data-ttu-id="209cc-103">Informationen zu Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="209cc-103">About Libraries</span></span>

<span data-ttu-id="209cc-104">In diesem Thema wird beschrieben, was Bibliotheken sind und wie Sie von Benutzern und Entwicklern profitieren können.</span><span class="sxs-lookup"><span data-stu-id="209cc-104">This topic describes what libraries are and how they can benefit users and developers.</span></span>

<span data-ttu-id="209cc-105">Bibliotheken sind benutzerdefinierte Auflistungen von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="209cc-105">Libraries are user-defined collections of folders.</span></span> <span data-ttu-id="209cc-106">In einer Bibliothek wird der physische Speicherort jedes Ordners nachverfolgt, wodurch der Benutzer und die Software dieser Aufgabe entlastet werden.</span><span class="sxs-lookup"><span data-stu-id="209cc-106">A library keeps track of each folder's physical storage location, which relieves the user and the software of that task.</span></span> <span data-ttu-id="209cc-107">Benutzer können verwandte Ordner in einer Bibliothek gruppieren, auch wenn diese Ordner auf unterschiedlichen Festplatten oder auf unterschiedlichen Computern gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="209cc-107">Users can group related folders together in a library even if those folders are stored on different hard drives or different computers.</span></span>

<span data-ttu-id="209cc-108">In einer Bibliothek werden die Ordner und Dateien für den Benutzer als einzelne Sammlung angezeigt. mithilfe der shellbibliotheks-API kann der Inhalt der Bibliothek auch an einem einzigen Speicherort zu einem Programm stehen.</span><span class="sxs-lookup"><span data-stu-id="209cc-108">In a library, the folders and files appear to the user as a single collection and, using the Shell Library API, the library's contents can also appear to be in a single location to a program.</span></span>

<span data-ttu-id="209cc-109">In einer Bibliothek können die Inhalte, wie z. b. Dokumente, Fotos, Videos oder Musik eines Benutzers, sortiert und angezeigt werden, wenn der Benutzer das gewünschte Dateisystem benötigt.</span><span class="sxs-lookup"><span data-stu-id="209cc-109">In a library, the contents, such as a user's documents, photos, videos, or music, can be sorted and displayed as the user wants and not simply as how the file system requires.</span></span> <span data-ttu-id="209cc-110">Beispielsweise können Benutzer den Inhalt einer Bibliothek mithilfe der Eigenschaften der Elemente in der Bibliothek organisieren, sodass Verwandte Elemente auch dann zusammen sortiert werden, wenn Sie in unterschiedlichen Ordnern gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="209cc-110">For example, users can organize the contents of a library using the properties of the items in the library so that related items will sort together even if they are stored in different folders.</span></span>

![Screenshot der Benutzeroberfläche "Bibliotheken"](images/libraries-whatare.png)

<span data-ttu-id="209cc-112">In diesem Thema:</span><span class="sxs-lookup"><span data-stu-id="209cc-112">In this topic:</span></span>

-   [<span data-ttu-id="209cc-113">Bibliotheks Vorteile</span><span class="sxs-lookup"><span data-stu-id="209cc-113">Library Benefits</span></span>](#library-benefits)
    -   [<span data-ttu-id="209cc-114">Benutzer Vorteile</span><span class="sxs-lookup"><span data-stu-id="209cc-114">User Benefits</span></span>](#user-benefits)
    -   [<span data-ttu-id="209cc-115">Vorteile für Entwickler</span><span class="sxs-lookup"><span data-stu-id="209cc-115">Developer Benefits</span></span>](#developer-benefits)
-   [<span data-ttu-id="209cc-116">Verwalten von Ordnern in Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="209cc-116">Managing Folders in Libraries</span></span>](#managing-folders-in-libraries)
-   [<span data-ttu-id="209cc-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="209cc-117">Related topics</span></span>](#related-topics)

## <a name="library-benefits"></a><span data-ttu-id="209cc-118">Bibliotheks Vorteile</span><span class="sxs-lookup"><span data-stu-id="209cc-118">Library Benefits</span></span>

<span data-ttu-id="209cc-119">In diesem Abschnitt werden einige der Vorteile von Bibliotheken aus der Perspektive des Endbenutzers und der Perspektive des Programm Entwicklers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="209cc-119">This section describes some of the benefits of libraries from the end-user's perspective and the program developer's perspective.</span></span>

### <a name="user-benefits"></a><span data-ttu-id="209cc-120">Benutzer Vorteile</span><span class="sxs-lookup"><span data-stu-id="209cc-120">User Benefits</span></span>

<span data-ttu-id="209cc-121">Das Hinzufügen von Bibliotheks Unterstützung zu Ihrem Programm bietet dem Benutzer die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="209cc-121">Adding library support to your program provides the following benefits to the user:</span></span>

-   <span data-ttu-id="209cc-122">**Bibliotheken stellen eine konsistente Benutzeroberfläche in Windows 7 bereit.**</span><span class="sxs-lookup"><span data-stu-id="209cc-122">**Libraries provide a consistent user interface in Windows 7**</span></span>

    <span data-ttu-id="209cc-123">Die Dialogfelder allgemeine Dateien unterstützen Bibliotheken und bieten dieselbe Benutzer Darstellung wie Windows-Explorer in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="209cc-123">The common file dialog boxes support libraries and provide the same user experience as the Windows Explorer in Windows 7.</span></span> <span data-ttu-id="209cc-124">Unterstützende Bibliotheken in Ihrem Programm helfen bei der Verwendung des Programms in Windows 7 dabei, eine nahtlose Interaktion für den Benutzer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="209cc-124">Supporting libraries in your program will help provide a more seamless interaction for the user when using your program in Windows 7.</span></span>

-   <span data-ttu-id="209cc-125">**Benutzer entscheiden, wo Inhalte gespeichert werden sollen.**</span><span class="sxs-lookup"><span data-stu-id="209cc-125">**Users decide where to store content**</span></span>

    <span data-ttu-id="209cc-126">Bibliotheken ermöglichen es Benutzern, den Speicherort Ihrer Inhalte zu steuern.</span><span class="sxs-lookup"><span data-stu-id="209cc-126">Libraries make it possible for users to control where their content is stored.</span></span> <span data-ttu-id="209cc-127">Gleichzeitig bieten Bibliotheken angemessene Standardeinstellungen für Benutzer, die diese Detailebene nicht auf Ihrem Computer verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="209cc-127">At the same time, libraries provide reasonable defaults for users who do not want to manage that level of detail in their computer.</span></span> <span data-ttu-id="209cc-128">Benutzer entscheiden, wie viel oder wie wenig Sie steuern möchten, wo und wie Ihre Inhalte gespeichert werden und wie die Bibliothek in jedem Fall ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="209cc-128">Users decide how much, or how little, control they want to exercise over where and how their content is stored and the library works fine either way.</span></span>

### <a name="developer-benefits"></a><span data-ttu-id="209cc-129">Vorteile für Entwickler</span><span class="sxs-lookup"><span data-stu-id="209cc-129">Developer Benefits</span></span>

<span data-ttu-id="209cc-130">Sie können Bibliotheken in Ihrem Programm verwenden, um eine flexiblere und bequeme Benutzeroberfläche bereitzustellen, ohne viel komplexen Programmcode hinzufügen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="209cc-130">You can use libraries in your program to provide a more flexible and convenient user interface without having to add a lot of complex program code.</span></span> <span data-ttu-id="209cc-131">Zu den Vorteilen beim Hinzufügen von Bibliotheks Unterstützung gehören:</span><span class="sxs-lookup"><span data-stu-id="209cc-131">Some of the advantages of adding library support include:</span></span>

-   <span data-ttu-id="209cc-132">**Bibliotheken unterstützen Bibliothek-und Dateisystem Zugriff**</span><span class="sxs-lookup"><span data-stu-id="209cc-132">**Libraries support library and file-system access**</span></span>

    <span data-ttu-id="209cc-133">Mithilfe der [**shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)können Programme für den Benutzer Bibliotheks Unterstützung bereitstellen und gleichzeitig die Komplexität des Datei-und Ordner Verwaltungs Codes verringern.</span><span class="sxs-lookup"><span data-stu-id="209cc-133">Using the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), programs can provide library support for the user while reducing the complexity of their file and folder management code.</span></span> <span data-ttu-id="209cc-134">Wenn das Programm die Dateisystem-API bereits verwendet, können Sie den vorhandenen Code beliebig beibehalten und dem Benutzer dennoch Bibliotheks Unterstützung bereitstellen, indem Sie die erforderlichen Dateisystem Informationen aus der **shellbibliotheks-API** erhalten.</span><span class="sxs-lookup"><span data-stu-id="209cc-134">If your program already uses the file-system API, you can preserve as much of that existing code as you want and still provide library support to the user by getting the necessary file-system information from the **Shell Library API**.</span></span>

-   <span data-ttu-id="209cc-135">**Einfachere Änderungs Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="209cc-135">**Simpler change notification**</span></span>

    <span data-ttu-id="209cc-136">Sowohl das Dateisystem als auch die Shell-API können das Programm Benachrichtigen, wenn sich der Inhalt eines überwachten Ordners oder einer Bibliothek ändert.</span><span class="sxs-lookup"><span data-stu-id="209cc-136">Both the file-system and the Shell API can notify your program when the contents of a monitored folder or library change.</span></span> <span data-ttu-id="209cc-137">Mithilfe der Shell-API können Sie jedoch alle Ordner in der Bibliothek mit einer einzelnen Benachrichtigung überwachen, auch wenn der Ordner in der Bibliothek möglicherweise auf unterschiedlichen Laufwerken oder sogar auf unterschiedlichen Computern gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="209cc-137">Using the Shell API, however, you can monitor all the folders in the library with a single notification, even though the folder in the library may be stored on different drives or even different computers.</span></span>

-   <span data-ttu-id="209cc-138">**Bibliotheken verwenden von Dateieigenschaften**</span><span class="sxs-lookup"><span data-stu-id="209cc-138">**Libraries use file properties**</span></span>

    <span data-ttu-id="209cc-139">Programme können die Dateieigenschaften verwenden, um zu steuern, welche Dateien während der Öffnungs-und Speichervorgänge angezeigt werden, die die allgemeinen Datei Dialogfelder verwenden.</span><span class="sxs-lookup"><span data-stu-id="209cc-139">Programs can use the file properties to control which files are displayed during open and save operations that use the common file dialog boxes.</span></span> <span data-ttu-id="209cc-140">Programme können auch über die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen auf Dateieigenschaften zugreifen.</span><span class="sxs-lookup"><span data-stu-id="209cc-140">Programs can also have access to file properties by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces.</span></span> <span data-ttu-id="209cc-141">Die Dialogfelder für die gemeinsame Datei können auch so konfiguriert werden, dass Benutzer die dem Inhalt zugeordneten Eigenschaften aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="209cc-141">The common file dialog boxes can also be configured allow users to update the properties that are associated with their content.</span></span>

-   <span data-ttu-id="209cc-142">**Programme können dedizierte Bibliotheken erstellen**</span><span class="sxs-lookup"><span data-stu-id="209cc-142">**Programs can create dedicated libraries**</span></span>

    <span data-ttu-id="209cc-143">Eine neue Bibliothek kann erstellt werden, wenn vorhandene Benutzer Bibliotheken die Programmanforderungen nicht erfüllen – beispielsweise, wenn ein Programm einen neuen Typ von Benutzer Inhalt erstellt.</span><span class="sxs-lookup"><span data-stu-id="209cc-143">A new library can be created when an existing user libraries does not meet the program's needs—for example, if a program creates a new type of user content.</span></span> <span data-ttu-id="209cc-144">Die neue Bibliothek kann mit einem eindeutigen Symbol konfiguriert werden, das ihren Inhalt darstellt und die Identifizierung der Bibliothek im Windows-Explorer erleichtert.</span><span class="sxs-lookup"><span data-stu-id="209cc-144">The new library can be configured with a unique icon that represents their content and makes the library easy to identify in the Windows Explorer.</span></span>

## <a name="managing-folders-in-libraries"></a><span data-ttu-id="209cc-145">Verwalten von Ordnern in Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="209cc-145">Managing Folders in Libraries</span></span>

<span data-ttu-id="209cc-146">Benutzer können Ihre Bibliotheken organisieren, indem Sie Ordner in der Bibliothek hinzufügen, verschieben oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="209cc-146">Users can organize their libraries by adding, moving, or removing folders in the library.</span></span> <span data-ttu-id="209cc-147">Nicht alle Ordner unterstützen jedoch die gesamte Funktionalität, die eine Bibliothek bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="209cc-147">Not all folders, however, support all the functionality that a library can provide.</span></span> <span data-ttu-id="209cc-148">Viele Bibliotheks Features erfordern einen schnellen Zugriff auf die verschiedenen Eigenschaften des Ordners und dessen Inhalte, die nur über Windows Search verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="209cc-148">Many library features require quick access to the different properties of the folder and its contents that are only available through Windows Search.</span></span> <span data-ttu-id="209cc-149">Um vollständige Bibliotheksfunktionen bereitzustellen, muss ein Ordner von Windows Search indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="209cc-149">To provide full library functionality, a folder must be able to be indexed by Windows Search.</span></span>

<span data-ttu-id="209cc-150">In einer Bibliothek kann ein Benutzer keine Ordner hinzufügen, die keine vollständige Bibliotheks Funktionalität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="209cc-150">A library does not allow a user to add folders that do not provide full library functionality.</span></span> <span data-ttu-id="209cc-151">Die [**shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) kann jedoch solche Ordner hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="209cc-151">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can, however, add such folders.</span></span> <span data-ttu-id="209cc-152">Wenn eine Bibliothek einen Ordner enthält, der die Funktionalität der vollständigen Bibliothek nicht unterstützt, wird die Bibliothek in einem abgesicherten Modus betrieben und bietet eine eingeschränkte Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="209cc-152">If a library contains a folder that does not support full library functionality, the library will operate in a safe mode and provide a limited functionality.</span></span> <span data-ttu-id="209cc-153">In der folgenden Tabelle werden die Ordner beschrieben, die vollständige Bibliotheksfunktionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="209cc-153">The following table describes the folders that support full library functionality and those that do not.</span></span>



| <span data-ttu-id="209cc-154">Ordner Typen, die vollständige Bibliotheksfunktionen unterstützen</span><span class="sxs-lookup"><span data-stu-id="209cc-154">Folder types that support full library functionality</span></span>                                                               | <span data-ttu-id="209cc-155">Ordner Typen, die keine vollständige Bibliotheks Funktionalität unterstützen</span><span class="sxs-lookup"><span data-stu-id="209cc-155">Folder types that do not support full library functionality</span></span>                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="209cc-156">Feste und externe NTFS-und FAT32-Festplatten.</span><span class="sxs-lookup"><span data-stu-id="209cc-156">Fixed and external NTFS and FAT32 hard drives.</span></span>                                                                     | <span data-ttu-id="209cc-157">Wechsel Datenträger, z. b. USB-Flash Laufwerke oder sichere digitale (SD) Speicherkarten.</span><span class="sxs-lookup"><span data-stu-id="209cc-157">Removable drives such as USB flash drives or Secure Digital (SD) memory cards.</span></span>               |
| <span data-ttu-id="209cc-158">Dateifreigaben, die von Windows Search indiziert werden, z. b. Abteilungs Server, Windows 7 oder Windows Vista Home PCs.</span><span class="sxs-lookup"><span data-stu-id="209cc-158">File shares that are indexed by Windows Search such as departmental servers, Windows 7, or Windows Vista home PCs.</span></span> | <span data-ttu-id="209cc-159">Wechselmedien, z. b. CD-ROM oder DVD-Medien.</span><span class="sxs-lookup"><span data-stu-id="209cc-159">Removable media such as CD-ROM or DVD media.</span></span>                                                 |
| <span data-ttu-id="209cc-160">Offline verfügbare Dateifreigaben, z. b. ein umgeleiteter Ordner " **Eigene Dokumente** " oder ein Client-Side Cache.</span><span class="sxs-lookup"><span data-stu-id="209cc-160">File shares that are available offline such as a redirected **My Documents** folder or a Client-Side Cache.</span></span>        | <span data-ttu-id="209cc-161">Netzwerkfreigaben, die weder Offline noch Remote indiziert sind, z. b. NAS-Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="209cc-161">Network shares that are neither available offline nor remotely indexed such as NAS drives.</span></span>   |
|                                                                                                                    | <span data-ttu-id="209cc-162">Andere Datenquellen, z. b. Microsoft SharePoint, Microsoft Exchange und Microsoft onedrive.</span><span class="sxs-lookup"><span data-stu-id="209cc-162">Other data sources such as Microsoft SharePoint, Microsoft Exchange, and Microsoft OneDrive.</span></span> |



 

<span data-ttu-id="209cc-163">In der folgenden Abbildung wird die eingeschränkte Anzeige der Bibliotheksinhalte im abgesicherten Modus gezeigt.</span><span class="sxs-lookup"><span data-stu-id="209cc-163">The following image shows the limited display of library contents while in safe mode.</span></span>

![Dialogfeld öffnen, wenn sich Bibliotheken im abgesicherten Modus befinden](images/libraries-supportedfolders.png)

## <a name="related-topics"></a><span data-ttu-id="209cc-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="209cc-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="209cc-166">Informationen zu Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="209cc-166">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="209cc-167">**Ishelllibrary**</span><span class="sxs-lookup"><span data-stu-id="209cc-167">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="209cc-168">Shelllinks</span><span class="sxs-lookup"><span data-stu-id="209cc-168">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="209cc-169">Bekannte Ordner</span><span class="sxs-lookup"><span data-stu-id="209cc-169">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="209cc-170">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="209cc-170">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
