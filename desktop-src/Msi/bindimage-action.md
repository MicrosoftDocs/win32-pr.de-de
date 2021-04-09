---
description: Die BindImage-Aktion bindet jede ausführbare Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: BindImage-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864439"
---
# <a name="bindimage-action"></a>BindImage-Aktion

Die BindImage-Aktion bindet jede ausführbare Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss. Die BindImage-Aktion agiert für jede Datei in der [BindImage](bindimage-table.md) -Tabelle, aber nur für die, die lokal installiert werden sollen. Das Installationsprogramm berechnet die virtuelle Adresse jeder aus allen DLLs importierten Funktion und speichert dann die berechnete virtuelle Adresse in der [*Import Adress Tabelle*](i-gly.md) (IAT) des importierten Images.

Mit der BindImage-Aktion wird die Windows-API **BindImageEx** intern aufgerufen.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die BindImage-Aktion muss nach der Aktion " [InstallFiles](installfiles-action.md) " erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten     |
|-------|--------------------------------|
| \[1\] | Datei Bezeichner der ausführbaren Datei. |



 

 

 



