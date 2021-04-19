---
description: Eine Anlage-Snap-in-Erweiterung bietet eine Schnittstelle, mit der Benutzer Dienst spezifische Konfigurationseinstellungen ändern können.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Erstellen einer Anlagen-Snap-in-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347712"
---
# <a name="creating-an-attachment-snap-in-extension"></a><span data-ttu-id="fc884-103">Erstellen einer Anlagen-Snap-in-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="fc884-103">Creating an Attachment Snap-in Extension</span></span>

<span data-ttu-id="fc884-104">Eine Anlage-Snap-in-Erweiterung bietet eine Schnittstelle, mit der Benutzer Dienst spezifische Konfigurationseinstellungen ändern können.</span><span class="sxs-lookup"><span data-stu-id="fc884-104">An attachment snap-in extension provides an interface that users can use to change service-specific configuration settings.</span></span> <span data-ttu-id="fc884-105">Die Erweiterungs-Snap-in-Erweiterung muss die MMC-Anforderungen erfüllen, damit Sie eine gültige Snap-in-Erweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="fc884-105">The attachment snap-in extension must fulfill the MMC requirements to be a valid snap-in extension.</span></span> <span data-ttu-id="fc884-106">Weitere Informationen zu diesen Anforderungen finden Sie in der Dokumentation zur [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="fc884-106">For more information on those requirements, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="fc884-107">Zusätzlich zu den von der MMC benötigten Schnittstellen muss die COM-Schnittstelle " [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)" implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc884-107">In addition to the interfaces required by MMC, an attachment snap-in extension must implement the COM interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="fc884-108">Mit den Sicherheits Konfigurations-Snap-Ins werden Methoden dieser Schnittstelle aufgerufen, um zu bestimmen, ob die Konfigurationsdaten geändert wurden, und wenn ja, um die Sicherheitsdatenbank zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fc884-108">The Security Configuration snap-ins call methods of this interface to determine whether the configuration data has changed, and if so, to update the security database.</span></span> <span data-ttu-id="fc884-109">Das Anlagen-Snap-in muss alle Konfigurationsänderungen speichern, bis die Sicherheits Konfigurations-Snap-ins diese Daten abrufen.</span><span class="sxs-lookup"><span data-stu-id="fc884-109">The attachment snap-in must store any configuration changes until the Security Configuration snap-ins retrieves that data.</span></span>

<span data-ttu-id="fc884-110">Eine Anlage-Snap-in-Erweiterung muss die folgenden Funktionen bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="fc884-110">An attachment snap-in extension must provide the following functionality:</span></span>

-   [<span data-ttu-id="fc884-111">Konfigurations-und Analyse Informationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="fc884-111">Display Configuration and Analysis Information</span></span>](displaying-configuration-and-analysis-information.md)
-   [<span data-ttu-id="fc884-112">Ändern der Konfigurationsinformationen in der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="fc884-112">Modify Configuration Information in the User Interface</span></span>](modifying-configuration-information-in-the-user-interface.md)
-   [<span data-ttu-id="fc884-113">Ändern der Konfigurationsinformationen in der Sicherheitsdatenbank</span><span class="sxs-lookup"><span data-stu-id="fc884-113">Modify Configuration Information in the Security Database</span></span>](modifying-configuration-information-in-the-database.md)

<span data-ttu-id="fc884-114">Um Ihre Snap-in-Erweiterung bei der Ausführung dieser Aufgaben zu unterstützen, implementieren die Sicherheitskonfigurations-Snap-Ins eine COM-Schnittstelle, [**iscesvasetachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), die Methoden bereitstellt, die Ihre Snap-in-Erweiterung zum Initialisieren und Abfragen von Informationen aus der Sicherheitsdatenbank aufruft.</span><span class="sxs-lookup"><span data-stu-id="fc884-114">To assist your snap-in extension in performing these tasks, the Security Configuration snap-ins implement a COM interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), which provides methods your snap-in extension can call in order to initialize itself and query information from the security database.</span></span>

<span data-ttu-id="fc884-115">Nachdem Sie die Erweiterungs-Snap-in-Erweiterung erstellt haben, müssen Sie Sie mit den Snap-Ins für die Sicherheitskonfiguration registrieren, wie unter [Registrieren einer Anlage-Snap-in-Erweiterung](registering-an-attachment-snap-in-extension.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc884-115">After you have created your attachment snap-in extension, you must register it with the Security Configuration snap-ins as described in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span>

 

 
