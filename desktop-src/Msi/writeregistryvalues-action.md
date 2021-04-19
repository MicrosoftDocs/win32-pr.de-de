---
description: Die Aktion "beschreiteregistryvalues" richtet die Registrierungsinformationen einer Anwendung ein.
ms.assetid: ab121de3-f07d-401a-b52a-246a555c142c
title: Schreibegistryvalues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13cc5cf5a817e44caa34b9084115b7dda8cee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349482"
---
# <a name="writeregistryvalues-action"></a>Schreibegistryvalues-Aktion

Die Aktion "beschreiteregistryvalues" richtet die Registrierungsinformationen einer Anwendung ein. Die Registrierungsinformationen werden von der [Komponenten Tabelle](component-table.md)abgegrenzt. Ein Registrierungs Wert wird in die Registrierung geschrieben, wenn die entsprechende Komponente so festgelegt wurde, dass Sie entweder lokal oder als von der Quelle ausgeführt wird. Weitere Informationen finden Sie unter [Registry Table](registry-table.md).

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallValidate-Aktion](installvalidate-action.md) muss vor der Aktion "beschreiteregistryvalues" erfolgen. Wenn eine [removeregistryvalues-Aktion](removeregistryvalues-action.md)vorhanden ist, muss Sie vor der Aktion "schreiteregistryvalues" stehen.

Eine benutzerdefinierte Aktion kann verwendet werden, um der [Registrierungs Tabelle](registry-table.md) während einer Installation, einer Neuinstallation oder einer Reparatur Transaktion Zeilen hinzuzufügen. Diese Zeilen bleiben in der Registrierungs Tabelle nicht erhalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar. Die benutzerdefinierte Aktion muss daher bei jeder Installation, deinstalstallation oder Reparatur Transaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen benötigt. Die benutzerdefinierte Aktion muss vor den Aktionen [removeregistryvalues](removeregistryvalues-action.md) und schreiteregistryvalues in der Aktions Sequenz erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                               |
|-------|----------------------------------------------------------|
| \[1\] | Der Pfad zum Registrierungsschlüssel des Werts, der in die Registrierung geschrieben wurde.       |
| \[2\] | Formatierter Textzeichen folgen Name des in die Registrierung geschriebenen Werts. |
| \[3\] | Formatierte Text Zeichenfolge des in die Registrierung geschriebenen Werts.      |



 

 

 



