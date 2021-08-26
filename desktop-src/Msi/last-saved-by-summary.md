---
description: Das Installationsprogramm legt die Eigenschaft Last Saved by Summary auf einen Wert fest, der davon abhängt, ob es sich um ein Installations-, Transformations- oder Patchpaket handelt. In einem Installationspaket legt das Installationsprogramm diese Eigenschaft während einer Administratorinstallation auf den Wert der LogonUser-Eigenschaft fest. Entwickler von Datenbankbearbeitungstools können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person nachzuverfolgen, die die Installationsdatenbank ändert. Diese Eigenschaft sollte in einer endgültigen Versanddatenbank auf NULL festgelegt werden. Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss sie nie ändern. In einer Transformation enthält diese Zusammenfassungseigenschaft die Plattform- und Sprach-IDs, die eine Datenbank nach der Transformation aufweisen sollte. Die -Eigenschaft gibt an, welche Vorlagenzusammenfassung in der neuen Datenbank festgelegt werden soll. In einem Patchpaket enthält diese Zusammenfassungseigenschaft eine durch Semikolons getrennte Liste von Transformationsunterstoragenamen in der Reihenfolge, in der sie von diesem Patch angewendet werden.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Last Saved By Summary -Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9299dc6a00af4e48eb3901842aba58a3c8d9a9c1d98d3a3e1e0f05bfccc4333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979450"
---
# <a name="last-saved-by-summary-property"></a>Last Saved By Summary -Eigenschaft

Das Installationsprogramm legt die Eigenschaft **Last Saved by Summary** auf einen Wert fest, der davon abhängt, ob es sich um ein Installations-, Transformations- oder Patchpaket handelt.

In einem Installationspaket legt das Installationsprogramm diese Eigenschaft während einer [Administratorinstallation](administrative-installation.md)auf den Wert der [**LogonUser-Eigenschaft**](logonuser.md) fest. Entwickler von Datenbankbearbeitungstools können diese Eigenschaft während des Entwicklungsprozesses verwenden, um die letzte Person nachzuverfolgen, die die Installationsdatenbank ändert. Diese Eigenschaft sollte in einer endgültigen Versanddatenbank auf NULL festgelegt werden. Das Installationsprogramm verwendet diese Eigenschaft nie, und ein Benutzer muss sie nie ändern.

In einer Transformation enthält diese Zusammenfassungseigenschaft die Plattform- und Sprach-IDs, die eine Datenbank nach der Transformation aufweisen sollte. Die -Eigenschaft gibt an, welche [**Vorlagenzusammenfassung**](template-summary.md) in der neuen Datenbank festgelegt werden soll.

In einem Patchpaket enthält diese Zusammenfassungseigenschaft eine durch Semikolons getrennte Liste von Transformationsunterstoragenamen in der Reihenfolge, in der sie von diesem Patch angewendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zusammenfassungseigenschaftenbeschreibungen](summary-property-descriptions.md)
</dt> </dl>

 

 




