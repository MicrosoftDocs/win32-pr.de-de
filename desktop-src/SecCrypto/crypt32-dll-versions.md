---
description: Crypt32.dll ist das Modul, das viele der CryptoAPI-Funktionen implementiert.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750921"
---
# <a name="crypt32dll-versions"></a>Crypt32.dll Versionen

Crypt32.dll ist das Modul, das viele der Zertifikat-und kryptografienachrichtenfunktionen in der CryptoAPI implementiert, z. [**b. cryptsignmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll ist ein Modul, das in den Betriebssystemen Windows und Windows Server enthalten ist, aber unterschiedliche Versionen dieser DLL bieten unterschiedliche Funktionen. Es gibt keine API, um die verwendete kryptoapi-Version zu bestimmen, Sie können jedoch die Version von Crypt32.dll bestimmen, die derzeit verwendet wird, indem Sie die Funktionen [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) und [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) verwenden.

Im Allgemeinen werden die Versions Bereiche von Crypt32.dll den Betriebssystemversionen zugeordnet, wie in der folgenden Tabelle dargestellt. Diese Tabelle sollte jedoch nur als Richtlinie verwendet werden, da es in anderen Aktualisierungsmöglichkeiten möglich ist, dass sich die Crypt32.dll Version von der in der Tabelle aufgeführten unterscheidet.

| Crypt32.dll Version                               | Betriebssystem                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Version* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *Version* >= 5.131.2600.1243                   | Windows XP mit Service Pack 2 (SP2) Windows XP mit Service Pack 1 (SP1) mit Hotfix [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *Version* < 5.131.2600.1243 | Windows XP mit SP1Windows XP<br/>                                                                                                                                        |



 

 

 
