---
title: Installation (Windows Multimedia)
description: Installation
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- installierbare Treiber, installieren
- installierbare Treiber, DRV_INSTALL Meldung
- installierbare Treiber, DRV_REMOVE Meldung
- DRV_INSTALL Meldung
- DRV_REMOVE Meldung
- Drvconfiginfo-Meldung
- Installieren von Treibern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ebebd090c7499698c59c325d1ac0d487902454
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391399"
---
# <a name="installation-windows-multimedia"></a><span data-ttu-id="1540c-110">Installation (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="1540c-110">Installation (Windows Multimedia)</span></span>

<span data-ttu-id="1540c-111">Ein installier barer Treiber kann Treiber spezifische Installationsaufgaben ausführen, wenn die [**drv- \_ Installations**](drv-install.md) -und [**drv- \_ Entfernungs**](drv-remove.md) Meldungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1540c-111">An installable driver can carry out driver-specific installation tasks when processing the [**DRV\_INSTALL**](drv-install.md) and [**DRV\_REMOVE**](drv-remove.md) messages.</span></span> <span data-ttu-id="1540c-112">Eine Installationsanwendung (z. b. eine System Steuerungsanwendung) sendet die Nachrichten an den Treiber, wenn der Treiber installiert bzw. entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1540c-112">An installation application, such as a Control Panel application, sends the messages to the driver when installing or removing the driver, respectively.</span></span>

<span data-ttu-id="1540c-113">Bei der Verarbeitung der drv \_ -Installations Meldung überprüft der Treiber in der Regel, ob die erforderliche Hardware vorhanden ist. Anschließend wird das Dialogfeld Konfiguration angezeigt, in dem der Benutzer die anfänglichen Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="1540c-113">When processing the DRV\_INSTALL message, the driver typically verifies that the required hardware is present and then displays the configuration dialog box to let the user choose the initial configuration settings for the driver and associated hardware.</span></span> <span data-ttu-id="1540c-114">Die Nachricht enthält die Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur, die die Namen des Registrierungsschlüssels und des Werts enthält, die dem Treiber zugeordnet sind. der Treiber überprüft den Registrierungs Wert auf Standard Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="1540c-114">The message includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver; the driver checks the registry value for default configuration information.</span></span> <span data-ttu-id="1540c-115">Schließlich erstellt der Treiber auch alle zusätzlichen Registrierungsschlüssel und-Werte, die für den erfolgreichen Betrieb erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1540c-115">Finally, the driver also creates any additional registry keys and values needed for successful operation.</span></span>

<span data-ttu-id="1540c-116">Beim Verarbeiten der drv \_ -Entfernungs Nachricht entfernt der Treiber alle Registrierungsschlüssel und-Werte, die er möglicherweise erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="1540c-116">When processing the DRV\_REMOVE message, the driver removes any registry keys and values it may have created.</span></span>

 

 
