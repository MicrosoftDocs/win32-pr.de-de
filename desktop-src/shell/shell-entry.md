---
description: Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die für die Ausführung von Anwendungen und die Verwaltung des Betriebssystems erforderlich sind.
title: Windows-Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979904"
---
# <a name="windows-shell"></a><span data-ttu-id="ff0f0-103">Windows-Shell</span><span class="sxs-lookup"><span data-stu-id="ff0f0-103">Windows Shell</span></span>

<span data-ttu-id="ff0f0-104">Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die für die Ausführung von Anwendungen und die Verwaltung des Betriebssystems erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-104">The Windows UI provides users with access to a wide variety of objects necessary for running applications and managing the operating system.</span></span> <span data-ttu-id="ff0f0-105">Die häufigsten und vertrauten Objekte sind die Ordner und Dateien, die sich auf Computer Laufwerken befinden.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="ff0f0-106">Es gibt auch eine Reihe von virtuellen Objekten, die es dem Benutzer ermöglichen, Aufgaben auszuführen, z. b. das Senden von Dateien an Remote Drucker oder den Zugriff auf den Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-106">There are also a number of virtual objects that allow the user to perform tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="ff0f0-107">Die Shell organisiert diese Objekte in einem hierarchischen Namespace und bietet Benutzern und Anwendungen eine konsistente und effiziente Möglichkeit, auf Objekte zuzugreifen und diese zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-107">The Shell organizes these objects into a hierarchical namespace and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="shell-development-scenarios"></a><span data-ttu-id="ff0f0-108">Shellentwicklungs Szenarien</span><span class="sxs-lookup"><span data-stu-id="ff0f0-108">Shell Development Scenarios</span></span>

<span data-ttu-id="ff0f0-109">Die folgenden Entwicklungsszenarien beziehen sich auf die Anwendungsentwicklung:</span><span class="sxs-lookup"><span data-stu-id="ff0f0-109">The following development scenarios relate to application development:</span></span>

-   <span data-ttu-id="ff0f0-110">Erweitern der Shell, die das Erstellen einer Datenquelle (im Gegensatz zum Verarbeiten des shelldatenmodells) umfasst</span><span class="sxs-lookup"><span data-stu-id="ff0f0-110">Extending the Shell, which consists of creating a data source (versus consuming the Shell data model)</span></span>
-   <span data-ttu-id="ff0f0-111">Implementieren einer Teilmenge der Shell-Datenquellen Tasks</span><span class="sxs-lookup"><span data-stu-id="ff0f0-111">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="ff0f0-112">Unterstützende Bibliotheken und Element Ansichten in Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="ff0f0-112">Supporting libraries and item views in Windows Explorer</span></span>
-   <span data-ttu-id="ff0f0-113">Verwenden des allgemeinen Datei Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="ff0f0-113">Using the common file dialog</span></span>
-   <span data-ttu-id="ff0f0-114">Implementieren von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-114">Implementing Control Panel items</span></span>
-   <span data-ttu-id="ff0f0-115">Verwalten von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-115">Managing notifications</span></span>

<span data-ttu-id="ff0f0-116">Die folgenden Entwicklungsszenarien beziehen sich auf den Besitz des Datei Formats:</span><span class="sxs-lookup"><span data-stu-id="ff0f0-116">The following development scenarios relate to file format ownership:</span></span>

-   <span data-ttu-id="ff0f0-117">Implementieren einer Teilmenge der Shell-Datenquellen Tasks</span><span class="sxs-lookup"><span data-stu-id="ff0f0-117">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="ff0f0-118">Implementieren eines beliebigen Handlers</span><span class="sxs-lookup"><span data-stu-id="ff0f0-118">Implementing any handler</span></span>
-   <span data-ttu-id="ff0f0-119">Unterstützung der Desktop Suche</span><span class="sxs-lookup"><span data-stu-id="ff0f0-119">Supporting desktop search</span></span>

<span data-ttu-id="ff0f0-120">Die folgenden Entwicklungsszenarien beziehen sich auf den Datenspeicher Besitz:</span><span class="sxs-lookup"><span data-stu-id="ff0f0-120">The following development scenarios relate to data storage ownership:</span></span>

-   <span data-ttu-id="ff0f0-121">Unterstützung der Desktop Suche und OpenSearch</span><span class="sxs-lookup"><span data-stu-id="ff0f0-121">Supporting desktop search and OpenSearch</span></span>
-   <span data-ttu-id="ff0f0-122">Implementieren einer Teilmenge der Shell-Datenquellen Tasks (virtuelle Ordner)</span><span class="sxs-lookup"><span data-stu-id="ff0f0-122">Implementing a subset of the Shell data source tasks (virtual folders)</span></span>
-   <span data-ttu-id="ff0f0-123">Unterstützende Bibliotheken in Windows-Explorer</span><span class="sxs-lookup"><span data-stu-id="ff0f0-123">Supporting libraries in Windows Explorer</span></span>

<span data-ttu-id="ff0f0-124">Das folgende Entwicklungsszenario bezieht sich auf die Geräte Unterstützung:</span><span class="sxs-lookup"><span data-stu-id="ff0f0-124">The following development scenario relates to device support:</span></span>

-   <span data-ttu-id="ff0f0-125">Automatisch ausführen und automatisch abspielen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-125">Auto run and auto play</span></span>

## <a name="windows-shell-sdk-documentation"></a><span data-ttu-id="ff0f0-126">Dokumentation zum Windows Shell SDK</span><span class="sxs-lookup"><span data-stu-id="ff0f0-126">Windows Shell SDK Documentation</span></span>

<span data-ttu-id="ff0f0-127">Diese Dokumentation ist in drei Hauptabschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="ff0f0-127">This documentation is broken into three major sections:</span></span>

-   <span data-ttu-id="ff0f0-128">Das [shellentwicklerhandbuch](intro.md) bietet konzeptionelle Informationen zur Funktionsweise der Shell und zur Verwendung der Shell-API in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-128">The [Shell Developer's Guide](intro.md) provides conceptual material about how the Shell works and how to use the Shell's API in your application.</span></span>
-   <span data-ttu-id="ff0f0-129">Der Abschnitt " [Shellverweis](shell-reference-bumper.md) " dokumentiert Programmier Elemente, die die verschiedenen Shell-APIs bilden.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-129">The [Shell Reference](shell-reference-bumper.md) section documents programming elements that make up the various Shell APIs.</span></span>
-   <span data-ttu-id="ff0f0-130">[Shellbeispiele](samples-entry.md) bieten Links zu verwandten Codebeispielen.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-130">[Shell Samples](samples-entry.md) provides links to related code samples.</span></span>

<span data-ttu-id="ff0f0-131">In der folgenden Tabelle finden Sie einen Überblick über den Abschnitt shellreferenz.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-131">The following table provides an outline of the Shell Reference section.</span></span> <span data-ttu-id="ff0f0-132">Sofern nicht anders angegeben, werden alle Programmier Elemente in nicht verwaltetem C++ dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-132">Unless otherwise noted, all programming elements are documented in unmanaged C++.</span></span>



| <span data-ttu-id="ff0f0-133">`Section`</span><span class="sxs-lookup"><span data-stu-id="ff0f0-133">Section</span></span>                                                               | <span data-ttu-id="ff0f0-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff0f0-134">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff0f0-135">Shellklassen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-135">Shell Classes</span></span>](classes.md)                                          | <span data-ttu-id="ff0f0-136">In diesem Abschnitt werden Windows-shellklassen auswählen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-136">This section describes select Windows Shell classes.</span></span>                                                                 |
| [<span data-ttu-id="ff0f0-137">Shellschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-137">Shell Interfaces</span></span>](interfaces.md)                                    | <span data-ttu-id="ff0f0-138">In diesem Abschnitt werden die Schnittstellen der Windows Shell-Component Object Model (com) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-138">This section describes the Windows Shell Component Object Model (COM) interfaces.</span></span>                                    |
| [<span data-ttu-id="ff0f0-139">Shellfunktionen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-139">Shell Functions</span></span>](functions.md)                                      | <span data-ttu-id="ff0f0-140">In diesem Abschnitt werden die Windows-Shellfunktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-140">This section describes the Windows Shell functions.</span></span>                                                                  |
| [<span data-ttu-id="ff0f0-141">Shellrückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-141">Shell Callback Functions</span></span>](callbacks.md)                             | <span data-ttu-id="ff0f0-142">In diesem Abschnitt werden die Vorlagen für Windows Shell-Rückruf Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-142">This section describes the Windows Shell callback functions templates.</span></span>                                               |
| [<span data-ttu-id="ff0f0-143">Shellkonstanten, Enumerationen und Flags</span><span class="sxs-lookup"><span data-stu-id="ff0f0-143">Shell Constants, Enumerations, and Flags</span></span>](consts-enums-flags.md)    | <span data-ttu-id="ff0f0-144">In diesem Abschnitt werden die in den Shell-APIs verwendeten Windows Shell-Konstanten, Enumerationen und Flags beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-144">This section describes the Windows Shell constants, enumerations, and flags used in the Shell APIs.</span></span>                  |
| [<span data-ttu-id="ff0f0-145">Shell Lightweight Utility-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-145">Shell Lightweight Utility Functions</span></span>](shlwapi.md)                    | <span data-ttu-id="ff0f0-146">In diesem Abschnitt werden die in Shlwapi.dll bereitgestellten Windows Shell Lightweight Utility-Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-146">This section describes the Windows Shell lightweight utility functions provided in Shlwapi.dll.</span></span>                      |
| [<span data-ttu-id="ff0f0-147">Shellmakros</span><span class="sxs-lookup"><span data-stu-id="ff0f0-147">Shell Macros</span></span>](macros.md)                                            | <span data-ttu-id="ff0f0-148">In diesem Abschnitt werden die Makros des Windows Shell-Hilfsprogramms beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-148">This section describes the Windows Shell utility macros.</span></span>                                                             |
| [<span data-ttu-id="ff0f0-149">Shellnachrichten und Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-149">Shell Messages and Notifications</span></span>](messages.md)                      | <span data-ttu-id="ff0f0-150">In diesem Abschnitt werden die Nachrichten und Benachrichtigungen beschrieben, die von Elementen der Windows-Shell gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-150">This section describes the messages and notifications sent by elements of the Windows Shell.</span></span>                         |
| [<span data-ttu-id="ff0f0-151">Shellobjekte für Skripterstellung und Microsoft-Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ff0f0-151">Shell Objects for Scripting and Microsoft Visual Basic</span></span>](objects.md) | <span data-ttu-id="ff0f0-152">In diesem Abschnitt werden die Windows-Objekte beschrieben, die von der Shell für die Verwendung in Skripts und Microsoft Visual Basic implementiert werden</span><span class="sxs-lookup"><span data-stu-id="ff0f0-152">This section describes the Windows objects implemented by the Shell for use in scripting and Microsoft Visual Basic.</span></span> |
| [<span data-ttu-id="ff0f0-153">Shellobjekte für C++</span><span class="sxs-lookup"><span data-stu-id="ff0f0-153">Shell Objects for C++</span></span>](objects-cpp.md)                              | <span data-ttu-id="ff0f0-154">In diesem Abschnitt werden die von der Shell implementierten C++-Windows-Objekte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-154">This section describes the C++ Windows objects implemented by the Shell.</span></span>                                             |
| [<span data-ttu-id="ff0f0-155">Shellschemas</span><span class="sxs-lookup"><span data-stu-id="ff0f0-155">Shell Schemas</span></span>](schemas.md)                                          | <span data-ttu-id="ff0f0-156">In diesem Abschnitt werden die von der Windows-Shell verwendeten Bibliotheks-, Eigenschafts-und Übertragungs manifest-Schemas beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-156">This section describes library, property, and transfer manifest schemas used by the Windows Shell.</span></span>                   |
| [<span data-ttu-id="ff0f0-157">Shellstrukturen</span><span class="sxs-lookup"><span data-stu-id="ff0f0-157">Shell Structures</span></span>](structures.md)                                    | <span data-ttu-id="ff0f0-158">In diesem Abschnitt werden die in den Shell-APIs verwendeten Windows Shell-Strukturen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ff0f0-158">This section describes the Windows Shell structures used in the Shell APIs.</span></span>                                          |



 

 

 



