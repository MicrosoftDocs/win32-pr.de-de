---
description: Die Aktion RegisterComPlus registriert COM+-Anwendungen.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: RegisterComPlus-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046d1f40293888d3a1be48a3c55fd5082b6073828c8d5cc7d34c464556986d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082640"
---
# <a name="registercomplus-action"></a>RegisterComPlus-Aktion

Die Aktion RegisterComPlus registriert COM+-Anwendungen.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RegisterComPlus-Aktion muss der [InstallFiles-Aktion](installfiles-action.md) und der [UnregisterComPlus-Aktion](unregistercomplus-action.md)folgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten              |
|-------|-----------------------------------------|
| \[1\] | Anwendungs-ID der COM+-Anwendung. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Complus-Tabelle](complus-table.md)
</dt> <dt>

[UnregisterComPlus-Aktion](unregistercomplus-action.md)
</dt> <dt>

[Installieren einer COM+-Anwendung mit dem Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



