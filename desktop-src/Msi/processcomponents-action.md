---
description: Mit der ProcessComponents-Aktion werden Komponenten, ihre Schlüsselpfade und die Komponentenclients registriert und deren Registrierung aufgehoben.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: ProcessComponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e866c6003052922dfc0e1fca5bd4ff8ea63d207eeb03c5ada22cf5f2d3e7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259280"
---
# <a name="processcomponents-action"></a>ProcessComponents-Aktion

Mit der ProcessComponents-Aktion werden Komponenten, ihre Schlüsselpfade und die Komponentenclients registriert und deren Registrierung aufgehoben. Die ProcessComponents-Aktion fragt die KeyPath-Spalte der [Component-Tabelle](component-table.md) ab, um Schlüsselpfade zu bestimmen. Diese Registrierung wird von [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) verwendet, um den Pfad einer Komponente für einen Produktclient zurückzugeben.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die ProcessComponents-Aktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) erfolgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Für jede zu registrierende Komponente.



| Feld | Beschreibung der Aktionsdaten      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | Componentid                     |
| \[3\] | Der Schlüsselpfad für die Komponente. |



 

Für jede Komponente, deren Registrierung aufgehoben wird.



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | Componentid                |



 

 

 



