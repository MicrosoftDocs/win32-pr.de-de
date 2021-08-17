---
description: Die BindImage-Aktion bindet jede ausführbare Datei oder DLL, die an die von ihr importierten DLLs gebunden werden muss.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: BindImage-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d621728de551c182d6678561b2ef5daf649fb8fae840f47a460d83a4d38f3635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638776"
---
# <a name="bindimage-action"></a>BindImage-Aktion

Die BindImage-Aktion bindet jede ausführbare Datei oder DLL, die an die von ihr importierten DLLs gebunden werden muss. Die BindImage-Aktion wirkt sich auf jede Datei in der [BindImage-Tabelle](bindimage-table.md) aus, jedoch nur auf die Dateien, die lokal installiert werden sollen. Das Installationsprogramm berechnet die virtuelle Adresse jeder Funktion, die aus allen DLLs importiert wurde, [](i-gly.md) und speichert dann die berechnete virtuelle Adresse in der Importadressentabelle (IAT) des importierenden Images.

Die BindImage-Aktion ruft intern die **BindImageEx-Windows-API** auf.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die BindImage-Aktion muss nach der [InstallFiles-Aktion](installfiles-action.md) durchgeführt werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten     |
|-------|--------------------------------|
| \[1\] | Dateibezeichner der ausführbaren Datei. |



 

 

 



