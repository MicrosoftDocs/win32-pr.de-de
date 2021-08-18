---
title: Konfiguration (Windows Multimedia)
description: Erfahren Sie, wie Windows multimedia-Treiber Benutzern die Auswahl von Konfigurationseinstellungen ermöglichen kann, indem sie ein Konfigurationsdialogfeld anzeigen.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- Installierbare Treiber, Konfiguration
- Installierbare Treiber, DRV_CONFIGURE
- DRV_CONFIGURE-Nachricht
- DRV_QUERYCONFIGURE-Nachricht
- DRVCONFIGINFO-Meldung
- Konfigurieren installierbarer Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1f5079878ba3da60484efb8afccc2effbbd8ec7212dfd339ab0cba5f43653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144963"
---
# <a name="configuration-windows-multimedia"></a>Konfiguration (Windows Multimedia)

Mit einem installierbaren Treiber können Benutzer Konfigurationseinstellungen für den Treiber und die zugehörige Hardware auswählen, indem sie beim Verarbeiten der DRV CONFIGURE-Meldung ein [**\_ Konfigurationsdialogfeld**](drv-configure.md) anzeigen. Der Treiber ist für das Erstellen und Verwalten des Dialogfelds, die Verarbeitung beliebiger Benutzereingaben aus dem Dialogfeld und das Ändern der Konfiguration des Treibers oder der Hardware verantwortlich, wie vom Benutzer angefordert. Der Treiber muss eine separate Dialogfeldprozedur zum Verarbeiten von Fenstermeldungen für das Dialogfeld und eine Dialogfeldvorlage bereitstellen, um die Darstellung und den Inhalt des Dialogfelds zu definieren.

Vor dem Empfang der DRV \_ CONFIGURE-Nachricht empfängt ein Treiber die [**DRV \_ QUERYCONFIGURE-Nachricht.**](drv-queryconfigure.md) Der Treiber muss einen Wert ungleich 0 (null) an die Abfrage zurückgeben, um den Empfang der nachfolgenden DRV \_ CONFIGURE-Nachricht sicherzustellen.

Beim Initialisieren des Konfigurationsdialogfelds ruft der Treiber in der Regel Konfigurationsinformationen aus der Registrierung ab. Um diese Informationen zu finden, enthält die DRV CONFIGURE-Meldung in der Regel die Adresse einer \_ [**DRVCONFIGINFO-Struktur,**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) die die Namen des Registrierungsschlüssels und des Werts enthält, die dem Treiber zugeordnet sind. Wenn der Benutzer Änderungen an der Konfiguration an fordert, sollte der Treiber die Konfigurationsinformationen in der Registrierung aktualisieren.

 

 
