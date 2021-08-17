---
description: Die Aktion RegisterProduct registriert die Produktinformationen beim Installationsprogramm und bei "Programme hinzufügen/entfernen". Darüber hinaus speichert diese Aktion das Windows Installer-Datenbankpaket auf dem lokalen Computer.
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: RegisterProduct-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185b670b7a24c31e6dc5adb402cd6c557e2eba9eac3db5138744cd1e827113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375961"
---
# <a name="registerproduct-action"></a>RegisterProduct-Aktion

Die Aktion RegisterProduct registriert die Produktinformationen beim Installationsprogramm und bei "Programme hinzufügen/entfernen". Darüber hinaus speichert diese Aktion das Windows Installer-Datenbankpaket auf dem lokalen Computer.

Die RegisterProduct-Aktion konfiguriert die Steuerelemente, die von der Software in Systemsteuerung angezeigt werden. Weitere Informationen finden Sie unter [Konfigurieren von Programmen mit Windows Installer.](configuring-add-remove-programs-with-windows-installer.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten            |
|-------|---------------------------------------|
| \[1\] | Informationen zum registrierten Produkt. |



 

## <a name="remarks"></a>Hinweise

Die RegisterProduct-Aktion wird während der Installation auf einem Administratorinstallationspunkt nicht ausgeführt.

 

 



