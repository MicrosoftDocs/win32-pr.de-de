---
description: Erläutert, wie eine Nachricht mithilfe von cryptmsgcountersign gegen signiert werden kann.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Gegen Signieren einer Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353574"
---
# <a name="countersigning-a-message"></a>Gegen Signieren einer Nachricht

**So setzen Sie eine signierte Nachricht mithilfe von cryptmsgcountersign gegen Signieren**

1.  Aufrufen von [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , um ein Handle für die signierte Nachricht zu erhalten.
2.  Initialisieren Sie eine [**CMSG-Signatur Geber- \_ \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) Struktur für den gegen Signatur Geber.
3.  Fügen Sie die Struktur der [**CMSG-Signatur Geber- \_ \_ \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) einem Array von gegen Signatur Bezeichnern hinzu (derzeit wird nur ein gegen Signatur Geber unterstützt).
4.  Aufrufen von [**cryptmsgcountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) zum Hinzufügen der gegen Signatur oder der gegen Signaturen.

Wenn alle Funktionsaufrufe erfolgreich sind, verfügt die ursprüngliche Nachricht nun über eine [*gegen Signatur*](../secgloss/c-gly.md) , die als nicht authentifiziertes Attribut enthalten ist.

**So setzen Sie eine signierte Nachricht mithilfe von cryptmsgcountersignencoded gegen Signieren**

1.  Aufrufen von [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , um ein Handle für die signierte Nachricht zu erhalten.
2.  Rufen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um die codierten Signatur Geber Informationen der signierten Nachricht abzurufen.
3.  Initialisieren Sie eine [**CMSG-Signatur Geber- \_ \_ \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) Struktur für den gegen Signatur Geber.
4.  Fügen Sie die Struktur der [**CMSG-Signatur Geber- \_ \_ \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) einem Array von gegen Signatur Bezeichnern hinzu (derzeit wird nur ein gegen Signatur Geber unterstützt).
5.  Rufen Sie [**cryptmsgcountersignencoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) auf, um das codierte gegen Signatur-Attribut zu erstellen.
6.  Bitten Sie [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) , das gegen Signatur-Attribut der ursprünglichen Nachricht als nicht authentifiziertes Attribut hinzuzufügen.

Wenn alle Funktionsaufrufe erfolgreich sind, wird der ursprünglichen Nachricht ein [*gegen Signatur*](../secgloss/c-gly.md) -Attribut hinzugefügt.

 

 
