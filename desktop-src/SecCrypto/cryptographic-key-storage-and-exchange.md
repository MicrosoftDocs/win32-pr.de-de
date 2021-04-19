---
description: Es gibt Situationen, in denen Schlüssel aus der sicheren Umgebung des Kryptografiedienstanbieters (kryptografischen Service Provider, CSP) in den Datenbereich einer Anwendung exportiert werden müssen. Schlüssel, die exportiert wurden, werden in verschlüsselten Schlüsselblob-Strukturen gespeichert.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Speicherung von Kryptografieschlüsseln und Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346091"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Speicherung von Kryptografieschlüsseln und Exchange

Es gibt Situationen, in denen Schlüssel aus der sicheren Umgebung des [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) in den Datenbereich einer Anwendung exportiert werden müssen. Schlüssel, die exportiert wurden, werden in verschlüsselten [*Schlüsselblob*](../secgloss/k-gly.md) -Strukturen gespeichert.

Es gibt zwei Situationen, in denen es erforderlich ist, Schlüssel zu exportieren:

-   Zum Speichern eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) für die spätere Verwendung durch eine Anwendung, z. b. eine Anwendung, die nur eine Datenbankdatei verschlüsselt hat, die zu einem späteren Zeitpunkt entschlüsselt werden soll. Die Anwendung ist dafür verantwortlich, den Verschlüsselungsschlüssel zu speichern. Dies ist erforderlich, da CSPs keine [*symmetrischen Schlüssel*](../secgloss/s-gly.md) von der Sitzung bis zur Sitzung erhalten.
-   , Um einen Schlüssel an eine andere Person zu senden. Dies wäre einfacher, wenn die entsprechenden CSPs direkt kommunizieren könnten, dies jedoch nicht möglich ist. Da CSPs nicht kommunizieren können, muss der Schlüssel von einem CSP exportiert, an die Zielanwendung übertragen und dann in den Ziel-CSP importiert werden. Dieser Prozess kann komplizierter werden, wenn der Kommunikations Pfad nicht vertrauenswürdig ist.

In beiden Fällen muss eine Anwendung einen Sitzungsschlüssel außerhalb des CSP für einen bestimmten Zeitraum speichern. Weitere Informationen finden Sie unter [Vorgehensweise zum Speichern eines Sitzungsschlüssels](procedure-for-storing-a-session-key.md).

 

 
