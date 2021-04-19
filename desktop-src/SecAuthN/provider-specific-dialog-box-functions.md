---
description: Mit anbieterspezifischen Dialogfeld Funktionen kann ein anbieternetzwerk spezifische Informationen anzeigen und behandeln, indem er die System Dialogfelder ändert oder benutzerdefinierte Dialogfelder anzeigt.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Dialog Feld Funktionen Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360765"
---
# <a name="provider-specific-dialog-box-functions"></a>Dialog Feld Funktionen Provider-Specific

Mit anbieterspezifischen Dialogfeld Funktionen kann ein anbieternetzwerk spezifische Informationen anzeigen und behandeln, indem er die System Dialogfelder ändert oder benutzerdefinierte Dialogfelder anzeigt.

Im folgenden Dialogfeld können Sie dem Dialogfeld **Eigenschaften** des Datei-Managers Schaltflächen hinzufügen. Der Anbieter kann dann die Ereignisse dieser Schaltflächen verarbeiten, um Netzwerk spezifische Aufgaben auszuführen. Beachten Sie, dass die Anzahl der Schaltflächen, die hinzugefügt werden können, begrenzt ist. Aus diesem Grund sollten Anbieter diese Funktion sparsam verwenden. Ein Anbieter kann auch eine Schaltfläche nicht hinzufügen, da der verfügbare Speicherplatz bereits von anderen Anbietern verwendet wurde. Ein Netzwerkanbieter sollte diese Situation verarbeiten.



| Funktion                                           | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Npgetpropertytext**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Bestimmt die Namen von Schaltflächen, die zu einem Eigenschaften Dialogfeld für eine bestimmte Ressource hinzugefügt werden.<br/>                                      |
| [**Nppropertydialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Wird aufgerufen, wenn ein Benutzer auf eine Schaltfläche klickt, die mithilfe der [**npgetpropertytext**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) -Funktion hinzugefügt wurde.<br/>               |
| [**Npsearchdialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Ermöglicht es Netzwerkanbietern, eigene Suchfunktionen zu implementieren, die über die im **Verbindungs** Dialogfeld bereitgestellten hinausgehen.<br/> |
| [**Npformatnetworkname**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Ermöglicht Netzwerkanbietern das Formatieren oder andere ändern von Netzwerknamen, bevor Sie dem Benutzer angezeigt werden.<br/>                 |



 

 

 




