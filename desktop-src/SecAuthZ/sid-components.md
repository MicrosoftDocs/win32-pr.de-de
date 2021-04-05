---
description: SID-Komponenten
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: SID-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041831"
---
# <a name="sid-components"></a>SID-Komponenten

Ein SID-Wert enthält Komponenten, die Informationen über die [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) -Struktur und die Komponenten bereitstellen, die einen Vertrauens nehmer eindeutig identifizieren. Eine SID besteht aus den folgenden Komponenten:

-   Die Revisions Ebene der [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) -Struktur.
-   Ein 48-Bit-bezeichnerautoritäts Wert, der die Autorität identifiziert, die die SID ausgegeben hat.
-   Eine Variable Anzahl von untergeordneten or-Rid-Werten ( [*relative Identifier*](/windows/desktop/SecGloss/r-gly) ), die den Vertrauens nehmer relativ zur Zertifizierungsstelle eindeutig identifizieren, die die SID ausgegeben hat.

Durch die Kombination aus dem Wert der bezeichnerbehörde und den Werten der untergeordneten Instanz wird sichergestellt, dass keine zwei SIDs identisch sind, auch wenn zwei verschiedene sid-ausstellende Autoritäten die gleiche Kombination von RID-Werten ausgeben. Jede sid-ausstellende Behörde gibt eine bestimmte Rid nur einmal aus.

SIDs werden im Binärformat in einer [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) -Struktur gespeichert. Um eine SID anzuzeigen, können Sie die [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) -Funktion aufrufen, um eine binäre SID in ein Zeichen folgen Format zu konvertieren. Wenn Sie eine SID-Zeichenfolge zurück in eine gültige, funktionale sid konvertieren möchten, müssen Sie die [**convertstringsidto sid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) -Funktion abrufen.

Diese Funktionen verwenden die folgende standardisierte Zeichen folgen Notation für SIDs, wodurch die Visualisierung Ihrer Komponenten vereinfacht wird:

s-*R* - *I* - *s*...

In dieser Notation identifiziert das Literalzeichen "S" die Reihen der Ziffern als sid, *R* die Revisions Ebene, *Ich bin* der Wert der Bezeichnerautorität und *S*... ist ein oder mehrere subauthority-Werte.

Im folgenden Beispiel wird diese Notation verwendet, um die bekannte Domänen relative SID der lokalen Administrator Gruppe anzuzeigen:

S-1-5-32-544

In diesem Beispiel verfügt die SID über die folgenden Komponenten. Die Konstanten in Klammern sind bekannte Bezeichnerautorität und [*RID*](/windows/desktop/SecGloss/r-gly) -Werte, die in "Winnt. h" definiert sind:

-   Eine Revisions Ebene von 1
-   Ein bezeichnerautoritäts Wert von 5 (Sicherheits- \_ NT- \_ Autorität)
-   Der erste subauthority-Wert 32 ( \_ sicherheitsbuiltin \_ Domäne \_ RID)
-   Eine zweite untergeordnete Instanz von 544 (Domänenalias- \_ \_ \_ Admins)

 

 
