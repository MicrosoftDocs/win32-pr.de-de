---
description: Nachdem eine Anforderung vom Server empfangen wurde, erstellt der Client die digestaufforderungs-Antwort durch Aufrufen der InitializeSecurityContext (Digest)-Funktion.
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: Erzeugen der digestaufforderungs-Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b577334348745425db23d3de41431ba4e37b7af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867876"
---
# <a name="generating-the-digest-challenge-response"></a>Erzeugen der digestaufforderungs-Antwort

Nachdem eine Anforderung vom Server empfangen wurde, erstellt der Client die digestaufforderungs-Antwort durch Aufrufen der [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion. Diese Funktion generiert einen MD5- [*Hash*](/windows/desktop/SecGloss/h-gly) Fingerabdruck, indem Informationen über die angeforderte Ressource und die Daten aus der Abfrage verwendet werden, und gibt ein Sicherheits Token aus, das einen partiellen [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly)darstellt. Zum Abschluss der Authentifizierung muss der Client das Token an den Server zurückgeben, der die Herausforderung ausgegeben hat.

In der folgenden Tabelle werden die Parameter der [*Funktion*](/windows/desktop/SecGloss/c-gly) [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) und die Werte beschrieben, die beim Erstellen einer digestaufforderungs-Antwort bereitgestellt werden.



| Parameter                  | BESCHREIBUNG                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *fContextReq*<br/>   | Die vom Client angeforderten Sicherheitskontext Attribute. Weitere Informationen finden Sie unter Kontext Anforderungen für digestaufforderungs-Antworten.<br/>                                                             |
| *psztargetname*<br/> | HTTP: NULL-terminierte Zeichenfolge, die die Ziel-URL angibt.<br/> SASL: NULL-terminierte Zeichenfolge, die das DNS/SPN-Ziel angibt.<br/>                                                         |
| *pinput*<br/>        | Puffer, die Informationen enthalten, die vom Digest-SSP benötigt werden. Weitere Informationen finden Sie unter [Eingabepuffer für die digestaufforderungs-Antwort](input-buffers-for-the-digest-challenge-response.md).<br/> |
| *pfContextAttr*<br/> | Empfängt die Attribute, die vom zurückgegebenen Sicherheitskontext unterstützt werden. Weitere Informationen finden Sie unter Kontext Anforderungen für digestaufforderungs-Antworten.<br/>                                                  |
| *poutput*<br/>       | Die Adresse eines secbuffer- \_ tokentyppuffers, der ein Sicherheits Token empfängt, das an den Server zurückgesendet werden soll.<br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a>Kontext Anforderungen für die Digest-Abfrage

Kontext Anforderungen sind Flags, die Folgendes bestimmen:

-   Gibt an, ob Microsoft Digest als SASL-Mechanismus oder http-Authentifizierungsprotokoll fungiert.
-   Die Qualität des Schutzes, der durch den vom Client und vom Server gemeinsam genutzten [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) unterstützt wird.

Standardmäßig Microsoft Digest Funktionen als SASL-Mechanismus.

Kontext Anforderungen werden als Flags angegeben, die an den *fContextReq* -Parameter der [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion übergeben werden. Die Flags wirken sich auf die Qualität des Sicherheits Kontexts aus, indem Sie die QoP-Direktive in der Challenge Response steuern.

Standardmäßig ist die QoP-Direktive auf "auth" festgelegt. Zum Generieren einer Challenge-Antwort, die QoP auf "auth-int" festlegt, muss Folgendes eintreten:

1.  Für die Digestherausforderung muss eine QoP-Direktive auf "auth-int" festgelegt sein.
2.  Der Client muss mindestens eines der folgenden Flags angeben:

    -   ISC \_ req- \_ Integrität
    -   ISC \_ req \_ Replay \_ Detect
    -   ISC \_ req- \_ Sequenz \_ Erkennung

Nur für SASL: Generieren Sie eine Anforderungs Antwort, bei der die QoP-Direktive auf "auth-conf" festgelegt ist, indem Sie das ISC \_ req- \_ Vertraulichkeits Kennzeichen angeben Da dieses Flag für die HTTP-Authentifizierung nicht gültig ist, kann es nicht mit dem \_ http-Flag ISC req verwendet werden \_ .

## <a name="verifying-the-quality-of-protection"></a>Überprüfen der Qualität des Schutzes

Der Client muss die im *pfContextAttr* -Parameter der [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion zurückgegebenen Flags für Sicherheitskontext Attribute untersuchen. Der Client sollte die Abfrage Antwort nur an den Server senden, wenn die von den Flags gekennzeichnete Qualität des Schutzes für seine Zwecke ausreicht. Die relevanten Flags können eine beliebige Kombination der folgenden sein:

-   ISC- \_ ret- \_ Integrität
-   ISC \_ ret \_ Replay Replay \_
-   ISC- \_ ret- \_ Sequenz \_ Erkennung
-   ISC \_ ret \_ Vertraulichkeit (nur SASL-Kontexte)

Weitere Informationen zur QoP-Direktive finden Sie unter [Qualität von Schutz und Chiffren](quality-of-protection-and-ciphers.md).

Weitere Informationen zu Challenge Response-Direktiven finden Sie unter [Content of a Digest Challenge Response](contents-of-a-digest-challenge-response.md).

 

