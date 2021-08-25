---
description: Erstellen Sie eine signierte Zertifikatvertrauensliste (Certificate Trust List, CTL), und speichern Sie sie in einem Zertifikatspeicher.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Erstellen, Signieren und Speichern einer CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f9aac8c75f7c112a09c62bb52d6e554aee7703e7f3e02c101545de5c5196db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876560"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Erstellen, Signieren und Speichern einer CTL

Mit den folgenden Verfahren wird eine [*signierte Zertifikatvertrauensliste*](../secgloss/c-gly.md) (Certificate Trust List, CTL) erstellt und in einem [*Zertifikatspeicher*](../secgloss/c-gly.md)gespeichert.

**So erstellen und signieren Sie eine CTL**

1.  Erstellen Sie ein Array von Elementen, die in der [*CTL*](../secgloss/c-gly.md)gespeichert werden sollen. Bei vertrauenswürdigen Zertifikaten müssen dies die SHA1- oder MD5-Hashes der vertrauenswürdigen Zertifikate sein.
2.  Initialisieren Sie eine [**CTL \_ INFO-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) die das Array der soeben erstellten Elemente enthält.
3.  Initialisieren sie eine [**CMSG \_ SIGNED \_ ENCODE \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
4.  Rufen Sie [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)auf. Dieser Funktionsaufruf gibt einen Zeiger auf eine signierte, codierte CTL (im PKCS \# 7-Format) zurück, die die Liste der in Schritt 1 erstellten Elemente enthält.

**So fügen Sie einem Zertifikatspeicher eine CTL hinzu**

1.  Abrufen eines Zeigers auf eine signierte und codierte CTL.
2.  Öffnen Sie den Zielzertifikatspeicher mit einem Aufruf von [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Rufen Sie [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)auf.

 

 
