---
title: Installation (Windows Multimedia)
description: Erfahren Sie mehr Windows Multimedia-Installation, einschließlich der Verarbeitung DRV_INSTALL und DRV_REMOVE Nachrichten.
ms.assetid: 1f0e23ad-4db7-4f32-98d9-e672370db559
keywords:
- Installierbare Treiber,Installieren
- Installierbare Treiber, DRV_INSTALL
- Installierbare Treiber, DRV_REMOVE
- DRV_INSTALL Nachricht
- DRV_REMOVE Nachricht
- DRVCONFIGINFO-Meldung
- Installieren von Treibern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ef47952f3d5a62c0dce246bf24689d37f11326f0f3ec251f7afc19c822fa9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140678"
---
# <a name="installation-windows-multimedia"></a>Installation (Windows Multimedia)

Ein installierbarer Treiber kann treiberspezifische Installationsaufgaben ausführen, wenn die [**DRV \_ INSTALL-**](drv-install.md) und [**DRV \_ REMOVE-Meldungen verarbeitet**](drv-remove.md) werden. Eine Installationsanwendung, z. B. Systemsteuerung Anwendung, sendet die Nachrichten an den Treiber, wenn der Treiber installiert oder entfernt wird.

Bei der Verarbeitung der DRV-Installationsmeldung überprüft der Treiber in der Regel, ob die erforderliche Hardware vorhanden ist, und zeigt dann das Konfigurationsdialogfeld an, damit der Benutzer die anfänglichen Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen \_ kann. Die Nachricht enthält die Adresse einer [**DRVCONFIGINFO-Struktur,**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) die die Namen des Registrierungsschlüssels und des Werts enthält, die dem Treiber zugeordnet sind. Der Treiber überprüft den Registrierungswert auf Standardkonfigurationsinformationen. Schließlich erstellt der Treiber auch alle zusätzlichen Registrierungsschlüssel und Werte, die für einen erfolgreichen Vorgang erforderlich sind.

Bei der Verarbeitung der DRV-REMOVE-Nachricht entfernt der Treiber alle Registrierungsschlüssel und Werte, die \_ er möglicherweise erstellt hat.

 

 
