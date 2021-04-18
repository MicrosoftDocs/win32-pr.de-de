---
description: Gebiets Schema \_ nouseroverride
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368779"
---
# <a name="locale_nouseroverride"></a>Gebiets Schema \_ nouseroverride

> [!Caution]  
> Da das Gebiets Schema " \_ nouseroverride" Benutzereinstellungen deaktiviert, wird dringend davon abgeraten. Diese Konstante garantiert keine Daten Stabilität, da [benutzerdefinierte](custom-locales.md)Gebiets Schemas, Dienst Updates, andere Betriebssystemversionen und andere Szenarien Daten auf unerwartete Weise ändern können. Weitere Informationen finden Sie unter [Verwenden von persistenten](using-persistent-locale-data.md)Gebiets Schema Daten.

 

Keine Benutzer Überschreibung. In mehreren Funktionen, z. b. [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) und [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), bewirkt diese Konstante, dass die Funktion jede Benutzer Außerkraftsetzung umgeht und den System Standardwert für jede andere Konstante verwendet, die im Funktions aufrufsausdruck angegeben ist. Die Informationen werden aus der locale-Datenbank abgerufen, auch wenn der Bezeichner das aktuelle Gebiets Schema angibt und der Benutzer einige der Werte mithilfe der Systemsteuerung geändert hat oder wenn eine Anwendung diese Werte mithilfe von [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa)geändert hat. Wenn diese Konstante nicht angegeben ist, haben alle Werte, die der Benutzer in der Systemsteuerung konfiguriert hat, oder eine Anwendung, die mithilfe von [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) konfiguriert wurde, Vorrang vor den Datenbankeinstellungen für das aktuelle Standard Gebiets Schema des Systems.

 

 



