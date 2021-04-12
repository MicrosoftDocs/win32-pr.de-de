---
description: Eine Anwendung, die eine Sicherungs Stelle zum Speichern von Sitzungs Schlüsseln verwendet, folgt in der Regel den folgenden Schritten.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Speichern von Sitzungs Schlüsseln mithilfe einer Sicherungs Stelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345728"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>Speichern von Sitzungs Schlüsseln mithilfe einer Sicherungs Stelle

Eine Anwendung, die eine [*Sicherungs*](../secgloss/b-gly.md) Stelle zum Speichern von Sitzungs Schlüsseln verwendet, folgt in der Regel den folgenden Schritten.

**So verwenden Sie eine Sicherungs Autorität**

1.  Verschlüsseln Sie die Datei wie gewohnt.
2.  Exportieren Sie den [*Sitzungsschlüssel*](../secgloss/s-gly.md) , der zum Verschlüsseln der Datei verwendet wird, in ein [*einfaches Schlüsselblob*](../secgloss/s-gly.md), und geben Sie dabei an, dass der [*öffentliche Schlüsselaustausch*](../secgloss/k-gly.md) Schlüssel zum Verschlüsseln des Schlüssel-BLOBs verwendet werden soll Speichern Sie dieses Schlüsselblob mit der verschlüsselten Datei.
3.  Exportieren Sie den Sitzungsschlüssel erneut, und geben Sie dabei an, dass der öffentliche Schlüssel der Sicherungs Behörde verwendet werden soll, um das Schlüsselblob zu verschlüsseln. Senden Sie dieses Schlüsselblob zusammen mit der Beschreibung, der Seriennummer usw. des Schlüssels an die Sicherungs Zertifizierungsstelle.

Wenn ein [*Schlüsselpaar*](../secgloss/k-gly.md) verloren geht, können die Schlüssel von der [*Sicherungs*](../secgloss/b-gly.md) Zertifizierungsstelle abgerufen werden, wenn die Identität des Besitzers der Schlüssel festgelegt werden kann. Die Vorgehensweise zum Einrichten der Identität wird durch die Richtlinie der jeweiligen Sicherungs Stelle bestimmt und umfasst keine kryptoapi.

Den Code, der zum Erstellen eines Sitzungsschlüssels und Exportieren des Schlüssels in ein [*einfaches Schlüsselblob*](../secgloss/s-gly.md) erforderlich ist, das in eine Datenträger Datei geschrieben werden kann, finden Sie unter [Beispiel C-Programm: Exportieren eines Sitzungsschlüssels](example-c-program-exporting-a-session-key.md).

 

 
