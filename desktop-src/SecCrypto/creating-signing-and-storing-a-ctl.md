---
description: Erstellen Sie eine signierte Zertifikats Vertrauens Liste (CTL), und speichern Sie Sie in einem Zertifikat Speicher.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Erstellen, Signieren und Speichern einer CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356729"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Erstellen, Signieren und Speichern einer CTL

In den folgenden Verfahren wird eine signierte [*Zertifikats Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) erstellt und in einem [*Zertifikat Speicher*](../secgloss/c-gly.md)gespeichert.

**So erstellen und Signieren Sie eine CTL**

1.  Erstellen Sie ein Array von Elementen, die in der [*CTL*](../secgloss/c-gly.md)gespeichert werden sollen. Im Fall vertrauenswürdiger Zertifikate müssen dies die SHA1-oder MD5-Hashwerte der vertrauenswürdigen Zertifikate sein.
2.  Initialisieren Sie eine [**CTL- \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) Struktur, die das Array der soeben erstellten Elemente einschließt.
3.  Initialisieren Sie eine [**CMSG- \_ signierte \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) Struktur mit Vorzeichen.
4.  Nennen Sie [**cryptmsgencodeandsignctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). Dieser Funktions aufrub gibt einen Zeiger auf eine signierte, codierte CTL (im PKCS \# 7-Format) zurück, die die Liste der in Schritt 1 erstellten Elemente enthält.

**So fügen Sie einem Zertifikat Speicher eine CTL hinzu**

1.  Einen Zeiger auf eine signierte und codierte CTL erhalten.
2.  Öffnen Sie den Ziel Zertifikat Speicher mit einem [**certopesstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)-Rückruf.
3.  Nennen Sie [**certaddencodedctldestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).

 

 
