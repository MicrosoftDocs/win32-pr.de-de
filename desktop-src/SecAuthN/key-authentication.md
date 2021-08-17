---
description: Viele Formen der Authentifizierung basieren auf der Idee, dass eine Entität ihre Identität nachweisen kann, wenn sie nachweisen kann, dass sie einen Schlüssel kennt, z. B. ein Kennwort, das nur sie kennen kann.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Schlüsselauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9273bc3fc57bca5157431ce78495f2b5c4b97595ed8513ba76fa068ef76fe0b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787262"
---
# <a name="key-authentication"></a>Schlüsselauthentifizierung

Viele Formen der Authentifizierung basieren auf der Idee, dass eine Entität ihre Identität nachweisen kann, wenn sie nachweisen kann, dass sie einen Schlüssel kennt, z. B. ein Kennwort, das nur sie kennen kann.

Authentifizierungstechniken, die auf einem Geheimnis basieren, z. B. ein Kennwort, müssen über eine Möglichkeit verfügen, das Geheimnis nicht öffentlich zu machen. Ein Kennwortbesitzer kann nicht zu einer Tür gehen und das Kennwort angeben. Jemand neben dem Doorkeeper lausft möglicherweise. Oder es kann die falsche Tür sein. Um ein Geheimnis zu behalten, muss es eine Möglichkeit geben, zu bestätigen, dass ein Benutzer das Kennwort kennt, ohne das Kennwort preiszugeben. Dies ist die Idee hinter der Authentifizierung mit geheimen Schlüsseln, einer Überprüfungsmethode, die im [*gesamten Kerberos-Protokoll verwendet wird.*](../secgloss/k-gly.md)

Beachten Sie, dass das "Geheimnis" bei der Authentifizierung mit geheimen Schlüsseln ist, dass der Authentifizierungsprozess "im Geheimen" erfolgt, d.>, ohne dass der Inhalt des Schlüssels tatsächlich preis gemacht wird.

Damit die Authentifizierung mit geheimen Schlüsseln funktioniert, [](../secgloss/s-gly.md) müssen die beiden Parteien einer Transaktion einen kryptografischen Sitzungsschlüssel gemeinsam verwenden, der ebenfalls geheim ist, der nur ihnen und keinem anderen bekannt ist. Der Schlüssel ist [*symmetrisch.*](../secgloss/s-gly.md) Das heißt, es handelt sich um einen einzelnen Schlüssel, der sowohl für die Verschlüsselung als auch für die Entschlüsselung verwendet wird. Eine Partei im Authentifizierungsprozess bestätigt ihre Kenntnis des Schlüssels, indem sie eine Nachricht verschlüsselt. Die andere Partei bestätigt ihre Kenntnis des Schlüssels, indem sie die Nachricht entschlüsselt.

 

 
