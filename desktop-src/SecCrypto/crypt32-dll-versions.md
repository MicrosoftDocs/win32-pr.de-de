---
description: Crypt32.dll ist das Modul, das viele der CryptoAPI-Funktionen implementiert.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fed9fb7e31af86673c4d24a9dd828c8d690441986725026f982c0720753c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876470"
---
# <a name="crypt32dll-versions"></a>Crypt32.dll Versionen

Crypt32.dll ist das Modul, das viele der Zertifikat- und Kryptografiemessagingfunktionen in der CryptoAPI implementiert, z. B. [**CryptSignMessage.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) Crypt32.dll ist ein Modul, das mit den Betriebssystemen Windows und Windows Server geliefert wird, aber verschiedene Versionen dieser DLL bieten unterschiedliche Funktionen. Es gibt keine API, um die version von CryptoAPI zu bestimmen, die verwendet wird, aber Sie können die Version von Crypt32.dll bestimmen, die derzeit verwendet wird, indem Sie die Funktionen [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) und [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) verwenden.

Im Allgemeinen werden die Versionsbereiche von Crypt32.dll den Betriebssystemversionen zugeordnet, wie in der folgenden Tabelle dargestellt. Diese Tabelle sollte jedoch nur als Richtlinie verwendet werden, da es durch andere Updatemöglichkeiten möglich ist, dass sich die Crypt32.dll Version von der in der Tabelle angegebenen unterscheidet.

| Crypt32.dll Version                               | Betriebssystem                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Version* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *Version* >= 5.131.2600.1243                   | Windows XP mit Service Pack 2 (SP2)Windows XP mit Service Pack 1 (SP1) mit Hotfix [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *Version* < 5.131.2600.1243 | Windows XP mit SP1Windows XP<br/>                                                                                                                                        |



 

 

 
