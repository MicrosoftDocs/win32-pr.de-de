---
description: Ein Massen Verschlüsselungsschlüssel wird generiert, indem ein Hashwert eines der Mac-Schlüssel mithilfe von crypthashsessionkey und der Nachrichteninhalte und anderen Daten erzeugt wird. Die Nachricht wird mit einem der Massen Verschlüsselungsschlüssel auf die übliche Weise verschlüsselt/entschlüsselt.
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: Massendaten Verschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecfb55c162e5aa576d8baa3d0ccbc45e9588c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355431"
---
# <a name="bulk-data-encryption"></a>Massendaten Verschlüsselung

Ein [*Massen Verschlüsselungsschlüssel*](../secgloss/b-gly.md) wird generiert, indem ein [*Hashwert*](../secgloss/h-gly.md) eines der Mac-Schlüssel mithilfe von [**crypthashsessionkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) und der Nachrichteninhalte und anderen Daten erzeugt wird. Die Nachricht wird mit einem der Massen Verschlüsselungsschlüssel auf die übliche Weise verschlüsselt/entschlüsselt.

Wenn eine [*Blockchiffre*](../secgloss/b-gly.md)verwendet wird, führt die [*SChannel*](../secgloss/s-gly.md) -Protokoll-Engine alle notwendigen *Block Chiffrierung* [*aus.*](../secgloss/p-gly.md) Wenn [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) und [**cryptentschlüsseln**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) aufgerufen werden, ist das abschließende Flag immer **false** , und die Daten Länge ist ein Vielfaches ganzer Block Längen.

> [!Note]  
> Der CSP darf Daten niemals intern Puffern. Nachdem die Daten verschlüsselt (oder entschlüsselt) wurden, muss die Größe des [*Klartext*](../secgloss/p-gly.md) immer genau mit der Größe des [*Chiffre*](../secgloss/c-gly.md)Texts übereinstimmen.

 

 

 
