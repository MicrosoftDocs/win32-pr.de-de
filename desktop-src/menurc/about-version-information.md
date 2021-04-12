---
title: Informationen zu Versionsinformationen
description: In diesem Thema werden die Funktionen der Versionsinformationen erläutert.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- Ressourcen, Versionsinformationen
- Versionsinformationen
- Hinzufügen von Versionsinformationen
- Dateikonflikte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390212"
---
# <a name="about-version-information"></a><span data-ttu-id="97ba5-107">Informationen zu Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="97ba5-107">About Version Information</span></span>

<span data-ttu-id="97ba5-108">Sie können die Versions Informationsfunktionen verwenden, um zu bestimmen, wo eine Datei installiert werden soll, und um Konflikte mit den derzeit installierten Dateien zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="97ba5-108">You can use the version information functions to determine where a file should be installed and identify conflicts with currently installed files.</span></span> <span data-ttu-id="97ba5-109">Diese Funktionen ermöglichen es Ihnen, die folgenden Probleme zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="97ba5-109">These functions enable you to avoid the following problems:</span></span>

-   <span data-ttu-id="97ba5-110">Installieren älterer Versionen von Komponenten in neueren Versionen</span><span class="sxs-lookup"><span data-stu-id="97ba5-110">installing older versions of components over newer versions</span></span>
-   <span data-ttu-id="97ba5-111">Ändern der Sprache in einem System mit gemischter Sprache ohne Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="97ba5-111">changing the language in a mixed-language system without notification</span></span>
-   <span data-ttu-id="97ba5-112">Installieren mehrerer Kopien einer Bibliothek in verschiedenen Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="97ba5-112">installing multiple copies of a library in different directories</span></span>
-   <span data-ttu-id="97ba5-113">Kopieren von Dateien in Netzwerk Verzeichnisse, die von mehreren Benutzern gemeinsam genutzt werden</span><span class="sxs-lookup"><span data-stu-id="97ba5-113">copying files to network directories shared by multiple users</span></span>

<span data-ttu-id="97ba5-114">Mit den Versions Informationsfunktionen können Anwendungen eine Versions Ressource nach Dateiinformationen Abfragen und die Informationen in einem klaren Format darstellen.</span><span class="sxs-lookup"><span data-stu-id="97ba5-114">The version information functions enable applications to query a version resource for file information and present the information in a clear format.</span></span> <span data-ttu-id="97ba5-115">Zu diesen Informationen gehören der Zweck der Datei, der Autor, die Versionsnummer usw.</span><span class="sxs-lookup"><span data-stu-id="97ba5-115">This information includes the file's purpose, author, version number, and so on.</span></span>

<span data-ttu-id="97ba5-116">Sie können allen Dateien, die über Windows-Ressourcen verfügen, z. b. DLLs, ausführbare Dateien oder. FON-Schriftart Dateien, Versionsinformationen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="97ba5-116">You can add version information to any files that can have Windows resources, such as DLLs, executable files, or .fon font files.</span></span> <span data-ttu-id="97ba5-117">Um die Informationen hinzuzufügen, erstellen Sie eine [VERSIONINFO-Ressource](/windows/desktop/menurc/versioninfo-resource) , und kompilieren Sie die Ressource mit dem Ressourcen Compiler.</span><span class="sxs-lookup"><span data-stu-id="97ba5-117">To add the information, create a [VERSIONINFO Resource](/windows/desktop/menurc/versioninfo-resource) and use the resource compiler to compile the resource.</span></span>

 

 