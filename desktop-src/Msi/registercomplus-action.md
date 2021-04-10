---
description: Die registercomplus-Aktion registriert com+-Anwendungen.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Registercomplus-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131617"
---
# <a name="registercomplus-action"></a>Registercomplus-Aktion

Die registercomplus-Aktion registriert com+-Anwendungen.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion registercomplus muss der Aktion [InstallFiles](installfiles-action.md) und der [unregistercomplus](unregistercomplus-action.md)-Aktion folgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten              |
|-------|-----------------------------------------|
| \[1\] | Anwendungs-ID der com+-Anwendung. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ComPlus-Tabelle](complus-table.md)
</dt> <dt>

[Unregistercomplus-Aktion](unregistercomplus-action.md)
</dt> <dt>

[Installieren einer COM+-Anwendung mit der Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



