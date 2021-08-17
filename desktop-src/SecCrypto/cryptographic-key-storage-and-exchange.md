---
description: Es gibt Situationen, in denen Schlüssel aus der sicheren Umgebung des Kryptografiedienstanbieters (Cryptographic Service Provider, CSP) in den Datenbereich einer Anwendung exportiert werden müssen. Exportierte Schlüssel werden in verschlüsselten Schlüssel-BLOB-Strukturen gespeichert.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Kryptografieschlüssel Storage und Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3028efb449b59deb24a7097369d8894d0876907f3555c836e95e14d8c4bf5cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768757"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Kryptografieschlüssel Storage und Exchange

Es gibt Situationen, in denen Schlüssel aus der sicheren Umgebung des [*Kryptografiedienstanbieters (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) in den Datenbereich einer Anwendung exportiert werden müssen. Exportierte Schlüssel werden in verschlüsselten [*Schlüssel-BLOB-Strukturen*](../secgloss/k-gly.md) gespeichert.

Es gibt zwei spezifische Situationen, in denen es erforderlich ist, Schlüssel zu exportieren:

-   Um einen [*Sitzungsschlüssel*](../secgloss/s-gly.md) zur späteren Verwendung durch eine Anwendung zu speichern, wenn beispielsweise eine Anwendung gerade eine Datenbankdatei verschlüsselt hat, die zu einem späteren Zeitpunkt entschlüsselt werden soll. Die Anwendung ist für das Speichern des Verschlüsselungsschlüssels verantwortlich. Dies ist erforderlich, da CSPs [*symmetrische Schlüssel*](../secgloss/s-gly.md) nicht von Sitzung zu Sitzung beibehalten.
-   So senden Sie einen Schlüssel an eine andere Person. Dies wäre einfacher, wenn die entsprechenden CSPs direkt kommunizieren könnten, aber nicht. Da CSPs nicht kommunizieren können, muss der Schlüssel von einem CSP exportiert, an die Zielanwendung übertragen und dann in den Ziel-CSP importiert werden. Dieser Prozess kann komplizierter werden, wenn der Kommunikationspfad nicht vertrauenswürdig ist.

In beiden Fällen muss eine Anwendung einen Sitzungsschlüssel außerhalb des CSP für einen bestimmten Zeitraum speichern. Weitere Informationen finden Sie unter [Vorgehensweise zum Speichern eines Sitzungsschlüssels.](procedure-for-storing-a-session-key.md)

 

 
