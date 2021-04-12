---
title: Überlegungen zu Projekten
description: Überlegungen zu Projekten
ms.assetid: aebe2886-0af0-443a-a5be-651f11936639
keywords:
- Windows Media-Format-SDK, Projekt Überlegungen
- Advanced Systems Format (ASF), Projekt Überlegungen
- ASF (Advanced Systems Format), Projekt Überlegungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1682e8008569c9b230b2c2f53f394326669d022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207313"
---
# <a name="project-considerations"></a><span data-ttu-id="ac4a5-106">Überlegungen zu Projekten</span><span class="sxs-lookup"><span data-stu-id="ac4a5-106">Project Considerations</span></span>

<span data-ttu-id="ac4a5-107">Sie müssen sicherstellen, dass der Endbenutzer Anwendungen, die Sie mit dem Windows Media Format SDK erstellen, ordnungsgemäß ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-107">You must ensure that the end user can properly run applications that you create with the Windows Media Format SDK.</span></span> <span data-ttu-id="ac4a5-108">In diesem Abschnitt werden zwei Aspekte beschrieben, die Sie beim Verteilen von Anwendungen, Dateinamen Erweiterungen und Software Weiterungen beachten müssen.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-108">This section describes two things you must consider when distributing applications, file name extensions and software redistribution.</span></span>

<span data-ttu-id="ac4a5-109">Sie müssen die richtigen Dateinamen Erweiterungen für alle Dateien verwenden, die mit Ihren Anwendungen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-109">You must use the correct file name extensions for any files created with your applications.</span></span> <span data-ttu-id="ac4a5-110">Durch die Verwendung der richtigen Dateinamen Erweiterungen wird Endbenutzern das Erkennen von ASF-Dateien erleichtert, und es werden Verwirrung beim Decodieren von Dateien verhindert.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-110">Using proper file name extensions makes it easier for end users to recognize ASF files and prevents confusion when decoding files.</span></span>

<span data-ttu-id="ac4a5-111">Sie müssen alle verteilbaren Komponenten bereitstellen, die zum Ausführen der Anwendungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-111">You must provide any redistributables that are required to run your applications.</span></span> <span data-ttu-id="ac4a5-112">Ohne die korrekten verteilbaren Komponenten können Benutzer ihre Anwendungen nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-112">Without the correct redistributables, users will not be able to use your applications.</span></span>

<span data-ttu-id="ac4a5-113">In den folgenden Abschnitten werden Dateinamen Erweiterungen und die Software Verteilung ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-113">The following sections describe file name extensions and software redistribution in detail.</span></span>



| <span data-ttu-id="ac4a5-114">`Section`</span><span class="sxs-lookup"><span data-stu-id="ac4a5-114">Section</span></span>                                                                      | <span data-ttu-id="ac4a5-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac4a5-115">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac4a5-116">Richtlinien für die Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="ac4a5-116">File Name Extension Guidelines</span></span>](file-name-extension-guidelines.md)         | <span data-ttu-id="ac4a5-117">Enthält Informationen über die Dateinamen Erweiterungen, die Sie für die von Ihrem Programm erstellten ASF-Dateien verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-117">Provides information about the file name extensions you should use for ASF files that your program creates.</span></span>     |
| [<span data-ttu-id="ac4a5-118">Software Verteilung</span><span class="sxs-lookup"><span data-stu-id="ac4a5-118">Software Redistribution</span></span>](software-redistribution.md)                       | <span data-ttu-id="ac4a5-119">Beschreibt die verteilbaren Dateien für das Windows Media-Format-SDK und wie diese in Ihre Anwendungen aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-119">Describes the redistributables for the Windows Media Format SDK and how to include them with your applications.</span></span> |
| [<span data-ttu-id="ac4a5-120">Anwendungs Abhängigkeit wird registriert</span><span class="sxs-lookup"><span data-stu-id="ac4a5-120">Registering Application Dependency</span></span>](registering-application-dependency.md) | <span data-ttu-id="ac4a5-121">Beschreibt, wie Sie die Anwendung als abhängig von der SDK-Laufzeit des Windows Media-Formats registrieren.</span><span class="sxs-lookup"><span data-stu-id="ac4a5-121">Describes how to register your application as being dependent on the Windows Media Format SDK runtime.</span></span>          |



 

 

 




