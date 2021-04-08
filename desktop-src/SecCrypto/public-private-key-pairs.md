---
description: Asymmetrische Schlüssel, die auch als öffentliche/private Schlüsselpaare bezeichnet werden, werden für die asymmetrische Verschlüsselung verwendet. Die asymmetrische Verschlüsselung wird hauptsächlich zum Verschlüsseln und Entschlüsseln von Sitzungs Schlüsseln und digitalen Signaturen verwendet. Die asymmetrische Verschlüsselung verwendet Verschlüsselungsalgorithmen für öffentliche Schlüssel.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Asymmetrische Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c475b1d0260bd20495d28ab542ca18c0d1cefa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759630"
---
# <a name="asymmetric-keys"></a>Asymmetrische Schlüssel

[*Asymmetrische Schlüssel*](../secgloss/a-gly.md), die auch als [*öffentliche/private Schlüsselpaare*](../secgloss/p-gly.md)bezeichnet werden, werden für die asymmetrische Verschlüsselung verwendet. Die asymmetrische Verschlüsselung wird hauptsächlich zum Verschlüsseln und Entschlüsseln von [*Sitzungs Schlüsseln*](../secgloss/s-gly.md) und [*digitalen Signaturen*](../secgloss/d-gly.md)verwendet. Die asymmetrische Verschlüsselung verwendet Verschlüsselungsalgorithmen für [*öffentliche Schlüssel*](../secgloss/p-gly.md) .

Algorithmen für öffentliche Schlüssel verwenden zwei verschiedene Schlüssel: einen [*öffentlichen Schlüssel*](../secgloss/p-gly.md) und einen [*privaten Schlüssel*](../secgloss/p-gly.md). Der private Schlüssel, der Mitglied des Paars ist, muss Privat und sicher aufbewahrt werden. Der öffentliche Schlüssel kann jedoch an jeden Benutzer verteilt werden, der ihn anfordert. Der öffentliche Schlüssel eines Schlüssel Paars wird häufig mithilfe eines [*digitalen Zertifikats*](../secgloss/c-gly.md)verteilt. Wenn ein Schlüssel eines Schlüssel Paars zum Verschlüsseln einer Nachricht verwendet wird, ist der andere Schlüssel aus diesem Paar zum Entschlüsseln der Nachricht erforderlich. Wenn also der öffentliche Schlüssel von Benutzer a zum Verschlüsseln von Daten verwendet wird, kann nur der Benutzer a (oder ein Benutzer, der Zugriff auf den privaten Schlüssel von User a hat) die Daten entschlüsseln. Wenn der private Schlüssel von Benutzer a zum Verschlüsseln von Daten verwendet wird, entschlüsselt nur der öffentliche Schlüssel von Benutzer a die Daten und gibt dadurch an, dass Benutzer a (oder jemand mit Zugriff auf den privaten Schlüssel des Benutzers a) die Verschlüsselung durchgeführt hat.

Wenn der private Schlüssel verwendet wird, um eine Nachricht zu signieren, muss der öffentliche Schlüssel aus diesem Paar zum Überprüfen der Signatur verwendet werden. Wenn Alice z. b. jemand eine Digital signierte Nachricht senden möchte, signiert Sie die Nachricht mit Ihrem privaten Schlüssel, und die andere Person könnte Ihre Signatur mithilfe Ihres öffentlichen Schlüssels verifizieren. Da nur Alice Zugriff auf Ihren privaten Schlüssel hat, gibt die Tatsache, dass die Signatur mit dem öffentlichen Schlüssel von Alice überprüft werden kann, an, dass Alice die Signatur erstellt hat.

Leider sind Algorithmen für öffentliche Schlüssel sehr langsam, ungefähr 1.000-mal langsamer als symmetrische Algorithmen. Es ist nicht praktikabel, Sie zum Verschlüsseln großer Datenmengen zu verwenden. In der Praxis werden die Algorithmen für öffentliche Schlüssel verwendet, um [*Sitzungsschlüssel*](../secgloss/s-gly.md)zu verschlüsseln. [*Symmetrische Algorithmen*](../secgloss/s-gly.md) werden verwendet, um die meisten Daten zu verschlüsseln und zu entschlüsseln.

Ebenso ist es nicht praktikabel, mithilfe von Signatur Algorithmen mit öffentlichem Schlüssel große Nachrichten zu signieren, da eine Nachricht die Nachricht tatsächlich verschlüsselt. Stattdessen wird ein [*Hashwert*](../secgloss/h-gly.md) mit fester Länge der Nachricht erstellt, und der Hashwert wird signiert. Weitere Informationen finden Sie unter [Hashes und digitale Signaturen](hashes-and-digital-signatures.md).

Jeder Benutzer hat im Allgemeinen zwei [*Schlüsselpaare aus öffentlichem und privatem Schlüssel*](../secgloss/p-gly.md). Ein Schlüsselpaar wird verwendet, um die Sitzungsschlüssel zu verschlüsseln, und das andere zum Erstellen [*digitaler Signaturen*](../secgloss/d-gly.md). Diese werden als [*Schlüsselaustausch Schlüssel-Paar*](../secgloss/k-gly.md) bzw. [*Signatur Schlüsselpaar*](../secgloss/s-gly.md)bezeichnet.

Beachten Sie, dass zwar die von den meisten [*Kryptografiedienstanbietern*](../secgloss/c-gly.md) (CSPs) erstellten Schlüssel Container zwei Schlüsselpaare enthalten, dies jedoch nicht erforderlich ist. Einige CSPs speichern keine [*Schlüsselpaare*](../secgloss/k-gly.md) , während andere CSPs mehr als zwei Paare speichern.

Alle Schlüssel in CryptoAPI werden in CSPs gespeichert. CSPs sind auch dafür verantwortlich, die Schlüssel zu erstellen, zu zerstören und Sie zum Durchführen verschiedener kryptografischer Vorgänge zu verwenden. Das Exportieren von Schlüsseln aus dem CSP, sodass diese an andere Benutzer gesendet werden können, wird unter [Kryptografieschlüssel Storage und Exchange](cryptographic-key-storage-and-exchange.md)erläutert.

 

 
