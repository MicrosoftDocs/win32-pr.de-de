---
description: Die unregistercomplus-Aktion entfernt com+-Anwendungen aus der Registrierung.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Unregistercomplus-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960918"
---
# <a name="unregistercomplus-action"></a>Unregistercomplus-Aktion

Die unregistercomplus-Aktion entfernt com+-Anwendungen aus der Registrierung.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion [registercomplus](registercomplus-action.md) muss der Aktion [InstallFiles](installfiles-action.md) und der unregistercomplus-Aktion folgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Anwendungs Bezeichner der zu entfernenden com+-Anwendung. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registercomplus-Aktion](registercomplus-action.md)
</dt> <dt>

[ComPlus-Tabelle](complus-table.md)
</dt> <dt>

[Installieren einer COM+-Anwendung mit der Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



