---
title: Objektnamen und Identitäten
description: Ein Objekt in Active Directory Domain Services verfügt über mehrere Identitäten, einschließlich der folgenden.
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- Active Directory von Objektnamen und Identitäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a803b4cc068a3ee0f9e2a75f61ff239c1d971bf3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472516"
---
# <a name="object-names-and-identities"></a>Objektnamen und Identitäten

Ein Objekt in Active Directory Domain Services verfügt über mehrere Identitäten, einschließlich der folgenden.

## <a name="relative-distinguished-name"></a>Relativer definierter Name

Der Relative Distinguished Name ist der Name, der durch das Naming-Attribut eines Objekts definiert wird. Das Attribut **rDNAttID** eines **classSchema** -Objekts identifiziert das Naming-Attribut für Instanzen der-Klasse. Die meisten Objektklassen verwenden das **CN** -Attribut (Common-Name) als Naming-Attribut. Der Relative Distinguished Name eines Objekts muss in dem Container eindeutig sein, in dem sich das Objekt befindet. Es können viele Objektinstanzen mit demselben relativen Distinguished Name vorhanden sein, aber es können sich nicht zwei in demselben Container befinden. Weitere Informationen zum **rDNAttID** -Attribut und zu **classSchema** -Objekten finden Sie unter [Eigenschaften von Objektklassen](characteristics-of-object-classes.md).

## <a name="distinguished-name"></a>Definierter Name

Der [*Distinguished Name*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) ist der aktuelle Name des Objekts und ist im Attribut "Distinguished **shedname** " des-Objekts enthalten. Der Distinguished Name ist eine Zeichenfolge, die den Speicherort des Objekts einschließt und durch Verkettung des relativen Distinguished Name des Objekts und der einzelnen seine übergeordneten Elemente bis zum Stamm gebildet wird. Der Distinguished Name des Benutzers "Users" in der Domäne "fabrikam.com" lautet z. b. "CN = Users, DC = fabrikam, DC = com". Distinguished Names sind innerhalb einer Gesamtstruktur eindeutig. Der Distinguished Name eines Objekts ändert sich, wenn das Objekt verschoben oder umbenannt wird.

## <a name="object-guid"></a>Objekt-GUID

Die Objekt-GUID ist eine Globally Unique Identifier, die von Active Directory Domain Services zugewiesen wird, wenn die Objektinstanz erstellt wird. Die Objekt-GUID ist im **objectGUID** -Attribut des-Objekts enthalten. Eine GUID ist eine 128-Bit-Zahl, die im Raum und in der Zeit garantiert eindeutig ist. Objekt-GUIDs ändern sich nie. Wenn also ein Objekt in der Enterprise-Gesamtstruktur umbenannt oder verschoben wird, bleibt die Objekt-GUID unverändert. Anwendungen, die Verweise auf Objekte in Active Directory Domain Services speichern, müssen die Objekt-GUID verwenden, um sicherzustellen, dass der Objekt Verweis einen Umbenennen des Objekts überdauert. Der Distinguished Name für ein Objekt kann sich ändern, aber die Objekt-GUID wird nicht verwendet.

## <a name="other-identities"></a>Andere Identitäten

Objektinstanzen können über viele andere Attribute verfügen, und die Attribute können zur Identifizierung durch Anwendungen verwendet werden. Beispielsweise verfügen Sicherheits Prinzipal Objekte (Instanzen der **Benutzer**-, **Computer**-und **Gruppen** Objektklassen) über die Attribute " **userPrincipalName**", " **sAMAccountName**" und " **objectSID** ". Diese Attribute sind für Windows 2000 sehr wichtig "Names", aber Sie sind nicht Teil der Objekt Identität aus der Perspektive des Verzeichnisses.

 

 