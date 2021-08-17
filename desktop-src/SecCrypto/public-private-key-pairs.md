---
description: Asymmetrische Schlüssel, auch als Paare aus öffentlichen und privaten Schlüsseln bezeichnet, werden für die asymmetrische Verschlüsselung verwendet. Asymmetrische Verschlüsselung wird hauptsächlich zum Verschlüsseln und Entschlüsseln von Sitzungsschlüsseln und digitalen Signaturen verwendet. Bei der asymmetrischen Verschlüsselung werden Verschlüsselungsalgorithmen mit öffentlichem Schlüssel verwendet.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Asymmetrische Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374ba5ae17610154e306f7bdafd895116e83371ea446babfa19b5c92c29a2247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901472"
---
# <a name="asymmetric-keys"></a>Asymmetrische Schlüssel

[*Asymmetrische Schlüssel*](../secgloss/a-gly.md), auch als [*Paare aus öffentlichem und privatem Schlüssel*](../secgloss/p-gly.md)bezeichnet, werden für die asymmetrische Verschlüsselung verwendet. Asymmetrische Verschlüsselung wird hauptsächlich zum Verschlüsseln und Entschlüsseln von [*Sitzungsschlüsseln*](../secgloss/s-gly.md) und [*digitalen Signaturen*](../secgloss/d-gly.md)verwendet. Bei der asymmetrischen Verschlüsselung werden Verschlüsselungsalgorithmen mit [*öffentlichem Schlüssel*](../secgloss/p-gly.md) verwendet.

Algorithmen für öffentliche Schlüssel verwenden zwei verschiedene Schlüssel: einen [*öffentlichen und*](../secgloss/p-gly.md) einen [*privaten Schlüssel.*](../secgloss/p-gly.md) Das Element des privaten Schlüssels des Paars muss privat und sicher gehalten werden. Der öffentliche Schlüssel kann jedoch an alle Benutzer verteilt werden, die ihn anfordern. Der öffentliche Schlüssel eines Schlüsselpaars wird häufig über ein [*digitales Zertifikat*](../secgloss/c-gly.md)verteilt. Wenn ein Schlüssel eines Schlüsselpaars zum Verschlüsseln einer Nachricht verwendet wird, ist der andere Schlüssel aus diesem Paar erforderlich, um die Nachricht zu entschlüsseln. Wenn also der öffentliche Schlüssel von Benutzer A zum Verschlüsseln von Daten verwendet wird, kann nur Benutzer A (oder eine Person, die Zugriff auf den privaten Schlüssel von Benutzer A hat) die Daten entschlüsseln. Wenn der private Schlüssel von Benutzer A zum Verschlüsseln eines Datenteils verwendet wird, entschlüsselt nur der öffentliche Schlüssel von Benutzer A die Daten. Dies bedeutet, dass Benutzer A (oder eine Person mit Zugriff auf den privaten Schlüssel von Benutzer A) die Verschlüsselung durchgeführt hat.

Wenn der private Schlüssel zum Signieren einer Nachricht verwendet wird, muss der öffentliche Schlüssel aus diesem Paar verwendet werden, um die Signatur zu überprüfen. Wenn Alice beispielsweise eine digital signierte Nachricht senden möchte, würde sie die Nachricht mit ihrem privaten Schlüssel signieren, und die andere Person könnte ihre Signatur mit ihrem öffentlichen Schlüssel überprüfen. Da vermutlich nur Alice Zugriff auf ihren privaten Schlüssel hat, gibt die Tatsache, dass die Signatur mit dem öffentlichen Schlüssel von Alice überprüft werden kann, an, dass Alice die Signatur erstellt hat.

Leider sind Algorithmen mit öffentlichem Schlüssel sehr langsam, ungefähr 1.000 Mal langsamer als symmetrische Algorithmen. Es ist unpraktisch, sie zum Verschlüsseln großer Datenmengen zu verwenden. In der Praxis werden Algorithmen für öffentliche Schlüssel verwendet, um [*Sitzungsschlüssel*](../secgloss/s-gly.md)zu verschlüsseln. [*Symmetrische Algorithmen*](../secgloss/s-gly.md) werden für die Verschlüsselung/Entschlüsselung der meisten Daten verwendet.

Da das Signieren einer Nachricht tatsächlich die Nachricht verschlüsselt, ist es nicht praktikabel, Signaturalgorithmen für öffentliche Schlüssel zum Signieren großer Nachrichten zu verwenden. Stattdessen wird ein [*Hash*](../secgloss/h-gly.md) fester Länge aus der Nachricht erstellt, und der Hashwert wird signiert. Weitere Informationen finden Sie unter [Hashes und digitale Signaturen.](hashes-and-digital-signatures.md)

Jeder Benutzer verfügt im Allgemeinen über zwei [*Paare aus öffentlichem und privatem Schlüssel.*](../secgloss/p-gly.md) Ein Schlüsselpaar wird zum Verschlüsseln von Sitzungsschlüsseln und das andere zum Erstellen [*digitaler Signaturen*](../secgloss/d-gly.md)verwendet. Diese werden als [*Schlüsselaustauschschlüsselpaar*](../secgloss/k-gly.md) bzw. [*Signaturschlüsselpaar*](../secgloss/s-gly.md)bezeichnet.

Beachten Sie, dass Schlüsselcontainer, die von den meisten [*Kryptografiedienstanbietern (CSPs)*](../secgloss/c-gly.md) erstellt wurden, zwar zwei Schlüsselpaare enthalten, dies jedoch nicht erforderlich ist. Einige CSPs speichern keine [*Schlüsselpaare,*](../secgloss/k-gly.md) während andere CSPs mehr als zwei Paare speichern.

Alle Schlüssel in CryptoAPI werden in CSPs gespeichert. CSPs sind auch dafür verantwortlich, die Schlüssel zu erstellen, zu zerstören und für die Durchführung einer Vielzahl kryptografischer Vorgänge zu verwenden. Das Exportieren von Schlüsseln aus dem CSP, damit sie an andere Benutzer gesendet werden können, wird unter [Kryptografieschlüssel Storage und Exchange](cryptographic-key-storage-and-exchange.md)erläutert.

 

 
