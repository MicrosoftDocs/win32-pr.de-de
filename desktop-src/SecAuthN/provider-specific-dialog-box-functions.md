---
description: Anbieterspezifische Dialogfeldfunktionen ermöglichen es einem Anbieter, netzwerkspezifische Informationen anzuzeigen und zu verarbeiten, indem Systemdialogfelder geändert oder benutzerdefinierte Dialogfelder angezeigt werden.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific Dialogfeldfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d31a38f09dd0e0806fe21f491d02b5e18fe0abb1e5a181e40f0ab6370280b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920577"
---
# <a name="provider-specific-dialog-box-functions"></a>Provider-Specific Dialogfeldfunktionen

Anbieterspezifische Dialogfeldfunktionen ermöglichen es einem Anbieter, netzwerkspezifische Informationen anzuzeigen und zu verarbeiten, indem Systemdialogfelder geändert oder benutzerdefinierte Dialogfelder angezeigt werden.

Die folgenden Dialogfeldfunktionen fügen Schaltflächen zum Dialogfeld **Datei-Manager-Eigenschaften** hinzu. Der Anbieter kann dann die Ereignisse dieser Schaltflächen verarbeiten, um netzwerkspezifische Aufgaben auszuführen. Beachten Sie, dass es eine Beschränkung für die Anzahl von Schaltflächen gibt, die hinzugefügt werden können. Aus diesem Grund sollten Anbieter diese Funktion nur wenig verwenden. Außerdem kann ein Anbieter möglicherweise keine Schaltfläche hinzufügen, da der verfügbare Speicherplatz bereits von anderen Anbietern verwendet wurde. Dieser Fall sollte von einem Netzwerkanbieter behandelt werden.



| Funktion                                           | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Bestimmt die Namen der Schaltflächen, die einem Eigenschaftendialogfeld für eine bestimmte Ressource hinzugefügt werden.<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Wird aufgerufen, wenn ein Benutzer mithilfe der [**NPGetPropertyText-Funktion**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) auf eine Schaltfläche klickt, die hinzugefügt wurde.<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Ermöglicht Netzwerkanbietern, ihre eigene Suchfunktion über die im Dialogfeld Verbindung **bereitgestellte hinaus** zu implementieren.<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Ermöglicht Es Netzwerkanbietern, Netzwerknamen zu formatieren oder anderweitig zu ändern, bevor sie dem Benutzer angezeigt werden.<br/>                 |



 

 

 




