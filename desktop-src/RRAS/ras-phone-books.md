---
title: RAS-Telefonbücher
description: Telefonbücher stellen eine Standardmethode zum Erfassen und angeben der Informationen dar, die der RAS-Verbindungs-Manager zum Herstellen einer Remote Verbindung benötigt.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Telefonbücher, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037061"
---
# <a name="ras-phone-books"></a><span data-ttu-id="954a7-104">RAS-Telefonbücher</span><span class="sxs-lookup"><span data-stu-id="954a7-104">RAS Phone Books</span></span>

<span data-ttu-id="954a7-105">Telefonbücher stellen eine Standardmethode zum Erfassen und angeben der Informationen dar, die der RAS-Verbindungs-Manager zum Herstellen einer Remote Verbindung benötigt.</span><span class="sxs-lookup"><span data-stu-id="954a7-105">Phone books provide a standard way to collect and specify the information that the Remote Access Connection Manager needs to establish a remote connection.</span></span> <span data-ttu-id="954a7-106">In Telefonbüchern werden Eintrags Namen mit Informationen wie Telefonnummern, com-Ports und Modem Einstellungen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="954a7-106">Phone books associate entry names with information such as phone numbers, COM ports, and modem settings.</span></span> <span data-ttu-id="954a7-107">Jeder Telefonbucheintrag enthält die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="954a7-107">Each phone-book entry contains the information needed to establish a RAS connection.</span></span>

<span data-ttu-id="954a7-108">Telefonbücher werden in Telefonbuch Dateien gespeichert. dabei handelt es sich um Textdateien, die die Eintrags Namen und die zugehörigen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="954a7-108">Phone books are stored in phone-book files, which are text files that contain the entry names and associated information.</span></span> <span data-ttu-id="954a7-109">RAS erstellt eine Telefonbuchdatei mit dem Namen RASPHONE. Pbk.</span><span class="sxs-lookup"><span data-stu-id="954a7-109">RAS creates a phone-book file called RASPHONE.PBK.</span></span> <span data-ttu-id="954a7-110">Der Benutzer kann das Dialogfeld "hauptdfü **-Netzwerk** " verwenden, um persönliche Telefonbuch Dateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="954a7-110">The user can use the main **Dial-Up Networking** dialog box to create personal phone-book files.</span></span> <span data-ttu-id="954a7-111">Die RAS-API bietet derzeit keine Unterstützung für das Erstellen einer Telefonbuchdatei.</span><span class="sxs-lookup"><span data-stu-id="954a7-111">The RAS API does not currently provide support for creating a phone-book file.</span></span> <span data-ttu-id="954a7-112">Einige RAS-Funktionen, wie z. b. die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ", verfügen über einen Parameter, der eine Telefonbuchdatei angibt.</span><span class="sxs-lookup"><span data-stu-id="954a7-112">Some RAS functions, such as the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function, have a parameter that specifies a phone-book file.</span></span> <span data-ttu-id="954a7-113">Wenn der Aufrufer keine Telefonbuchdatei angibt, verwendet die Funktion die standardmäßige Telefonbuchdatei, die vom Benutzer auf dem Eigenschaften Blatt **Benutzereinstellungen** des Dialog Felds DFÜ **-Netzwerke** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="954a7-113">If the caller does not specify a phone-book file, the function uses the default phone-book file, which is the one selected by the user in the **User Preferences** property sheet of the **Dial-Up Networking** dialog box.</span></span>

<span data-ttu-id="954a7-114">Windows NT 4,0 bietet die Funktionen [**rasphonebookdlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) und [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) , die die integrierte RAS-Benutzeroberfläche anzeigen, mit deren Hilfe Benutzer mit Telefonbüchern und Telefonbucheinträgen arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="954a7-114">Windows NT 4.0 provides the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) functions that display the built-in RAS user interface that enable users to work with phone books and phone-book entries.</span></span>

<span data-ttu-id="954a7-115">**Windows 95:** Das Einwählnetzwerk speichert Telefonbucheinträge in der Registrierung und nicht in einer Telefonbuchdatei.</span><span class="sxs-lookup"><span data-stu-id="954a7-115">**Windows 95:** Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.</span></span> <span data-ttu-id="954a7-116">Windows 95 unterstützt keine persönlichen Telefonbuch Dateien oder Funktionen, die die integrierten RAS-Dialogfelder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="954a7-116">Windows 95 does not support personal phone-book files or functions that display the built-in RAS dialog boxes.</span></span>

 

 




