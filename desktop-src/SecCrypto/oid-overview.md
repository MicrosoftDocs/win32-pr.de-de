---
description: Erweiterbarkeit wird erreicht, indem neue Objektbezeichner (OIDs), neue Codierungstypen und neue DLLs verwendet werden.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Übersicht über OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85251fa2f7084a2c0a4f691216592edaba79109af4c7651de54764a802642c90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979899"
---
# <a name="oid-overview"></a>Übersicht über OID

Erweiterbarkeit wird erreicht, indem neue [*Objektbezeichner*](../secgloss/o-gly.md) (OIDs), neue Codierungstypen und neue DLLs verwendet werden.

CryptoAPI-OIDs können eine der folgenden Formen annehmen:

-   Eine numerische Zeichenfolge wie "1.2.3.500.88"
-   Eine alphanumerische Zeichenfolge wie *MyFunction*
-   Eine Konstante mit einem Wert, der kleiner oder gleich 0xFFFF ist. Diese Konstanten werden häufig mit einem Namen verknüpft, indem eine **\# define-Anweisung** in einer Headerdatei verwendet wird.

Erweiterbare Funktionen akzeptieren OID- und Codierungstypargumente. Diese Funktionen durchsuchen die Systemregistrierung, um eine DLL zu finden, die der OID zugeordnet ist, und Codierungstypargumente, die an die Funktion übergeben werden. Wenn eine DLL für die OID gefunden wird, wird eine Codierungstypkombination gefunden, die DLL wird geladen, und ihre Funktion wird aufgerufen. Die folgende Abbildung zeigt diesen Ablauf für die [**CryptEncodeObject-Funktion:**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)

![oid-Fluss](images/oidflow.png)

Dadurch kann die Funktionalität der CryptoAPI bei Bedarf erweitert werden. Die Verwendung dieser Methodik stellt eine Belastung für den Entwickler der neuen Funktionalität dar, den gesamten erforderlichen Code für diese Funktionalität zu schreiben. Um beispielsweise eine neue Datenstruktur zu codieren, muss die Funktion in der DLL den gesamten Codierungsprozess ausführen.

 

 
