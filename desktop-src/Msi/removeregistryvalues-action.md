---
description: Die RemoveRegistryValues-Aktion kann nur Werte aus der Systemregistrierung entfernen, die in der Registry-Tabelle oder der RemoveRegistry-Tabelle verfasst wurden.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: RemoveRegistryValues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fe284043f76cbffe3fe6a6887f46d6ab16ba65e9103efce6e4e62baac31d31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339660"
---
# <a name="removeregistryvalues-action"></a>RemoveRegistryValues-Aktion

Die RemoveRegistryValues-Aktion kann nur Werte aus der Systemregistrierung entfernen, die in der [Registry-Tabelle](registry-table.md) oder der [RemoveRegistry-Tabelle verfasst wurden.](removeregistry-table.md) Mit dieser Aktion wird ein Registrierungswert entfernt, der in der Registrierungstabelle verfasst wurde, wenn die zugeordnete Komponente lokal oder als aus der Quelle ausgeführt installiert wurde und jetzt deinstalliert werden soll. Mit dieser Aktion wird ein Registrierungswert entfernt, der in der RemoveRegistry-Tabelle verfasst wurde, wenn die zugeordnete Komponente so festgelegt ist, dass sie lokal installiert oder als aus der Quelle ausgeführt wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [InstallValidate-Aktion](installvalidate-action.md) muss aufgerufen werden, bevor RemoveRegistryValues aufgerufen wird. Wenn eine [WriteRegistryValues-Aktion](writeregistryvalues-action.md) verwendet wird, muss sie nach RemoveRegistryValues kommen. RemoveRegistryValues muss vor [UnregisterMIMEInfo](unregistermimeinfo-action.md) oder [UnregisterProgIDInfo kommen.](unregisterprogidinfo-action.md)

Eine benutzerdefinierte Aktion kann verwendet werden, um der [Registrierungstabelle](registry-table.md) während einer Installation, Deinstallation oder Reparaturtransaktion Zeilen hinzuzufügen. Diese Zeilen werden in der Registrierungstabelle nicht beibehalten, und die Informationen sind nur während der aktuellen Transaktion verfügbar. Die benutzerdefinierte Aktion muss daher in jeder Installations-, Deinstallations- oder Reparaturtransaktion ausgeführt werden, die die Informationen in diesen zusätzlichen Zeilen erfordert. Die benutzerdefinierte Aktion muss vor den Aktionen RemoveRegistryValues und [WriteRegistryValues](writeregistryvalues-action.md) in der Aktionssequenz ausgeführt werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                          |
|-------|-----------------------------------------------------|
| \[1\] | Registrierungspfad zum Schlüssel des entfernten Registrierungswerts.     |
| \[2\] | Formatierte Zeichenfolge mit dem Namen des entfernten Registrierungswerts. |



 

## <a name="remarks"></a>Hinweise

Um einen Registrierungswert zu entfernen, zeichnen Sie den Wert in der Spalte Wert der Registrierungstabelle auf. Wenn die WriteRegistryValues-Aktion REG MULTI SZ-Zeichenfolgen an den Wert in der Registry-Tabelle angefügt hat, entfernt die \_ \_ [](registry-table.md)RemoveRegistryValues-Aktion nur diese Zeichenfolgen aus dem Registrierungswert.

 

 



