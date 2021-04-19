---
description: Die processcomponents-Aktion registriert und hebt die Registrierung von Komponenten, Ihren Schlüssel Pfaden und den Komponenten Clients auf.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Processcomponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363654"
---
# <a name="processcomponents-action"></a>Processcomponents-Aktion

Die processcomponents-Aktion registriert und hebt die Registrierung von Komponenten, Ihren Schlüssel Pfaden und den Komponenten Clients auf. Mit der processcomponents-Aktion wird die KEYPATH-Spalte der [Component-Tabelle](component-table.md) abgefragt, um KEYPATH zu bestimmen. Diese Registrierung wird von [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) verwendet, um den Pfad einer Komponente für einen Produkt Client zurückzugeben.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion processcomponents muss nach der [InstallInitialize](installinitialize-action.md) -Aktion erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Für jede Komponente, die registriert wird.



| Feld | Beschreibung der Aktions Daten      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | ComponentID                     |
| \[3\] | Der Schlüssel Pfad für die Komponente. |



 

Für jede Komponente, deren Registrierung aufgehoben wird.



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | ComponentID                |



 

 

 



