---
description: Der Windows Installer-Dienst verwendet die Sprache des aktuellen Benutzers in allen Dialogfeldern, bis ein Windows Installer Paket geöffnet wird.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Lokalisieren der von Dialogfeldern angezeigten Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353579"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a><span data-ttu-id="f3260-103">Lokalisieren der von Dialogfeldern angezeigten Sprache</span><span class="sxs-lookup"><span data-stu-id="f3260-103">Localizing the Language Displayed by Dialogs</span></span>

<span data-ttu-id="f3260-104">Der Windows Installer-Dienst verwendet die Sprache des aktuellen Benutzers in allen Dialogfeldern, bis ein Windows Installer Paket geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f3260-104">The Windows Installer service uses the current user's language in all dialogs until a Windows Installer package is opened.</span></span> <span data-ttu-id="f3260-105">Der Windows Installer bestimmt dies mithilfe von **GetUserDefaultUILanguage**.</span><span class="sxs-lookup"><span data-stu-id="f3260-105">The Windows Installer determines this by using **GetUserDefaultUILanguage**.</span></span> <span data-ttu-id="f3260-106">Wenn ein Windows Installer Paket geöffnet wird, zeigt das Installationsprogramm die Dialoge mithilfe der Sprache des Pakets an, wie in der Eigenschaft [**Vorlagen Zusammenfassung**](template-summary.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3260-106">When a Windows Installer package is opened, the installer displays dialogs using the package's language as specified by the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="f3260-107">Weitere Informationen zum Lokalisieren der Sprache eines Windows Installer Pakets finden Sie unter [ein Beispiel für eine Lokalisierung](a-localization-example.md).</span><span class="sxs-lookup"><span data-stu-id="f3260-107">For more information about localizing the language of a Windows Installer package, see also [A Localization Example](a-localization-example.md).</span></span>

 

 



