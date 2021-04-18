---
description: Gebiets Schema \_ nouseroverride
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368779"
---
# <a name="locale_nouseroverride"></a><span data-ttu-id="be6a5-103">Gebiets Schema \_ nouseroverride</span><span class="sxs-lookup"><span data-stu-id="be6a5-103">LOCALE\_NOUSEROVERRIDE</span></span>

> [!Caution]  
> <span data-ttu-id="be6a5-104">Da das Gebiets Schema " \_ nouseroverride" Benutzereinstellungen deaktiviert, wird dringend davon abgeraten.</span><span class="sxs-lookup"><span data-stu-id="be6a5-104">Since LOCALE\_NOUSEROVERRIDE disables user preferences, its use is strongly discouraged.</span></span> <span data-ttu-id="be6a5-105">Diese Konstante garantiert keine Daten Stabilität, da [benutzerdefinierte](custom-locales.md)Gebiets Schemas, Dienst Updates, andere Betriebssystemversionen und andere Szenarien Daten auf unerwartete Weise ändern können.</span><span class="sxs-lookup"><span data-stu-id="be6a5-105">This constant does not guarantee data stability since [custom locales](custom-locales.md), service updates, different operating system versions, and other scenarios can change data in unexpected ways.</span></span> <span data-ttu-id="be6a5-106">Weitere Informationen finden Sie unter [Verwenden von persistenten](using-persistent-locale-data.md)Gebiets Schema Daten.</span><span class="sxs-lookup"><span data-stu-id="be6a5-106">For more information, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

<span data-ttu-id="be6a5-107">Keine Benutzer Überschreibung.</span><span class="sxs-lookup"><span data-stu-id="be6a5-107">No user override.</span></span> <span data-ttu-id="be6a5-108">In mehreren Funktionen, z. b. [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) und [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), bewirkt diese Konstante, dass die Funktion jede Benutzer Außerkraftsetzung umgeht und den System Standardwert für jede andere Konstante verwendet, die im Funktions aufrufsausdruck angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="be6a5-108">In several functions, for example, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), this constant causes the function to bypass any user override and use the system default value for any other constant specified in the function call.</span></span> <span data-ttu-id="be6a5-109">Die Informationen werden aus der locale-Datenbank abgerufen, auch wenn der Bezeichner das aktuelle Gebiets Schema angibt und der Benutzer einige der Werte mithilfe der Systemsteuerung geändert hat oder wenn eine Anwendung diese Werte mithilfe von [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa)geändert hat.</span><span class="sxs-lookup"><span data-stu-id="be6a5-109">The information is retrieved from the locale database, even if the identifier indicates the current locale and the user has changed some of the values using the Control Panel, or if an application has changed these values by using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="be6a5-110">Wenn diese Konstante nicht angegeben ist, haben alle Werte, die der Benutzer in der Systemsteuerung konfiguriert hat, oder eine Anwendung, die mithilfe von [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) konfiguriert wurde, Vorrang vor den Datenbankeinstellungen für das aktuelle Standard Gebiets Schema des Systems.</span><span class="sxs-lookup"><span data-stu-id="be6a5-110">If this constant is not specified, any values that the user has configured from the Control Panel or that an application has configured using [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) take precedence over the database settings for the current system default locale.</span></span>

 

 



