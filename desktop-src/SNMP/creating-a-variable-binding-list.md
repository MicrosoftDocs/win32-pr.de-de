---
title: Erstellen einer Variablenbindungsliste
description: Die SnmpCreateVbl-Funktion erstellt eine neue Variablenbindungsliste.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2530b59524375ad6413ff9aa1416db8e25ee3641136284cb4a0f70795e388a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009578"
---
# <a name="creating-a-variable-binding-list"></a>Erstellen einer Variablenbindungsliste

Die [**SnmpCreateVbl-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) erstellt eine neue Variablenbindungsliste. Wenn die WinSNMP-Anwendung einen Variablennamen und einen Wert angibt, erstellt die Funktion die Liste und fügt den Namen und den Wert als ersten Eintrag in der Liste hinzu. Wenn die Anwendung **NULL** für den Variablennamen angibt, erstellt die Funktion eine leere Liste.

Um eine Variablenbindungsliste zu kopieren, rufen Sie die [**SnmpDuplicateVbl-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) auf. Die Funktion erstellt eine neue Variablenbindungsliste und initialisiert die neue Liste mit einer Kopie der Daten in der Bindungsliste der Quellvariablen.

Die [**SnmpCreateVbl-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) und die [**SnmpDuplicateVbl-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) weisen den erforderlichen Arbeitsspeicher für die neue Variablenbindungsliste zu. Die WinSNMP-Anwendung muss die Ressourcen freigeben, die diesen Listen zugeordnet sind. Es wird empfohlen, dass die Anwendung dazu jeden Aufruf von [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) und [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) mit einem entsprechenden Aufruf der [**SnmpFreeVbl-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) abgleicht, wenn es sinnvoll ist, den belegten Arbeitsspeicher freizugeben.

 

 




