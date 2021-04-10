---
description: Benutzerdefinierte Aktionen dürfen die SRSetRestorePoint-Funktion nicht aufzurufen, da dies dazu führen kann, dass ein Wiederherstellungs Einstiegspunkt in die Mitte einer Windows Installer-Installation geschrieben wird.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Festlegen eines Wiederherstellungs Punkts aus einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131941"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Festlegen eines Wiederherstellungs Punkts aus einer benutzerdefinierten Aktion

Benutzerdefinierte Aktionen dürfen die [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) -Funktion nicht aufzurufen, da dies dazu führen kann, dass ein Wiederherstellungs Einstiegspunkt in die Mitte einer Windows Installer-Installation geschrieben wird.

Weitere Informationen finden Sie unter [System Wiederherstellungspunkte und die Windows Installer](system-restore-points-and-the-windows-installer.md).

 

 
