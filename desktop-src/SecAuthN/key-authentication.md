---
description: Viele Formen der Authentifizierung basieren auf der Idee, dass eine Entität Ihre Identität nachweisen kann, wenn Sie einen Schlüssel (z. b. ein Kennwort) kennt, den nur Sie kennt.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Schlüsselauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216340"
---
# <a name="key-authentication"></a>Schlüsselauthentifizierung

Viele Formen der Authentifizierung basieren auf der Idee, dass eine Entität Ihre Identität nachweisen kann, wenn Sie einen Schlüssel (z. b. ein Kennwort) kennt, den nur Sie kennt.

Authentifizierungstechniken, die auf einem geheimen Schlüssel basieren (z. b. ein Kennwort), müssen über eine Möglichkeit verfügen, das Geheimnis von öffentlichem wissen zu bewahren. Ein Kenn Wort Besitzer kann nicht zu einer Tür gehen und das Kennwort angeben. Eine Person neben dem doorkeeper könnte lauschen. oder Sie ist möglicherweise die falsche Tür. Um einen geheimen Schlüssel beizubehalten, muss ein Benutzer das Kennwort kennen, ohne das Kennwort offenzulegen. Das ist die Idee hinter der Authentifizierung mit geheimem Schlüssel, einer Überprüfungs Methode, die im gesamten [*Kerberos-Protokoll*](../secgloss/k-gly.md)verwendet wird.

Beachten Sie, dass das "Geheimnis" bei der Authentifizierung mit geheimem Schlüssel darin besteht, dass der Authentifizierungsprozess "im geheimen Schlüssel" stattfindet, ohne dass der Inhalt des Schlüssels jemals offen geht.

Damit die Authentifizierung mit geheimem Schlüssel funktioniert, müssen die beiden Parteien an eine Transaktion einen [*kryptografiesitzungsschlüssel*](../secgloss/s-gly.md) gemeinsam verwenden, der auch geheim ist, nur für Sie und für andere bekannt ist. Der Schlüssel ist [*symmetrisch*](../secgloss/s-gly.md). Das heißt, es ist ein einzelner Schlüssel, der sowohl für die Verschlüsselung als auch für die Entschlüsselung verwendet wird. Eine Partei im Authentifizierungsprozess weist ihr Wissen über den Schlüssel auf, indem Sie eine Nachricht verschlüsselt. Die andere Partei weist ihr Wissen über den Schlüssel auf, indem Sie die Nachricht entschlüsselt.

 

 
