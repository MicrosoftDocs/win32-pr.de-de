---
description: Überprüfen Sie die Signatur der CTL bei jeder Verwendung der CTL, damit ein interloper-CTL (Certificate Trust List, CTL) eine vorhandene CTL-Datei nicht ersetzen kann.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Überprüfen einer CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527614"
---
# <a name="verifying-a-ctl"></a>Überprüfen einer CTL

Überprüfen Sie die Signatur der CTL bei jeder Verwendung der CTL, damit ein interloper-CTL ( [*Certificate Trust List*](../secgloss/c-gly.md) , CTL) eine vorhandene CTL-Datei nicht ersetzen kann. Verwenden Sie keine CTL, die keine vertrauenswürdige Signatur enthält.

**So überprüfen Sie eine CTL-Signatur**

1.  Öffnen Sie den [*Zertifikat Speicher*](../secgloss/c-gly.md) , der die gewünschte CTL enthält.
2.  Erhalten Sie ein Handle für einen [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) für die CTL. Dies kann durch Aufrufen einer der Funktionen erfolgen, die ein Handle für den **CTL- \_ Kontext** zurückgeben, z. [**b. certfindctlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
3.  Nennen Sie [**cryptmsggetandverifysigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), und übergeben Sie dabei den in Schritt 2 des Parameters " *hcryptmsg* " abgerufenen [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) , ein Handle für den Zertifikat Speicher, das das Zertifikat der vertrauenswürdigen Quelle für CTLs im *rghsignerstore* -Parameter enthält, und das Flag "CMSG \_ Trusted \_ Signer" \_ im *dwFlags* -Parameter. Wenn die Funktion " **true**" zurückgibt, wurde die Signatur überprüft, und ein Zeiger auf den [**pccert- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) des CTL-Signatur Gebers wird im Parameter " *ppsigner* " zurückgegeben.

 

 
