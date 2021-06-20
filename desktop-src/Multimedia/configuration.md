---
title: Konfiguration (Windows Multimedia)
description: Erfahren Sie, wie Ein Windows Multimedia-Treiber Benutzern das Auswählen von Konfigurationseinstellungen ermöglichen kann, indem ein Konfigurationsdialogfeld angezeigt wird.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- Installierbare Treiber, Konfiguration
- Installierbare Treiber, DRV_CONFIGURE Meldung
- DRV_CONFIGURE Meldung
- DRV_QUERYCONFIGURE Meldung
- DRVCONFIGINFO-Meldung
- Konfigurieren von installierbaren Treibern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403923"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="a63f8-109">Konfiguration (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="a63f8-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="a63f8-110">Mit einem installierbaren Treiber können Benutzer Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen, indem sie bei der Verarbeitung der [**DRV \_ CONFIGURE-Meldung**](drv-configure.md) ein Konfigurationsdialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a63f8-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="a63f8-111">Der Treiber ist dafür verantwortlich, das Dialogfeld zu erstellen und zu verwalten, alle Benutzereingaben aus dem Dialogfeld zu verarbeiten und die Konfiguration des Treibers oder der Hardware wie vom Benutzer angefordert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a63f8-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="a63f8-112">Der Treiber muss eine separate Dialogfeldprozedur zum Verarbeiten von Fenstermeldungen für das Dialogfeld und eine Dialogfeldvorlage bereitstellen, um die Darstellung und den Inhalt des Dialogfelds zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a63f8-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="a63f8-113">Vor dem Empfang der DRV \_ CONFIGURE-Nachricht empfängt ein Treiber die [**DRV \_ QUERYCONFIGURE-Nachricht.**](drv-queryconfigure.md)</span><span class="sxs-lookup"><span data-stu-id="a63f8-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="a63f8-114">Der Treiber muss einen Wert ungleich 0 (null) an die Abfrage zurückgeben, um sicherzustellen, dass die nachfolgende DRV \_ CONFIGURE-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="a63f8-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="a63f8-115">Beim Initialisieren des Konfigurationsdialogfelds ruft der Treiber in der Regel Konfigurationsinformationen aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="a63f8-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="a63f8-116">Um diese Informationen zu finden, enthält die DRV \_ CONFIGURE-Nachricht in der Regel die Adresse einer [**DRVCONFIGINFO-Struktur,**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) die die Namen des Registrierungsschlüssels und den wert enthält, der dem Treiber zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a63f8-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="a63f8-117">Wenn der Benutzer Änderungen an der Konfiguration anfordert, sollte der Treiber die Konfigurationsinformationen in der Registrierung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a63f8-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
