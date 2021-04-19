---
description: Mit der removeregistryvalues-Aktion können nur Werte aus der Systemregistrierung entfernt werden, die in der Registrierungs Tabelle oder der Tabelle "removeregistry" erstellt wurden.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Removeregistryvalues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360627"
---
# <a name="removeregistryvalues-action"></a>Removeregistryvalues-Aktion

Mit der removeregistryvalues-Aktion können nur Werte aus der Systemregistrierung entfernt werden, die in der [Registrierungs Tabelle](registry-table.md) oder der [Tabelle "removeregistry](removeregistry-table.md)" erstellt wurden. Diese Aktion entfernt einen Registrierungs Wert, der in der Registrierungs Tabelle erstellt wurde, wenn die zugeordnete Komponente lokal installiert wurde oder von der Quelle ausgeführt wurde und jetzt deinstalliert wurde. Diese Aktion entfernt einen Registrierungs Wert, der in der Tabelle "removeregistry" erstellt wurde, wenn die zugeordnete Komponente so festgelegt ist, dass Sie lokal installiert oder von der Quelle ausgeführt wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallValidate](installvalidate-action.md) -Aktion muss vor dem Aufruf von removeregistryvalues aufgerufen werden. Wenn eine " [schreiteregistryvalues](writeregistryvalues-action.md) "-Aktion verwendet wird, muss Sie nach "removeregistryvalues" erfolgen. ' Removeregistryvalues ' muss vor ' [unregistermimeinfo](unregistermimeinfo-action.md) ' oder ' [unregisterprogidinfo](unregisterprogidinfo-action.md)' stehen.

Eine benutzerdefinierte Aktion kann verwendet werden, um der [Registrierungs Tabelle](registry-table.md) während einer Installation, einer Neuinstallation oder einer Reparatur Transaktion Zeilen hinzuzufügen. Diese Zeilen bleiben in der Registrierungs Tabelle nicht erhalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar. Die benutzerdefinierte Aktion muss daher bei jeder Installation, deinstalstallation oder Reparatur Transaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen benötigt. Die benutzerdefinierte Aktion muss vor den Aktionen removeregistryvalues und [schreiteregistryvalues](writeregistryvalues-action.md) in der Aktions Sequenz erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                          |
|-------|-----------------------------------------------------|
| \[1\] | Der Registrierungs Pfad zum Schlüssel des entfernten Registrierungs Werts.     |
| \[2\] | Formatierte Zeichenfolge mit dem Namen des entfernten Registrierungs Werts. |



 

## <a name="remarks"></a>Bemerkungen

Notieren Sie den Wert in der Spalte Wert der Registrierungs Tabelle, um einen Registrierungs Wert zu entfernen. Wenn die Aktion "beschreiteregistryvalues" reg \_ MultiSZ-Zeichen folgen \_ an den Wert in der [Registrierungs Tabelle](registry-table.md)angehängt hat, entfernt die removeregistryvalues-Aktion nur diese Zeichen folgen aus dem Registrierungs Wert.

 

 



