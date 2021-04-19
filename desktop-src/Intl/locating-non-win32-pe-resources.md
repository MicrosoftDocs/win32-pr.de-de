---
description: Suchen von nicht-Win32 PE-Ressourcen
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Suchen von nicht-Win32 PE-Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079288cd6200eb64289f474636cbc8dc046c1e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356830"
---
# <a name="locating-non-win32-pe-resources"></a><span data-ttu-id="abfd3-103">Suchen von nicht-Win32 PE-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="abfd3-103">Locating Non-Win32 PE Resources</span></span>

<span data-ttu-id="abfd3-104">Um nicht-Win32 PE-Ressourcen zu suchen, sollte Ihre Anwendung zuerst die [**getfilemuipath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) -Funktion aufrufen, um die sprachspezifische Ressourcen Datei zu suchen, aus der Ressourcen geladen werden.</span><span class="sxs-lookup"><span data-stu-id="abfd3-104">To locate non-Win32 PE resources, your application should first call the [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) function to locate the language-specific resource file from which to load resources.</span></span> <span data-ttu-id="abfd3-105">Wenn die Anwendung den Einstellungen der Systemsprache folgt, muss Sie die-Funktion mit den für " \_ \_ \| \_ \_ \_ \_ *dwFlags* " angegebenen benutzerdefinierten UI-Sprachen für  "MUI Language Name MUI" und "Null" für " *pwszlanguage*" aufruft.</span><span class="sxs-lookup"><span data-stu-id="abfd3-105">If the application is following system language settings, it must call the function with MUI\_LANGUAGE\_NAME \| MUI\_USER\_PREFERRED\_UI\_LANGUAGES specified for *dwFlags* and **NULL** specified for *pwszLanguage*.</span></span> <span data-ttu-id="abfd3-106">Wenn die Anwendung anwendungsspezifische Spracheinstellungen verwendet, wird **getfilemuipath** verwendet, um zu bestimmen, ob eine sprachspezifische Datei vorhanden ist, indem die Sprache im *pwszlanguage* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abfd3-106">If the application is following application-specific language settings, it uses **GetFileMUIPath** to determine if a language-specific file exists by specifying the language in the *pwszLanguage* parameter.</span></span>

<span data-ttu-id="abfd3-107">Nach dem Aufrufen von [**getfilemuipath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)muss die Anwendung benutzerdefinierte Funktionen definieren, um das Ressourcen Modul zu laden und bestimmte Ressourcen daraus zu laden.</span><span class="sxs-lookup"><span data-stu-id="abfd3-107">After the call to [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath), the application must define custom functionality to load the resource module and load specific resources from it.</span></span> <span data-ttu-id="abfd3-108">Wenn Sie z. b. eine txt-oder XML-Ressourcen Datei verwenden, muss die Anwendung einen txt-oder XML-Parser verwenden, um die Datei zu laden und dann den Inhalt der Datei für jede erforderliche Ressource zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="abfd3-108">For example, if you are using a .txt or .xml resource file, the application must use a TXT or XML parser to load the file and then parse the contents of the file for each required resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abfd3-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="abfd3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abfd3-110">Verwenden der mehrsprachigen Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="abfd3-110">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="abfd3-111">**Getfilemuipath**</span><span class="sxs-lookup"><span data-stu-id="abfd3-111">**GetFileMUIPath**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



