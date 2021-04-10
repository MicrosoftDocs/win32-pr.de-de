---
title: Konfiguration (Windows Multimedia)
description: Konfiguration
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- installierbare Treiber, Konfiguration
- installierbare Treiber, DRV_CONFIGURE Meldung
- DRV_CONFIGURE Meldung
- DRV_QUERYCONFIGURE Meldung
- Drvconfiginfo-Meldung
- Konfigurieren installier barer Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a248f992a857b88b723bd54c771f1af5709d97
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039962"
---
# <a name="configuration-windows-multimedia"></a><span data-ttu-id="b2f93-109">Konfiguration (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="b2f93-109">Configuration (Windows Multimedia)</span></span>

<span data-ttu-id="b2f93-110">Mithilfe eines installierbaren Treibers können Benutzer Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen, indem Sie beim verarbeiten [**der \_ drv**](drv-configure.md) -Konfigurations Nachricht ein Konfigurations Dialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2f93-110">An installable driver can let users choose configuration settings for the driver and associated hardware by displaying a configuration dialog box when processing the [**DRV\_CONFIGURE**](drv-configure.md) message.</span></span> <span data-ttu-id="b2f93-111">Der Treiber ist verantwortlich für das Erstellen und Verwalten des Dialog Felds, das Verarbeiten von Benutzereingaben aus dem Dialogfeld und das Ändern der Konfiguration des Treibers bzw. der Hardware, wie vom Benutzer angefordert.</span><span class="sxs-lookup"><span data-stu-id="b2f93-111">The driver is responsible for creating and managing the dialog box, processing any user input from the dialog box, and changing the configuration of the driver or hardware as requested by the user.</span></span> <span data-ttu-id="b2f93-112">Der Treiber muss eine separate Dialogfeld Prozedur zum Verarbeiten von Fenster Meldungen für das Dialogfeld und eine Dialogfeld Vorlage bereitstellen, um die Darstellung und den Inhalt des Dialog Felds zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b2f93-112">The driver must provide a separate dialog box procedure to process window messages for the dialog box and a dialog box template to define the appearance and content of the dialog box.</span></span>

<span data-ttu-id="b2f93-113">Vor dem Empfang der drv- \_ Konfigurations Nachricht erhält ein Treiber die [**drv-Abfrage " \_ queryconfigure**](drv-queryconfigure.md) ".</span><span class="sxs-lookup"><span data-stu-id="b2f93-113">Before receiving the DRV\_CONFIGURE message, a driver receives the [**DRV\_QUERYCONFIGURE**](drv-queryconfigure.md) message.</span></span> <span data-ttu-id="b2f93-114">Der Treiber muss einen Wert ungleich 0 (null) an die Abfrage zurückgeben, um den Empfang der nachfolgenden drv- \_ Konfigurations Meldung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="b2f93-114">The driver must return a nonzero value to the query to ensure receipt of the subsequent DRV\_CONFIGURE message.</span></span>

<span data-ttu-id="b2f93-115">Wenn Sie das Dialogfeld Konfiguration initialisieren, ruft der Treiber normalerweise Konfigurationsinformationen aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="b2f93-115">When initializing the configuration dialog box, the driver typically retrieves configuration information from the registry.</span></span> <span data-ttu-id="b2f93-116">Um diese Informationen zu finden, enthält die drv \_ -Konfigurations Nachricht in der Regel die Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur, die die Namen des Registrierungsschlüssels und des Werts enthält, die dem Treiber zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b2f93-116">To help locate this information, the DRV\_CONFIGURE message usually includes the address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure that contains the names of the registry key and value associated with the driver.</span></span> <span data-ttu-id="b2f93-117">Wenn der Benutzer Änderungen an der Konfiguration anfordert, sollte der Treiber die Konfigurationsinformationen in der Registrierung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b2f93-117">If the user requests changes to the configuration, the driver should update the configuration information in the registry.</span></span>

 

 
