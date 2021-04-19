---
description: Mit der RegisterFonts-Aktion werden installierte Schriftarten beim System registriert. Durch diese Aktion wird der Schriftart Name in der FontTitle-Spalte der Schriftart Tabelle dem Pfad der installierten Schriftart Datei zugeordnet.
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: RegisterFonts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362206"
---
# <a name="registerfonts-action"></a>RegisterFonts-Aktion

Mit der RegisterFonts-Aktion werden installierte Schriftarten beim System registriert. Durch diese Aktion wird der Schriftart Name in der FontTitle-Spalte der [Schriftart Tabelle](font-table.md) dem Pfad der installierten Schriftart Datei zugeordnet.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Vor dem Aufrufen der RegisterFonts-Aktion muss die [InstallFiles](installfiles-action.md) -Aktion aufgerufen werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Schriftart Datei.                 |



 

## <a name="remarks"></a>Bemerkungen

Die Aktion RegisterFonts wird ausgeführt, wenn die Datei, die in der \_ Spalte Datei der [Schriftart Tabelle](font-table.md) angegeben ist, zu einer Komponente gehört, die installiert wird.

 

 



