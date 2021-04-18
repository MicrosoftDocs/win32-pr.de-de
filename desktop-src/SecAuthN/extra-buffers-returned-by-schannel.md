---
description: SChannel verfügt über einen klar definierten Satz von Verhalten für unvollständige oder übermäßige Informationen, die in den Eingabe Puffern für diese Funktionen enthalten sind.
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Von SChannel zurückgegebene zusätzliche Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352270"
---
# <a name="extra-buffers-returned-by-schannel"></a>Von SChannel zurückgegebene zusätzliche Puffer

Informationen müssen zwischen dem Client und dem Server gesendet werden, während ein [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eingerichtet wird, und danach, weil sichere Nachrichten mithilfe der von SChannel bereitgestellten Verschlüsselungs-und Entschlüsselungs Funktionen ausgetauscht werden. Die folgenden Funktionen werden zum Ausführen dieser Aufgaben verwendet:

-   [**Akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

SChannel verfügt über einen klar definierten Satz von Verhalten für unvollständige oder übermäßige Informationen, die in den Eingabe Puffern für diese Funktionen enthalten sind. Die Informationen werden auf folgende Weise zwischen Client und Server ausgetauscht:

1.  Die lokale Partei interagiert mit SChannel, indem eine SSPI-Funktion aufgerufen und Informationen übergeben werden. In der Regel wurden die Informationen von der Remote Partei empfangen.
2.  Die-Funktion gibt einen Statuscode und Ausgabepuffer zurück, die Informationen enthalten.
3.  Abhängig vom Statuscode werden die Ausgabepuffer mithilfe eines Kommunikationsmechanismus an den Remote Anbieter gesendet.
4.  Der Remote Anbieter liest von der lokalen Partei gesendete Informationen.
5.  Die Schleife wird wiederholt, wobei sich die lokalen und die Remote Parteien miteinander verbinden. (Die Remote Partei Ruft eine SSPI-Funktion auf und übergibt die im vorherigen Schritt gelesenen Informationen.)

Alles funktioniert erwartungsgemäß, wenn der Eingabepuffer der SSPI-Funktion genau die benötigten Informationen enthält. Aufgrund der Datenstrom orientierten Natur einiger Kommunikationsprotokolle ist dies jedoch möglicherweise nicht der Fall. ein von einem Remote Teilnehmer empfangener Informationsblock kann weniger Daten enthalten, als erforderlich sind, oder mehr Daten, als von SChannel in einem einzelnen Funktions Aufrufwert verarbeitet werden können.

Wenn der Eingabepuffer zu wenig Informationen enthält, geben die Funktionen "sec \_ E \_ unvollständige Nachricht" zurück \_ . Der Aufrufer muss zusätzliche Daten von der Remote Partei abrufen und die Funktion erneut aufzurufen.

Wenn die Eingabepuffer zu viele Informationen enthalten, behandelt SChannel dies nicht als Fehler. Die Funktion verarbeitet so viele der Eingaben wie möglich, und gibt den Statuscode für diese Verarbeitungs Aktivität zurück. Außerdem gibt SChannel das vorhanden sein nicht verarbeiteter Informationen in den Eingabe Puffern an, indem ein Ausgabepuffer vom Typ "secbuffer extra" zurückgegeben wird \_ . Das Testen der Ausgabepuffer für diese Art von Puffer ist die einzige Möglichkeit, diese Situation zu erkennen. Das **cbbuffer** -Feld der zusätzlichen Puffer Struktur gibt an, wie viele Bytes der Eingabe nicht verarbeitet wurden.

> [!Note]  
> Das **pvbuffer** -Feld des zusätzlichen Puffers enthält keine Kopie der überzähligen Daten.

 

Wenn Sie einen zusätzlichen Puffer von einer SSPI-Funktion erhalten, müssen Sie die bereits verarbeiteten Informationen aus dem Eingabepuffer entfernen und die Funktion erneut aufzurufen. SChannel kann und häufig nur den zusätzlichen Puffer und nichts anderes in den Ausgabe Puffern zurückgeben.

 

 
