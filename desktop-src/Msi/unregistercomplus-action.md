---
description: Die Aktion UnregisterComPlus entfernt COM+-Anwendungen aus der Registrierung.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: UnregisterComPlus-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3ed5e8e4afd853294e7f5832662e9aaf1eb122d3573e7c384115c86d994588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499850"
---
# <a name="unregistercomplus-action"></a>UnregisterComPlus-Aktion

Die Aktion UnregisterComPlus entfernt COM+-Anwendungen aus der Registrierung.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [RegisterComPlus-Aktion](registercomplus-action.md) muss der [Aktion InstallFiles](installfiles-action.md) und der Aktion UnregisterComPlus folgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Anwendungsbezeichner der COM+-Anwendung, die entfernt wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[RegisterComPlus-Aktion](registercomplus-action.md)
</dt> <dt>

[Complus-Tabelle](complus-table.md)
</dt> <dt>

[Installieren einer COM+-Anwendung mit dem Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



