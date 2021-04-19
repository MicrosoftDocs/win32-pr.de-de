---
description: Das Installationsprogramm legt die zuletzt gespeicherte Eigenschaft durch Summary auf einen Wert fest, der davon abhängt, ob es sich um ein Installationspaket, eine Transformation oder ein Patchpaket handelt. In einem Installationspaket legt das Installationsprogramm diese Eigenschaft während einer administrativen Installation auf den Wert der LogonUser-Eigenschaft fest. Entwickler von Tools zur Datenbankbearbeitung können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person zum Ändern der Installations Datenbank zu verfolgen. Diese Eigenschaft sollte in einer abschließenden Versand Datenbank auf NULL festgelegt werden. Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss Sie nicht ändern. In einer Transformation enthält diese Zusammenfassungs Eigenschaft die Plattform-und Sprach-IDs, die eine Datenbank haben sollte, nachdem Sie transformiert wurde. Die-Eigenschaft gibt an, wie die Vorlagen Zusammenfassung in der neuen Datenbank festgelegt werden soll. In einem Patchpaket enthält diese Zusammenfassungs Eigenschaft eine durch Semikolons getrennte Liste der Namen der Transformations unter Speicher in der Reihenfolge, in der Sie von diesem Patch angewendet werden.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Zuletzt durch Summary-Eigenschaft gespeichert
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366798"
---
# <a name="last-saved-by-summary-property"></a>Zuletzt durch Summary-Eigenschaft gespeichert

Das Installationsprogramm legt die **zuletzt gespeicherte Eigenschaft durch Summary** auf einen Wert fest, der davon abhängt, ob es sich um ein Installationspaket, eine Transformation oder ein Patchpaket handelt.

In einem Installationspaket legt das Installationsprogramm diese Eigenschaft während einer [administrativen Installation](administrative-installation.md)auf den Wert der [**LogonUser**](logonuser.md) -Eigenschaft fest. Entwickler von Tools zur Datenbankbearbeitung können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person zum Ändern der Installations Datenbank zu verfolgen. Diese Eigenschaft sollte in einer abschließenden Versand Datenbank auf NULL festgelegt werden. Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss Sie nicht ändern.

In einer Transformation enthält diese Zusammenfassungs Eigenschaft die Plattform-und Sprach-IDs, die eine Datenbank haben sollte, nachdem Sie transformiert wurde. Die-Eigenschaft gibt an, wie die [**Vorlagen Zusammenfassung**](template-summary.md) in der neuen Datenbank festgelegt werden soll.

In einem Patchpaket enthält diese Zusammenfassungs Eigenschaft eine durch Semikolons getrennte Liste der Namen der Transformations unter Speicher in der Reihenfolge, in der Sie von diesem Patch angewendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




