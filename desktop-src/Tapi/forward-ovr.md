---
description: Bei der Weiterleitung wird eine eingehende Sitzung an eine andere Zieladresse umgeleitet.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Weiter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862619"
---
# <a name="forward"></a>Weiter

Bei der Weiterleitung wird eine eingehende Sitzung an eine andere Zieladresse umgeleitet. TAPI ermöglicht es einer Anwendung, eine Liste von Weiterleitungs Bedingungen für eine Adresse anzugeben. Weiterleitungs Bedingungen können für jede aufrufende Adresse so fein wie ein anderes Ziel und [**Weiterleitungs Modus**](./lineforwardmode--constants.md) sein.

Der Weiterleitungs Vorgang kann auch verwendet werden, um eine selektive Funktion zum stören von Funktionen zu implementieren, indem einige Aufrufer an Voicemail weitergeleitet werden und anderen Benutzer den abschlussversuch gestatten.

Der Weiterleitungs Vorgang kann auch alle derzeit gültigen Weiterleitungen abbrechen.

Einige Dienstanbieter erfordern, dass eine Anwendung vor einem Weiterleitungs Vorgang einen Beratungs Rückruf erstellt. Der Weiterleitungs Vorgang wird dann als Zeiger auf den-Rückruf übermittelt.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Wenn Sie [**lineforward**](/windows/win32/api/tapi/nf-tapi-lineforward) festlegen möchten, um [**linegetaddressstatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)zu erhalten, ändern Sie die [**Zeile \_ addressstate**](./line-addressstate.md) -Benachrichtigungs Meldung mit lineaddressstate \_ Forward.

**TAPI 3. x:** Weitere Informationen finden Sie unter [**itaddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**itaddress:: get \_ currentforwardinfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), Change Notification: [**itadressssevent:: get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ Forward.

> [!Note]  
> Es ist möglicherweise nicht möglich, dass ein Dienstanbieter immer weiß, welche Weiterleitung für eine Adresse wirksam ist. Die Weiterleitung kann auf eine Weise abgebrochen oder geändert werden, die nicht zur Benachrichtigung an den Dienstanbieter führt.

 

 

 
