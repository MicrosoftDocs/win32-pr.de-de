---
description: Benutzerdefinierte Aktionen dürfen die SRSetRestorePoint-Funktion nicht aufrufen, da dies dazu führen kann, dass ein Wiederherstellungseinstiegspunkt in die Mitte einer installation Windows Installer geschrieben wird.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Festlegen eines Wiederherstellungspunkts aus einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b30dad9f8f250c0ae82286425d092538ad8324715e632e2c5074e428454f76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628580"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Festlegen eines Wiederherstellungspunkts aus einer benutzerdefinierten Aktion

Benutzerdefinierte Aktionen dürfen die [**SRSetRestorePoint-Funktion**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) nicht aufrufen, da dies dazu führen kann, dass ein Wiederherstellungseinstiegspunkt in die Mitte einer installation Windows Installer geschrieben wird.

Weitere Informationen finden Sie unter [Systemwiederherstellungspunkte und der Windows Installer.](system-restore-points-and-the-windows-installer.md)

 

 
