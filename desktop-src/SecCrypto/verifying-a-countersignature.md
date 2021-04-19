---
description: Erläutert, wie eine gegen Signatur mithilfe von cryptmsgverifycountersignaturecodiert überprüft wird.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Überprüfen einer gegen Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348836"
---
# <a name="verifying-a-countersignature"></a>Überprüfen einer gegen Signatur

**So überprüfen Sie eine gegen Signatur**

1.  Aufrufen von [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , um ein Handle für die signierte Nachricht zu erhalten.
2.  Verschaffen Sie sich einen Zeiger auf das Zertifikat des gegen Signatur Gebers ( [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).
3.  Rufen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um die Signatur Geber Informationen aus der Nachricht abzurufen.
4.  Rufen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um die [*gegen Signatur*](../secgloss/c-gly.md) aus der Nachricht abzurufen.
5.  Sie können [**cryptmsgverifycountersignaturecodierer**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) aufrufen, um die gegen Signatur zu überprüfen.

Wenn der [**cryptmsgverifycountersignaturecodierte**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) Funktions Aufrufvorgang erfolgreich ist, wird die [*gegen Signatur*](../secgloss/c-gly.md) überprüft.

 

 
