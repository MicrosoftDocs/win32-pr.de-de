---
title: Verwalten einer Variablen Bindungs Liste
description: Die snmpgetvb-Funktion ruft Variablen Bindungs Informationen aus einer Variablen Bindungs Liste ab. Die-Funktion Ruft den Variablennamen und den zugeordneten Wert der Variablen aus dem Variablen Bindungs Eintrag ab, der von der WinSNMP-Anwendung angegeben wird.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036715"
---
# <a name="managing-a-variable-binding-list"></a>Verwalten einer Variablen Bindungs Liste

Die [**snmpgetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) -Funktion ruft Variablen Bindungs Informationen aus einer Variablen Bindungs Liste ab. Die-Funktion Ruft den Variablennamen und den zugeordneten Wert der Variablen aus dem Variablen Bindungs Eintrag ab, der von der WinSNMP-Anwendung angegeben wird.

Um Variablen Bindungs Einträge in einer Variablen Bindungs Liste zu aktualisieren, müssen Sie die [**snmpsetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) -Funktion aufrufen. Die **snmpsetvb** -Funktion fügt auch neue Variablen Bindungs Einträge an eine vorhandene Variablen Bindungs Liste an.

Die WinSNMP-Anwendung muss die [**snmpdeletevb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) -Funktion aufrufen, um Einträge aus einer Variablen Bindungs Liste zu entfernen.

Zum Abrufen, ändern oder Löschen eines Variablen Bindungs Eintrags muss in der WinSNMP-Anwendung die Position des Eintrags in der Variablen Bindungs Liste angegeben werden.

Ein Aufrufen der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion ordnet eine Variablen Bindungs Liste einem PDU zu. Ein Aufrufen der [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion Ruft eine Variablen Bindungs Liste aus einem PDU ab. Eine einzelne Variablen Bindung ist nicht direkt einem PDU zugeordnet, aber Sie ist indirekt durch die Einbindung in eine Variablen Bindungs Liste verknüpft.

 

 




