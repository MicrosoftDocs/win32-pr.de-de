---
title: Installation (Windows Multimedia)
description: Erfahren Sie mehr über die Installation von Windows Multimedia, einschließlich der Verarbeitung DRV_INSTALL und DRV_REMOVE Nachrichten.
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- Installierbare Treiber,Installieren
- Installierbare Treiber, DRV_INSTALL
- Installierbare Treiber, DRV_REMOVE
- DRV_INSTALL-Nachricht
- DRV_REMOVE-Nachricht
- DRVCONFIGINFO-Meldung
- Installieren von Treibern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f82a23a781e62553d6488331b2c832104fd770
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989035"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="c727e-110">Installation (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="c727e-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="c727e-111">Ein installierbarer Treiber kann treiberspezifische Installationsaufgaben ausführen, wenn die [**DRV \_ INSTALL-**](drv-install.md) und [**DRV \_ REMOVE-Meldungen verarbeitet**](drv-remove.md) werden.</span><span class="sxs-lookup"><span data-stu-id="c727e-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="c727e-112">Eine Installationsanwendung, z. B. Systemsteuerung Anwendung, sendet die Nachrichten an den Treiber, wenn der Treiber installiert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c727e-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="c727e-113">Bei der Verarbeitung der DRV-Installationsmeldung überprüft der Treiber in der Regel, ob die erforderliche Hardware vorhanden ist, und zeigt dann das Konfigurationsdialogfeld an, damit der Benutzer die anfänglichen Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen \_ kann.</span><span class="sxs-lookup"><span data-stu-id="c727e-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="c727e-114">Die Nachricht enthält die Adresse einer [**DRVCONFIGINFO-Struktur,**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) die die Namen des Registrierungsschlüssels und des Werts enthält, die dem Treiber zugeordnet sind. Der Treiber überprüft den Registrierungswert auf Standardkonfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="c727e-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="c727e-115">Schließlich erstellt der Treiber auch alle zusätzlichen Registrierungsschlüssel und Werte, die für einen erfolgreichen Vorgang erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c727e-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="c727e-116">Beim Verarbeiten der DRV-REMOVE-Nachricht entfernt der Treiber alle Registrierungsschlüssel und Werte, die \_ er möglicherweise erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="c727e-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
