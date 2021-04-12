---
title: Erstellen einer Variablen Bindungs Liste
description: Die snmpkreatevbl-Funktion erstellt eine neue Variablen Bindungs Liste.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206883"
---
# <a name="creating-a-variable-binding-list"></a>Erstellen einer Variablen Bindungs Liste

Die [**snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) -Funktion erstellt eine neue Variablen Bindungs Liste. Wenn die WinSNMP-Anwendung einen Variablennamen und einen Wert angibt, erstellt die Funktion die Liste und fügt den Namen und den Wert als ersten Eintrag in der Liste hinzu. Wenn die Anwendung für den Variablennamen **null** angibt, erstellt die Funktion eine leere Liste.

Um eine Variablen Bindungs Liste zu kopieren, nennen Sie die Funktion [**snmpduplialisievbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . Die-Funktion erstellt eine neue Variablen Bindungs Liste und initialisiert die neue Liste mit einer Kopie der Daten in der Bindungs Liste der Quell Variablen.

Die Funktion [**snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) und die Funktion [**snmpduplimpevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) belegen den erforderlichen Arbeitsspeicher für die neue Variablen Bindungs Liste. Die WinSNMP-Anwendung muss die dieser Liste zugeordneten Ressourcen freigeben. Es wird empfohlen, dass die Anwendung dies durchsucht, indem Sie die einzelnen Aufrufe von [**snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) und [**snmpduplicallevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) mit einem entsprechenden Aufrufen der Funktion [**snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) vergleichen, wenn es angebracht ist, den belegten Arbeitsspeicher freizugeben.

 

 




