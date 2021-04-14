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
# <a name="installation-windows-multimedia"></a>Installation (Windows Multimedia)

Ein installier barer Treiber kann Treiber spezifische Installationsaufgaben ausführen, wenn die [**drv- \_ Installations**](drv-install.md) -und [**drv- \_ Entfernungs**](drv-remove.md) Meldungen verarbeitet werden. Eine Installationsanwendung (z. b. eine System Steuerungsanwendung) sendet die Nachrichten an den Treiber, wenn der Treiber installiert bzw. entfernt wird.

Bei der Verarbeitung der drv \_ -Installations Meldung überprüft der Treiber in der Regel, ob die erforderliche Hardware vorhanden ist. Anschließend wird das Dialogfeld Konfiguration angezeigt, in dem der Benutzer die anfänglichen Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen kann. Die Nachricht enthält die Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur, die die Namen des Registrierungsschlüssels und des Werts enthält, die dem Treiber zugeordnet sind. der Treiber überprüft den Registrierungs Wert auf Standard Konfigurationsinformationen. Schließlich erstellt der Treiber auch alle zusätzlichen Registrierungsschlüssel und-Werte, die für den erfolgreichen Betrieb erforderlich sind.

Beim Verarbeiten der drv \_ -Entfernungs Nachricht entfernt der Treiber alle Registrierungsschlüssel und-Werte, die er möglicherweise erstellt hat.

 

 
