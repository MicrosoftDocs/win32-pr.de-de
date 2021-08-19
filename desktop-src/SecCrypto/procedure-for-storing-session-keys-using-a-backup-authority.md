---
description: Eine Anwendung, die eine Sicherungsstelle zum Speichern von Sitzungsschlüsseln verwendet, folgt in der Regel diesen Schritten.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Speichern von Sitzungsschlüsseln mithilfe einer Sicherungsstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbd8d8fd4bebeb4b5f3c3711f4e64b9c023f57404e8d9f93200e00967dfbed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977454"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Speichern von Sitzungsschlüsseln mithilfe einer Sicherungsstelle

Eine Anwendung, die eine [*Sicherungsstelle*](../secgloss/b-gly.md) zum Speichern von Sitzungsschlüsseln verwendet, folgt in der Regel diesen Schritten.

**So verwenden Sie eine Sicherungsstelle**

1.  Verschlüsseln Sie die Datei wie gewohnt.
2.  Exportieren Sie den [*Sitzungsschlüssel,*](../secgloss/s-gly.md) der zum Verschlüsseln der Datei verwendet wird, in ein [*einfaches Schlüssel-BLOB,*](../secgloss/s-gly.md)und geben Sie dabei an, dass Ihr eigener [*öffentlicher Schlüsselaustauschschlüssel*](../secgloss/k-gly.md) zum Verschlüsseln des Schlüsselblobs verwendet werden soll. Store dieses Schlüsselblob mit der verschlüsselten Datei.
3.  Exportieren Sie den Sitzungsschlüssel erneut. Geben Sie dieses Mal an, dass der öffentliche Schlüssel der Sicherungsstelle zum Verschlüsseln des Schlüssel-BLOB verwendet werden soll. Senden Sie dieses Schlüsselblob zusammen mit der Beschreibung des Schlüssels, der Seriennummer usw. an die Sicherungsstelle.

Wenn ein [*Schlüsselpaar*](../secgloss/k-gly.md) verloren geht, können die Schlüssel von der [*Sicherungsstelle*](../secgloss/b-gly.md) abgerufen werden, wenn die Identität des Schlüsselbesitzers eingerichtet werden kann. Das Verfahren zum Einrichten der Identität wird durch die Richtlinie der jeweiligen Sicherungsstelle bestimmt und umfasst keine CryptoAPI.

Den Code, der zum Erstellen eines Sitzungsschlüssels und Exportieren dieses Schlüssels in ein [*einfaches Schlüsselblob*](../secgloss/s-gly.md) erforderlich ist, das in eine Datenträgerdatei geschrieben werden kann, finden Sie unter [Beispiel C-Programm: Exportieren eines Sitzungsschlüssels.](example-c-program-exporting-a-session-key.md)

 

 
